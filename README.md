<!DOCTYPE html>
<html lang="ar" dir="rtl" class="h-full bg-slate-950 text-slate-100">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منظومة إدارة وتخطيط المدارس 1448هـ | بشر بن عاصم والتحفيظ برابغ</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- Google Fonts: Tajawal -->
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800;900&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: { sans: ['Tajawal', 'sans-serif'] },
                    colors: {
                        brand: {
                            bg: '#090d16', card: '#111827', border: '#1f293d',
                            accent: '#10b981', gold: '#f59e0b', blue: '#3b82f6', purple: '#8b5cf6'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body { font-family: 'Tajawal', sans-serif; background-color: #090d16; color: #f8fafc; }
        .custom-scrollbar::-webkit-scrollbar { width: 6px; }
        .custom-scrollbar::-webkit-scrollbar-track { background: #090d16; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: #10b981; border-radius: 10px; }
        @media print {
            .no-print { display: none !important; }
            .print-area { background: white !important; color: black !important; padding: 0 !important; width: 100% !important; }
            body { background: white !important; color: black !important; }
            .tab-panel:not(.active-print) { display: none !important; }
            .sched-subtab-panel:not(.active-print) { display: none !important; }
        }
    </style>
</head>
<body class="h-full flex overflow-hidden antialiased custom-scrollbar">

    <!-- SIDEBAR NAVIGATION (الشريط الجانبي) -->
    <aside class="w-72 bg-brand-card border-l border-brand-border flex flex-col justify-between z-50 no-print flex-shrink-0">
        <div class="p-4 space-y-6 overflow-y-auto custom-scrollbar flex-1">
            <!-- Header Identity -->
            <div class="flex items-center gap-3 border-b border-brand-border pb-4">
                <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-emerald-600 to-teal-400 flex items-center justify-center text-white shadow-lg shadow-emerald-900/40 flex-shrink-0">
                    <i class="fa-solid fa-graduation-cap text-2xl"></i>
                </div>
                <div>
                    <h1 class="font-black text-sm text-white leading-tight">منظومة التخطيط المالي والإداري 1448 هـ</h1>
                    <p class="text-[10px] text-emerald-400 font-bold mt-1">بشر بن عاصم والتحفيظ برابغ</p>
                </div>
            </div>

            <!-- Navigation Links -->
            <nav class="space-y-1.5 text-xs font-bold">
                <button onclick="switchTab('dashboard')" id="nav-dashboard" class="nav-btn active w-full px-3.5 py-3 rounded-xl bg-emerald-600 text-white flex items-center gap-3 transition">
                    <i class="fa-solid fa-chart-pie text-base w-5 text-center"></i> لوحة المؤشرات الرئيسية
                </button>
                <button onclick="switchTab('term1-programs')" id="nav-term1-programs" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-list-check text-emerald-400 text-base w-5 text-center"></i> متابعة البرامج الفصل الأول
                </button>
                <button onclick="switchTab('term2-indicators')" id="nav-term2-indicators" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-chart-line text-blue-400 text-base w-5 text-center"></i> متابعة المؤشرات الفصل الثاني
                </button>
                <button onclick="switchTab('schedules')" id="nav-schedules" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-calendar-days text-amber-400 text-base w-5 text-center"></i> الجداول المدرسية
                </button>
                <button onclick="switchTab('vision')" id="nav-vision" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-eye text-emerald-400 text-base w-5 text-center"></i> الرؤية والرسالة والقيم
                </button>
                <button onclick="switchTab('evaluation')" id="nav-evaluation" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-chart-simple text-brand-gold text-base w-5 text-center"></i> نتائج التقويم الخارجي
                </button>
                <button onclick="switchTab('swot')" id="nav-swot" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-magnifying-glass-chart text-blue-400 text-base w-5 text-center"></i> تشخيص الواقع (SWOT)
                </button>
                <button onclick="switchTab('risk')" id="nav-risk" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-shield-halved text-rose-400 text-base w-5 text-center"></i> سجل إدارة المخاطر
                </button>
                <button onclick="switchTab('cards')" id="nav-cards" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-id-card text-teal-400 text-base w-5 text-center"></i> بطاقات البرامج الشاملة
                </button>
                <button onclick="switchTab('committees')" id="nav-committees" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-users-gear text-brand-gold text-base w-5 text-center"></i> اللجان المدرسية الأربعة
                </button>
                <button onclick="switchTab('links')" id="nav-links" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-globe text-purple-400 text-base w-5 text-center"></i> المواقع المنصات اليومية
                </button>
                <button onclick="switchTab('files')" id="nav-files" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-folder-open text-amber-400 text-base w-5 text-center"></i> مركز إدارة الملفات
                </button>
                <button onclick="switchTab('data')" id="nav-data" class="nav-btn w-full px-3.5 py-3 rounded-xl text-slate-300 hover:bg-slate-800 flex items-center gap-3 transition">
                    <i class="fa-solid fa-school text-emerald-400 text-base w-5 text-center"></i> بيانات وإحصائيات المدرسة
                </button>
            </nav>
        </div>

        <div class="p-4 border-t border-brand-border space-y-2">
            <button onclick="window.print()" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white py-2.5 rounded-xl text-xs font-bold transition flex items-center justify-center gap-2 shadow-lg">
                <i class="fa-solid fa-print"></i> طباعة التقرير الشامل
            </button>
        </div>
    </aside>

    <!-- MAIN CONTENT AREA (منطقة العرض الرئيسية) -->
    <main class="flex-1 overflow-y-auto p-8 space-y-8 custom-scrollbar">

        <!-- TAB 0: DASHBOARD -->
        <section id="tab-dashboard" class="tab-panel space-y-6">
            <div class="flex justify-between items-center bg-brand-card p-6 rounded-2xl border border-brand-border">
                <div>
                    <h2 class="text-xl font-black text-white flex items-center gap-2">
                        <i class="fa-solid fa-chart-pie text-emerald-400"></i> لوحة الأداء ومؤشرات الإنجاز الرئيسية (KPIs Dashboard)
                    </h2>
                    <p class="text-xs text-slate-400 mt-1">متابعة المبادرات، ونسب التقدم، وتوزيع الميزانية للعام الدراسي 1448 هـ</p>
                </div>
            </div>

            <!-- Stats Overview Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border">
                    <p class="text-xs text-slate-400 font-bold mb-1">نسبة الإنجاز العامة للخطة</p>
                    <div class="text-3xl font-black text-emerald-400" id="overallProgress">0%</div>
                    <div class="w-full bg-slate-800 h-2 rounded-full mt-2 overflow-hidden">
                        <div id="overallBar" class="bg-emerald-500 h-full w-0 transition-all duration-500"></div>
                    </div>
                </div>
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border">
                    <p class="text-xs text-slate-400 font-bold mb-1">البرامج المكتملة 100%</p>
                    <div class="text-3xl font-black text-white" id="completedCount">0 / 24</div>
                    <p class="text-[10px] text-emerald-400 mt-2">مكتملة وموثقة بالشواهد</p>
                </div>
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border">
                    <p class="text-xs text-slate-400 font-bold mb-1">إجمالي الميزانية المرصودة</p>
                    <div class="text-3xl font-black text-white">7,000 <span class="text-xs text-slate-400 font-normal">ريال</span></div>
                    <p class="text-[10px] text-slate-400 mt-2">موزعة على المجالات الـ 4</p>
                </div>
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border">
                    <p class="text-xs text-slate-400 font-bold mb-1">إجمالي البرامج المسجلة</p>
                    <div class="text-3xl font-black text-brand-gold" id="totalProgramsCount">24 برنامجاً</div>
                    <p class="text-[10px] text-slate-400 mt-2">مربوطة بمعايير الاعتماد ETEC</p>
                </div>
            </div>

            <!-- Domain Progress Cards -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
                <div class="bg-slate-900/90 p-4 rounded-2xl border border-slate-800 space-y-2">
                    <span class="text-xs text-emerald-400 font-bold">1. الإدارة المدرسية</span>
                    <p class="text-lg font-black text-white">5 برامج (1,000 ريال)</p>
                    <p class="text-[11px] text-slate-400">الحوكمة والتخطيط والشراكة</p>
                </div>
                <div class="bg-slate-900/90 p-4 rounded-2xl border border-slate-800 space-y-2">
                    <span class="text-xs text-blue-400 font-bold">2. التعليم والتعلم</span>
                    <p class="text-lg font-black text-white">6 برامج (1,300 ريال)</p>
                    <p class="text-[11px] text-slate-400">الاستراتيجيات والتحول الرقمي</p>
                </div>
                <div class="bg-slate-900/90 p-4 rounded-2xl border border-slate-800 space-y-2">
                    <span class="text-xs text-brand-gold font-bold">3. نواتج التعلم</span>
                    <p class="text-lg font-black text-white">7 برامج (2,200 ريال)</p>
                    <p class="text-[11px] text-slate-400">نافس والتحصيل والقيم والابتكار</p>
                </div>
                <div class="bg-slate-900/90 p-4 rounded-2xl border border-slate-800 space-y-2">
                    <span class="text-xs text-purple-400 font-bold">4. البيئة المدرسية</span>
                    <p class="text-lg font-black text-white">6 برامج (2,500 ريال)</p>
                    <p class="text-[11px] text-slate-400">الأمن والسلامة والوصول الشامل</p>
                </div>
            </div>

        </section>

        <!-- TAB 1: TERM 1 PROGRAM TRACKING -->
        <section id="tab-term1-programs" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border">
                <h2 class="text-xl font-black text-white flex items-center gap-2">
                    <i class="fa-solid fa-list-check text-emerald-400"></i> متابعة البرامج الفصل الأول
                </h2>
                <p class="text-xs text-slate-400 mt-1">رصد البرامج التشغيلية ومواعيد التنفيذ والشواهد خلال الفصل الدراسي الأول</p>
            </div>
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <div class="flex justify-between items-center">
                    <h3 class="font-black text-lg text-white">خطة البرامج التشغيلية للفصل الأول</h3>
                    <button onclick="window.print()" class="no-print bg-emerald-600 hover:bg-emerald-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold flex items-center gap-2">
                        <i class="fa-solid fa-print"></i> طباعة
                    </button>
                </div>
                <div class="overflow-x-auto">
                    <table class="w-full text-xs text-right border-collapse">
                        <thead>
                            <tr class="bg-slate-800 text-slate-300 font-bold border-b border-slate-700">
                                <th class="p-3">م</th><th class="p-3">اسم البرنامج</th><th class="p-3">المسؤول</th><th class="p-3">موعد الفصل الأول</th><th class="p-3">الشواهد</th><th class="p-3 w-48">نسبة الإنجاز</th>
                            </tr>
                        </thead>
                        <tbody id="term1ProgramsTableBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                    </table>
                </div>
            </div>
        </section>

        <!-- TAB 2: TERM 2 INDICATOR TRACKING -->
        <section id="tab-term2-indicators" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border">
                <h2 class="text-xl font-black text-white flex items-center gap-2">
                    <i class="fa-solid fa-chart-line text-blue-400"></i> متابعة المؤشرات الفصل الثاني
                </h2>
                <p class="text-xs text-slate-400 mt-1">متابعة المؤشرات التشغيلية المستهدفة وقياس مستوى التقدم خلال الفصل الدراسي الثاني</p>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border"><p class="text-xs text-slate-400 font-bold">متوسط المؤشرات</p><div id="term2OverallProgress" class="text-3xl font-black text-blue-400 mt-1">0%</div></div>
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border"><p class="text-xs text-slate-400 font-bold">المؤشرات المكتملة</p><div id="term2CompletedCount" class="text-3xl font-black text-white mt-1">0</div></div>
                <div class="bg-brand-card p-5 rounded-2xl border border-brand-border"><p class="text-xs text-slate-400 font-bold">عدد المؤشرات المسجلة</p><div id="term2TotalCount" class="text-3xl font-black text-brand-gold mt-1">0</div></div>
            </div>
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <div class="flex justify-between items-center">
                    <h3 class="font-black text-lg text-white">سجل مؤشرات الفصل الثاني</h3>
                    <button onclick="window.print()" class="no-print bg-blue-600 hover:bg-blue-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold flex items-center gap-2">
                        <i class="fa-solid fa-print"></i> طباعة
                    </button>
                </div>
                <div class="overflow-x-auto">
                    <table class="w-full text-xs text-right border-collapse">
                        <thead>
                            <tr class="bg-slate-800 text-slate-300 font-bold border-b border-slate-700">
                                <th class="p-3">م</th><th class="p-3">البرنامج / المؤشر</th><th class="p-3">المؤشر المستهدف</th><th class="p-3">موعد القياس</th><th class="p-3">مصدر التحقق</th><th class="p-3 w-48">نسبة الإنجاز</th>
                            </tr>
                        </thead>
                        <tbody id="term2IndicatorsTableBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                    </table>
                </div>
            </div>
        </section>

        <!-- SCHEDULES TAB (الجداول المدرسية) -->
        <section id="tab-schedules" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <div class="flex justify-between items-center border-b border-slate-800 pb-4">
                    <div>
                        <h2 class="text-xl font-black text-white flex items-center gap-2">
                            <i class="fa-solid fa-calendar-days text-amber-400"></i> إدارة الجداول المدرسية
                        </h2>
                        <p class="text-xs text-slate-400 mt-1">تصفح وتعديل جداول المعلمين، الفصول، الانتظار، الإشراف والمناوبة تلقائياً</p>
                    </div>
                </div>

                <!-- SUB TABS NAVIGATION FOR SCHEDULES -->
                <div class="flex border-b border-slate-800 text-xs font-bold gap-2 overflow-x-auto pb-2 no-print">
                    <button onclick="switchSchedSubTab('teachers-sched')" id="sched-btn-teachers-sched" class="sched-subtab-btn active px-4 py-2.5 rounded-xl bg-emerald-600 text-white transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-chalkboard-user text-emerald-200"></i> 1. جداول المعلمين
                    </button>
                    <button onclick="switchSchedSubTab('classes-sched')" id="sched-btn-classes-sched" class="sched-subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-users text-blue-400"></i> 2. جداول الفصول
                    </button>
                    <button onclick="switchSchedSubTab('waiting-sched')" id="sched-btn-waiting-sched" class="sched-subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-clock-rotate-left text-rose-400"></i> 3. جدول الانتظار
                    </button>
                    <button onclick="switchSchedSubTab('supervision-sched')" id="sched-btn-supervision-sched" class="sched-subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-eye text-purple-400"></i> 4. جدول الإشراف
                    </button>
                    <button onclick="switchSchedSubTab('monawaba-sched')" id="sched-btn-monawaba-sched" class="sched-subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-user-shield text-teal-400"></i> 5. جدول المناوبة
                    </button>
                </div>

                <!-- SUB TAB 1: TEACHERS SCHEDULE (جداول المعلمين) -->
                <div id="sched-teachers-sched" class="sched-subtab-panel space-y-4 pt-2">
                    <div class="flex justify-between items-center no-print">
                        <div class="flex items-center gap-3">
                            <h3 class="font-black text-sm text-emerald-400"><i class="fa-solid fa-chalkboard-user"></i> جداول المعلمين التفصيلية المفرغة</h3>
                            <select id="teacherSelectFilter" onchange="renderTeacherIndividualSchedule()" class="bg-slate-900 border border-slate-700 rounded-xl px-3 py-2 text-xs text-emerald-300 font-bold max-w-xs"></select>
                        </div>
                        <button onclick="printSingleSection('sched-teachers-sched')" class="bg-emerald-600 hover:bg-emerald-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition flex items-center gap-2 shadow-md">
                            <i class="fa-solid fa-print"></i> طباعة جدول المعلم
                        </button>
                    </div>
                    <div class="overflow-x-auto print-area bg-slate-900 p-4 rounded-2xl border border-slate-800">
                        <div class="hidden print:block text-center font-black text-lg mb-4 text-black" id="printTeacherTitle">جدول المعلم</div>
                        <table class="w-full text-xs text-center border-collapse border border-slate-700">
                            <thead>
                                <tr class="bg-slate-800 text-slate-200 font-bold border-b border-slate-700">
                                    <th class="p-2.5 border border-slate-700 w-24">اليوم / الحصة</th>
                                    <th class="p-2.5 border border-slate-700">1</th>
                                    <th class="p-2.5 border border-slate-700">2</th>
                                    <th class="p-2.5 border border-slate-700">3</th>
                                    <th class="p-2.5 border border-slate-700">4</th>
                                    <th class="p-2.5 border border-slate-700">5</th>
                                    <th class="p-2.5 border border-slate-700">6</th>
                                    <th class="p-2.5 border border-slate-700">7</th>
                                </tr>
                            </thead>
                            <tbody id="individualTeacherSchedBody" class="divide-y divide-slate-800 text-slate-200"></tbody>
                        </table>
                    </div>
                </div>

                <!-- SUB TAB 2: CLASSES SCHEDULE (جداول الفصول) -->
                <div id="sched-classes-sched" class="sched-subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center no-print">
                        <div class="flex items-center gap-3">
                            <h3 class="font-black text-sm text-blue-400"><i class="fa-solid fa-users"></i> جداول الفصول الدراسية المفرغة</h3>
                            <select id="classSelectFilter" onchange="renderClassIndividualSchedule()" class="bg-slate-900 border border-slate-700 rounded-xl px-3 py-2 text-xs text-blue-300 font-bold">
                                <option value="ع4-1">عام 4-1 (بشر بن عاصم)</option>
                                <option value="ع5-1">عام 5-1 (بشر بن عاصم)</option>
                                <option value="ع5-2">عام 5-2 (بشر بن عاصم)</option>
                                <option value="ع6-1">عام 6-1 (بشر بن عاصم)</option>
                                <option value="ت3-1">تحفيظ 3-1 (تحفيظ القرآن)</option>
                                <option value="ت3-2">تحفيظ 3-2 (تحفيظ القرآن)</option>
                                <option value="ت4-1">تحفيظ 4-1 (تحفيظ القرآن)</option>
                                <option value="ت4-2">تحفيظ 4-2 (تحفيظ القرآن)</option>
                                <option value="ت5-1">تحفيظ 5-1 (تحفيظ القرآن)</option>
                                <option value="ت5-2">تحفيظ 5-2 (تحفيظ القرآن)</option>
                                <option value="ت6-1">تحفيظ 6-1 (تحفيظ القرآن)</option>
                                <option value="ت6-2">تحفيظ 6-2 (تحفيظ القرآن)</option>
                            </select>
                        </div>
                        <button onclick="printSingleSection('sched-classes-sched')" class="bg-blue-600 hover:bg-blue-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition flex items-center gap-2 shadow-md">
                            <i class="fa-solid fa-print"></i> طباعة جدول الفصل
                        </button>
                    </div>
                    <div class="overflow-x-auto print-area bg-slate-900 p-4 rounded-2xl border border-slate-800">
                        <div class="hidden print:block text-center font-black text-lg mb-4 text-black" id="printClassTitle">جدول الفصل</div>
                        <table class="w-full text-xs text-center border-collapse border border-slate-700">
                            <thead>
                                <tr class="bg-slate-800 text-slate-200 font-bold border-b border-slate-700">
                                    <th class="p-2.5 border border-slate-700 w-24">اليوم / الحصة</th>
                                    <th class="p-2.5 border border-slate-700">1</th>
                                    <th class="p-2.5 border border-slate-700">2</th>
                                    <th class="p-2.5 border border-slate-700">3</th>
                                    <th class="p-2.5 border border-slate-700">4</th>
                                    <th class="p-2.5 border border-slate-700">5</th>
                                    <th class="p-2.5 border border-slate-700">6</th>
                                    <th class="p-2.5 border border-slate-700">7</th>
                                </tr>
                            </thead>
                            <tbody id="individualClassSchedBody" class="divide-y divide-slate-800 text-slate-200"></tbody>
                        </table>
                    </div>
                </div>

                <!-- SUB TAB 3: WAITING SCHEDULE (جدول الانتظار) -->
                <div id="sched-waiting-sched" class="sched-subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center no-print">
                        <div>
                            <h3 class="font-black text-sm text-rose-400"><i class="fa-solid fa-clock-rotate-left"></i> جدول حصص الانتظار والاحتياط المعتمد</h3>
                            <p class="text-xs text-slate-400 mt-0.5">جدول مستخرج ومطابق للسجل المعتمد بالمدرسة مع إمكانية التعديل</p>
                        </div>
                        <button onclick="printSingleSection('sched-waiting-sched')" class="bg-rose-600 hover:bg-rose-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition flex items-center gap-2 shadow-md">
                            <i class="fa-solid fa-print"></i> طباعة جدول الانتظار
                        </button>
                    </div>
                    <div class="overflow-x-auto print-area bg-slate-900 p-4 rounded-2xl border border-slate-800">
                        <div class="hidden print:block text-center font-black text-lg mb-4 text-black">
                            جدول الانتظار والاحتياط اليومي - مدرسة بشر بن عاصم وتحفيظ القرآن الكريم برابغ 1448 هـ
                        </div>
                        <table class="w-full text-xs text-center border-collapse border border-slate-700">
                            <thead>
                                <tr class="bg-slate-800 text-slate-200 font-bold border-b border-slate-700">
                                    <th class="p-2.5 border border-slate-700 w-24">اليوم / الحصة</th>
                                    <th class="p-2.5 border border-slate-700">1</th>
                                    <th class="p-2.5 border border-slate-700">2</th>
                                    <th class="p-2.5 border border-slate-700">3</th>
                                    <th class="p-2.5 border border-slate-700">4</th>
                                    <th class="p-2.5 border border-slate-700">5</th>
                                    <th class="p-2.5 border border-slate-700">6</th>
                                    <th class="p-2.5 border border-slate-700">7</th>
                                </tr>
                            </thead>
                            <tbody id="waitingSchedBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                        </table>
                    </div>
                </div>

                <!-- SUB TAB 4: SUPERVISION SCHEDULE (جدول الإشراف) -->
                <div id="sched-supervision-sched" class="sched-subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center no-print">
                        <div>
                            <h3 class="font-black text-sm text-purple-400"><i class="fa-solid fa-eye"></i> جدول الإشراف الأسبوعي (إشراف الفسحة 9:16 ص – 9:39 ص)</h3>
                            <p class="text-xs text-slate-400 mt-0.5">التوزيع المعتمد لمواقع الإشراف بالمقصف والساحات خلال الفسحة</p>
                        </div>
                        <button onclick="printSingleSection('sched-supervision-sched')" class="bg-purple-600 hover:bg-purple-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition flex items-center gap-2 shadow-md">
                            <i class="fa-solid fa-print"></i> طباعة جدول الإشراف
                        </button>
                    </div>
                    <div class="overflow-x-auto print-area bg-slate-900 p-4 rounded-2xl border border-slate-800">
                        <div class="hidden print:block text-center font-black text-lg mb-4 text-black">
                            جدول الإشراف اليومي والميداني (إشراف الفسحة) - 1448 هـ
                        </div>
                        <table class="w-full text-xs text-center border-collapse border border-slate-700">
                            <thead>
                                <tr class="bg-slate-800 text-slate-200 font-bold border-b border-slate-700">
                                    <th class="p-2.5 border border-slate-700 w-28">اليوم</th>
                                    <th class="p-2.5 border border-slate-700">المشرفون المكلفون بالمقصف والساحة الرئيسية</th>
                                </tr>
                            </thead>
                            <tbody id="supervisionSchedBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                        </table>
                    </div>
                </div>

                <!-- SUB TAB 5: MONAWABA SCHEDULE (جدول المناوبة) -->
                <div id="sched-monawaba-sched" class="sched-subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center no-print">
                        <div>
                            <h3 class="font-black text-sm text-teal-400"><i class="fa-solid fa-user-shield"></i> جدول سجل المناوبة اليومية المباشرة</h3>
                            <p class="text-xs text-slate-400 mt-0.5">قائمة مرنة ومخصصة لإدخال وإضافة التواريخ والمعلمين المناوبين</p>
                        </div>
                        <div class="flex gap-2">
                            <button onclick="addMonawabaRow()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition">+ إضافة صف مناوبة جديد</button>
                            <button onclick="printSingleSection('sched-monawaba-sched')" class="bg-teal-600 hover:bg-teal-500 text-white px-3.5 py-2 rounded-xl text-xs font-bold transition flex items-center gap-2 shadow-md">
                                <i class="fa-solid fa-print"></i> طباعة جدول المناوبة
                            </button>
                        </div>
                    </div>
                    <div class="overflow-x-auto print-area bg-slate-900 p-4 rounded-2xl border border-slate-800">
                        <div class="hidden print:block text-center font-black text-lg mb-4 text-black">
                            سجل وجدول المناوبة المدرسية اليومية - 1448 هـ
                        </div>
                        <table class="w-full text-xs text-right border-collapse border border-slate-700">
                            <thead>
                                <tr class="bg-slate-800 text-slate-200 font-bold border-b border-slate-700">
                                    <th class="p-2.5 border border-slate-700 text-center w-12">م</th>
                                    <th class="p-2.5 border border-slate-700 w-28">اليوم</th>
                                    <th class="p-2.5 border border-slate-700 w-36">التاريخ</th>
                                    <th class="p-2.5 border border-slate-700">اسم المعلم المناوب</th>
                                    <th class="p-2.5 border border-slate-700">الموقع / الملاحظات</th>
                                    <th class="p-2.5 border border-slate-700 text-center no-print w-16">حذف</th>
                                </tr>
                            </thead>
                            <tbody id="monawabaSchedBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                        </table>
                    </div>
                </div>

            </div>
        </section>

        <!-- TAB 2: VISION & MISSION & VALUES -->
        <section id="tab-vision" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-2">
                <h2 class="text-xl font-black text-white flex items-center gap-2">
                    <i class="fa-solid fa-eye text-emerald-400"></i> الرؤية والرسالة والقيم الجوهرية للتعليم
                </h2>
                <p class="text-xs text-slate-400">المرتكزات الأساسية للعمل التربوي والتعليمي بمدرسة بشر بن عاصم وتحفيظ القرآن الكريم برابغ 1448 هـ</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-gradient-to-br from-slate-900 to-emerald-950/40 p-6 rounded-2xl border border-emerald-500/30 space-y-3 shadow-xl">
                    <div class="w-12 h-12 rounded-xl bg-emerald-500/20 text-emerald-400 flex items-center justify-center font-black text-2xl"><i class="fa-solid fa-compass"></i></div>
                    <h3 class="font-black text-lg text-emerald-400">الرؤية</h3>
                    <p class="text-sm font-bold text-slate-200 leading-relaxed">بناء جيلٍ متميز علمياً، متمسكٍ بقيم القرآن والهوية الوطنية، ومؤهلٍ بكفايات المستقبل للريادة والمنافسة.</p>
                </div>

                <div class="bg-gradient-to-br from-slate-900 to-teal-950/40 p-6 rounded-2xl border border-teal-500/30 space-y-3 shadow-xl">
                    <div class="w-12 h-12 rounded-xl bg-teal-500/20 text-teal-400 flex items-center justify-center font-black text-2xl"><i class="fa-solid fa-paper-plane"></i></div>
                    <h3 class="font-black text-lg text-teal-400">الرسالة</h3>
                    <p class="text-sm font-bold text-slate-200 leading-relaxed">تقديم تعليم نوعي محفز يجمع بين تعزير القيم الإسلامية والعناية بكتاب الله، وتنمية المهارات الأساسية والمستقبلية لطلابنا في بيئة مدرسية آمنة وجاذبة، بشراكة مجتمعية فاعلة وكوادر تربوية مؤهلة.</p>
                </div>
            </div>

            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <h3 class="font-black text-lg text-white flex items-center gap-2"><i class="fa-solid fa-gem text-brand-gold"></i> القيم الجوهرية والمفهوم التطبيقي</h3>
                <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5 gap-4 text-xs">
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 space-y-2">
                        <div class="text-emerald-400 font-black text-sm">1. التقوى والاعتزاز بالهوية</div>
                        <p class="text-slate-300 leading-relaxed">العناية بكتاب الله تعالى وغرس القدوة الحسنة والانتماء للوطن.</p>
                    </div>
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 space-y-2">
                        <div class="text-emerald-400 font-black text-sm">2. الإتقان والجودة</div>
                        <p class="text-slate-300 leading-relaxed">السعي المستمر لتحقيق التميز في نواتج التعلم والأداء الميداني.</p>
                    </div>
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 space-y-2">
                        <div class="text-emerald-400 font-black text-sm">3. الابتكار والتعلم المستمر</div>
                        <p class="text-slate-300 leading-relaxed">تنمية التفكير الناقد ومهارات الشغف بالمعرفة والتطور التقني.</p>
                    </div>
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 space-y-2">
                        <div class="text-emerald-400 font-black text-sm">4. الاحترام والانضباط</div>
                        <p class="text-slate-300 leading-relaxed">ترسيخ السلوك الإيجابي والمسؤولية والأخلاق الفاضلة لدى الطلاب.</p>
                    </div>
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800 space-y-2">
                        <div class="text-emerald-400 font-black text-sm">5. العمل الجماعي والشراكة</div>
                        <p class="text-slate-300 leading-relaxed">التكامل بين إدارة المدرسة والمعلمين وأسر الطلاب والمجتمع المحلي.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- TAB 3: EXTERNAL EVALUATION RESULTS -->
        <section id="tab-evaluation" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-2">
                <h2 class="text-xl font-black text-white flex items-center gap-2"><i class="fa-solid fa-chart-simple text-brand-gold"></i> تحليل نتائج التقويم الخارجي والاعتماد المدرسي</h2>
                <p class="text-xs text-slate-400">مؤشرات أداء مدرسة بشر بن عاصم ومدرسة تحفيظ القرآن الكريم برابغ من هيئة تقويم التعليم والتدريب (ETEC)</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                    <h3 class="font-black text-base text-teal-400 border-b border-slate-800 pb-3 flex items-center justify-between">
                        <span>مدرسة تحفيظ القرآن الكريم برابغ (32375)</span>
                        <span class="text-xs bg-teal-950 text-teal-300 px-3 py-1 rounded-full border border-teal-800">الأداء العام: 80% (التقدم)</span>
                    </h3>
                    <div class="space-y-3 text-xs">
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">الإدارة المدرسية</span><span class="font-black text-emerald-400">88.25% (التقدم)</span></div>
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">نواتج التعلم</span><span class="font-black text-emerald-400">81.50% (التقدم)</span></div>
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">التعليم والتعلم</span><span class="font-black text-brand-gold">74.00% (الانطلاق)</span></div>
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">البيئة المدرسية</span><span class="font-black text-emerald-400">81.25% (التقدم)</span></div>
                    </div>
                </div>

                <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                    <h3 class="font-black text-base text-emerald-400 border-b border-slate-800 pb-3 flex items-center justify-between">
                        <span>مدرسة بشر بن عاصم الابتدائية (133522)</span>
                        <span class="text-xs bg-emerald-950 text-emerald-300 px-3 py-1 rounded-full border border-emerald-800">الأداء العام: 81% (التقدم)</span>
                    </h3>
                    <div class="space-y-3 text-xs">
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">الإدارة المدرسية</span><span class="font-black text-emerald-400">89.50% (التقدم)</span></div>
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">نواتج التعلم</span><span class="font-black text-emerald-400">81.50% (التقدم)</span></div>
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">التعليم والتعلم</span><span class="font-black text-emerald-400">75.75% (التقدم)</span></div>
                        <div class="flex justify-between items-center bg-slate-900 p-3 rounded-xl border border-slate-800"><span class="font-bold text-slate-300">البيئة المدرسية</span><span class="font-black text-emerald-400">82.00% (التقدم)</span></div>
                    </div>
                </div>
            </div>

            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-3">
                <h3 class="font-black text-lg text-white text-rose-400"><i class="fa-solid fa-triangle-exclamation"></i> القضايا والأولويات التطويرية للتدخل السريع</h3>
                <ul class="text-xs space-y-2 text-slate-300 list-disc list-inside leading-relaxed">
                    <li><strong class="text-white">تنمية مهارات التفكير العليا (2-1-1-7):</strong> سجلت أدنى مؤشر بنسبة (51% إلى 54%).</li>
                    <li><strong class="text-white">المهارات الرقمية لدى المتعلمين (2-1-1-9):</strong> تقع في النطاق الحرِج بمتوسط (63% - 65%).</li>
                    <li><strong class="text-white">تنويع استراتيجيات التدريس والتقويم:</strong> تراوحت بين (67% - 73%) مما يستدعي التفعيل الميداني لمجتمعات التعلم والزيارات.</li>
                    <li><strong class="text-white">الشراكة المجتمعية برابغ وبرامج الموهوبين:</strong> تقع في نطاق التهيئة (65% - 69%) وتتطلب عقود شراكة وسفراء للموهبة.</li>
                </ul>
            </div>
        </section>

        <!-- TAB 4: SWOT ANALYSIS -->
        <section id="tab-swot" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-2">
                <h2 class="text-xl font-black text-white flex items-center gap-2"><i class="fa-solid fa-magnifying-glass-chart text-blue-400"></i> تشخيص الواقع الميداني (تحليل SWOT الشامل)</h2>
                <p class="text-xs text-slate-400">قراءة دقيقة للعوامل الداخلية والخارجية المؤثرة في البيئة التعليمية</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-xs">
                <div class="bg-emerald-950/20 border border-emerald-800/50 p-5 rounded-2xl space-y-3">
                    <h3 class="font-black text-emerald-400 text-sm flex items-center gap-2"><i class="fa-solid fa-circle-check"></i> نقاط القوة (Strengths)</h3>
                    <ul class="space-y-1.5 text-slate-300 list-disc list-inside">
                        <li>قيادة وتخطيط متميز وحوكمة احترافية وخطة مكتملة (100%).</li>
                        <li>تعزيز فعال للقيم الإسلامية والوطنية والسلوك الإيجابي (96%-99%).</li>
                        <li>بيئة آمنة وتفوق في الأمن والسلامة والنظافة (>90%).</li>
                        <li>كادر إداري وتعليمي مكتمل ومستقر.</li>
                    </ul>
                </div>

                <div class="bg-blue-950/20 border border-blue-800/50 p-5 rounded-2xl space-y-3">
                    <h3 class="font-black text-blue-400 text-sm flex items-center gap-2"><i class="fa-solid fa-lightbulb"></i> الفرص (Opportunities)</h3>
                    <ul class="space-y-1.5 text-slate-300 list-disc list-inside">
                        <li>رؤية المملكة 2030 وبرنامج تنمية القدرات البشرية.</li>
                        <li>مساندة إشرافية ومؤسسية مستمرة من مكتب تعليم رابغ بجدة.</li>
                        <li>توفر المنصات الرقمية الذكية (مدرستي، نور، إتقان).</li>
                        <li>شراكات واعدة مع القطاع الصحي والخدمي بمحافظة رابغ.</li>
                    </ul>
                </div>

                <div class="bg-amber-950/20 border border-amber-800/50 p-5 rounded-2xl space-y-3">
                    <h3 class="font-black text-amber-400 text-sm flex items-center gap-2"><i class="fa-solid fa-circle-exclamation"></i> نقاط الضعف (Weaknesses)</h3>
                    <ul class="space-y-1.5 text-slate-300 list-disc list-inside">
                        <li>ضعف مهارات التفكير العليا والحاجة لتجاوز مستوى الحفظ (51%-54%).</li>
                        <li>قصور في تفعيل المهارات التقنية والتعلم الرقمي (63%-65%).</li>
                        <li>تفاوت التحصيل وتنوع استراتيجيات التدريس وتقويم التعلم.</li>
                    </ul>
                </div>

                <div class="bg-rose-950/20 border border-rose-800/50 p-5 rounded-2xl space-y-3">
                    <h3 class="font-black text-rose-400 text-sm flex items-center gap-2"><i class="fa-solid fa-shield-cat"></i> التهديدات (Threats)</h3>
                    <ul class="space-y-1.5 text-slate-300 list-disc list-inside">
                        <li>تفاوت المتابعة الأسرية وانخراط بعض الأسر.</li>
                        <li>المشتتات الرقمية الخارجية والاستخدام غير الموجه للألعاب.</li>
                        <li>ضعف مهارات التعلم الذاتي والبحث لدى بعض الطلاب.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- TAB 5: RISK MANAGEMENT -->
        <section id="tab-risk" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-2">
                <h2 class="text-xl font-black text-white flex items-center gap-2"><i class="fa-solid fa-shield-halved text-rose-400"></i> سجل إدارة المخاطر وخطة الاستجابة الاستباقية</h2>
                <p class="text-xs text-slate-400">منظومة استباقية لحصر وتصنيف المخاطر الميدانية والوقاية منها لاستمرارية التعلم</p>
            </div>

            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border overflow-x-auto">
                <table class="w-full text-xs text-right border-collapse">
                    <thead>
                        <tr class="bg-slate-800 text-slate-300 font-bold border-b border-slate-700">
                            <th class="p-3">م</th>
                            <th class="p-3">الخطر المحتمل</th>
                            <th class="p-3">مستوى الخطورة</th>
                            <th class="p-3">الإجراء الوقائي والاستجابة الاستباقية</th>
                            <th class="p-3">الدورية</th>
                            <th class="p-3">المسؤول المباشر</th>
                            <th class="p-3">الشاهد وأداة التوثيق</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-800 text-slate-300">
                        <tr>
                            <td class="p-3 font-bold text-slate-500">1</td>
                            <td class="p-3 font-bold text-white">تعثر التحصيل وانخفاض أداء نافس</td>
                            <td class="p-3"><span class="bg-rose-950 text-rose-400 px-2 py-1 rounded font-bold border border-rose-800">مرتفع</span></td>
                            <td class="p-3 text-slate-300">تطبيق اختبارات تشخيصية مبكرة، حصص دعم، ونماذج محاكاة أسبوعية.</td>
                            <td class="p-3">شهري</td>
                            <td class="p-3 font-bold text-emerald-400">أ. حاتم أبو خضير</td>
                            <td class="p-3 text-slate-400">نتائج الاختبارات وكراسات نافس</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-bold text-slate-500">2</td>
                            <td class="p-3 font-bold text-white">ارتفاع الغياب أو التأخر الصباحي</td>
                            <td class="p-3"><span class="bg-rose-950 text-rose-400 px-2 py-1 rounded font-bold border border-rose-800">مرتفع</span></td>
                            <td class="p-3 text-slate-300">تفعيل برنامج "بوابة الحضور المبكر"، إشعار آلي فوري للأسر، وتطبيق السلوك.</td>
                            <td class="p-3">أسبوعي</td>
                            <td class="p-3 font-bold text-emerald-400">أ. عيد المحمدي</td>
                            <td class="p-3 text-slate-400">تقارير نظام نور وسجل الحضور</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-bold text-slate-500">3</td>
                            <td class="p-3 font-bold text-white">ضعف التواصل والمتابعة المنزلية</td>
                            <td class="p-3"><span class="bg-amber-950 text-amber-400 px-2 py-1 rounded font-bold border border-amber-800">متوسط</span></td>
                            <td class="p-3 text-slate-300">تنويع الرسائل الرقمية (SMS)، استبيانات الرضا، ولقاءات أولياء الأمور.</td>
                            <td class="p-3">فصلي</td>
                            <td class="p-3 font-bold text-emerald-400">أ. أحمد الغانمي</td>
                            <td class="p-3 text-slate-400">سجل التواصل الرقمي ومحاضر الجمعية</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-bold text-slate-500">4</td>
                            <td class="p-3 font-bold text-white">طوارئ الصيانة ووسائل السلامة</td>
                            <td class="p-3"><span class="bg-amber-950 text-amber-400 px-2 py-1 rounded font-bold border border-amber-800">متوسط</span></td>
                            <td class="p-3 text-slate-300">التفتيش الفوري لأجهزة السلامة، رفع بلاغات صيانة عاجلة برابغ.</td>
                            <td class="p-3">أسبوعي</td>
                            <td class="p-3 font-bold text-emerald-400">أ. وجدي الكريثي</td>
                            <td class="p-3 text-slate-400">سجل البلاغات واستمارة السلامة</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-bold text-slate-500">5</td>
                            <td class="p-3 font-bold text-white">ضعف توثيق وأرشفة شواهد البرامج الـ 24</td>
                            <td class="p-3"><span class="bg-amber-950 text-amber-400 px-2 py-1 rounded font-bold border border-amber-800">متوسط</span></td>
                            <td class="p-3 text-slate-300">اعتماد الأرشفة السحابية الفورية للجان وتثبيت البطاقات عبر الوكلاء.</td>
                            <td class="p-3">شهري</td>
                            <td class="p-3 font-bold text-emerald-400">لجنة التميز المدرسية</td>
                            <td class="p-3 text-slate-400">السجل السحابي الموحد وبطاقات التثبيت</td>
                        </tr>
                        <tr>
                            <td class="p-3 font-bold text-slate-500">6</td>
                            <td class="p-3 font-bold text-white">محدودية التجهيزات أو الموارد المالية</td>
                            <td class="p-3"><span class="bg-amber-950 text-amber-400 px-2 py-1 rounded font-bold border border-amber-800">متوسط</span></td>
                            <td class="p-3 text-slate-300">ترتيب أولويات الإنفاق واستثمار الشراكات المجتمعية برابغ.</td>
                            <td class="p-3">فصلي</td>
                            <td class="p-3 font-bold text-emerald-400">أ. خالد السيد</td>
                            <td class="p-3 text-slate-400">عقود الشراكة ونماذج الترشيد</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- TAB 6: FULL PROGRAM CARDS -->
        <section id="tab-cards" class="tab-panel hidden space-y-6">
            <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4 bg-brand-card p-5 rounded-2xl border border-brand-border">
                <div>
                    <h2 class="font-black text-xl text-white flex items-center gap-2"><i class="fa-solid fa-id-card text-emerald-400"></i> الدليل التفصيلي لبطاقات البرامج التشغيلية</h2>
                    <p class="text-xs text-slate-400 mt-1">عرض الأهداف، المبادرات، آلية التنفيذ، التواريخ، والمسؤولية الكاملة</p>
                </div>
                <div class="flex gap-2">
                    <button onclick="openProgramModal()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-4 py-2 rounded-xl text-xs font-bold transition flex items-center gap-2">+ إضافة برنامج جديد</button>
                    <select id="cardDomainFilter" onchange="renderProgramCards()" class="bg-slate-900 border border-slate-700 rounded-xl px-3 py-2 text-xs font-bold text-slate-200">
                        <option value="all">جميع البرامج</option>
                        <option value="1">1. مجال الإدارة المدرسية</option>
                        <option value="2">2. مجال التعليم والتعلم</option>
                        <option value="3">3. مجال نواتج التعلم</option>
                        <option value="4">4. مجال البيئة المدرسية</option>
                    </select>
                </div>
            </div>

            <div id="fullCardsGrid" class="space-y-6"></div>
        </section>

        <!-- TAB 7: 4 COMMITTEES -->
        <section id="tab-committees" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <div class="flex justify-between items-center border-b border-slate-800 pb-4">
                    <div>
                        <h3 class="font-black text-lg text-white"><i class="fa-solid fa-users-gear text-brand-gold"></i> سجل اللجان المدرسية الأربعة (تعديل، إضافة، وحذف)</h3>
                        <p class="text-xs text-slate-400 mt-1">يمكنك تعديل أسمائها وأعضائها وتكليفاتهم بحرية وسيتم حفظ التعديلات سحابياً</p>
                    </div>
                    <button onclick="addNewCommittee()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-4 py-2 rounded-xl text-xs font-bold">+ إضافة لجنة جديدة</button>
                </div>
                <div id="committeesContainer" class="space-y-6"></div>
            </div>
        </section>

        <!-- TAB 8: DAILY QUICK LINKS -->
        <section id="tab-links" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-2">
                <h2 class="text-xl font-black text-white flex items-center gap-2"><i class="fa-solid fa-globe text-emerald-400"></i> بوابات الدخول السريع للمواقع اليومية</h2>
                <p class="text-xs text-slate-400">روابط المنصات والأنظمة المعتمدة التي تحتاجه للدخول المباشر يومياً</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="bg-brand-card p-6 rounded-2xl border border-brand-border hover:border-emerald-500 transition shadow-xl space-y-4 flex flex-col justify-between">
                    <div class="space-y-3">
                        <div class="w-12 h-12 rounded-xl bg-emerald-500/10 text-emerald-400 flex items-center justify-center font-black text-xl"><i class="fa-solid fa-gauge"></i></div>
                        <h3 class="font-black text-lg text-white">منصة إتقان المدرسي</h3>
                        <p class="text-xs text-slate-400 leading-relaxed">لوحة متابعة النظام والتقارير الإدارية للطلاب والكادر التعليمي.</p>
                    </div>
                    <a href="https://www.smartble.net/pro/pro_dashboard/" target="_blank" class="w-full bg-emerald-600 hover:bg-emerald-500 text-white font-bold py-3 rounded-xl text-xs text-center transition">دخول المنصة <i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>

                <div class="bg-brand-card p-6 rounded-2xl border border-brand-border hover:border-teal-500 transition shadow-xl space-y-4 flex flex-col justify-between">
                    <div class="space-y-3">
                        <div class="w-12 h-12 rounded-xl bg-teal-500/10 text-teal-400 flex items-center justify-center font-black text-xl"><i class="fa-solid fa-school"></i></div>
                        <h3 class="font-black text-lg text-white">نظام نور الوزاري</h3>
                        <p class="text-xs text-slate-400 leading-relaxed">رصد الحضور والغياب، السلوك والمواظبة، والاختبارات المدرسية الرسمية.</p>
                    </div>
                    <a href="https://noor.moe.gov.sa/Noor/Login.aspx?ref=noor" target="_blank" class="w-full bg-teal-600 hover:bg-teal-500 text-white font-bold py-3 rounded-xl text-xs text-center transition">دخول نظام نور <i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>

                <div class="bg-brand-card p-6 rounded-2xl border border-brand-border hover:border-blue-500 transition shadow-xl space-y-4 flex flex-col justify-between">
                    <div class="space-y-3">
                        <div class="w-12 h-12 rounded-xl bg-blue-500/10 text-blue-400 flex items-center justify-center font-black text-xl"><i class="fa-solid fa-laptop-code"></i></div>
                        <h3 class="font-black text-lg text-white">منصة مدرستي</h3>
                        <p class="text-xs text-slate-400 leading-relaxed">متابعة الجداول الدراسية، الدروس التفاعلية، والتقارير الرقمية.</p>
                    </div>
                    <a href="https://schools.madrasati.sa/" target="_blank" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-bold py-3 rounded-xl text-xs text-center transition">دخول منصة مدرستي <i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                </div>
            </div>
        </section>

        <!-- TAB 9: EXTERNAL FILES MANAGEMENT -->
        <section id="tab-files" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4">
                    <div>
                        <h2 class="text-xl font-black text-white flex items-center gap-2"><i class="fa-solid fa-folder-open text-amber-400"></i> مركز رفع وإدارة الملفات والمرفقات الخارجية</h2>
                        <p class="text-xs text-slate-400 mt-1">إضافة، أرشفة، وتنزيل التقارير والسجلات الرسمية للمنظومة سحابياً</p>
                    </div>
                    <label class="bg-amber-600 hover:bg-amber-500 text-white px-4 py-2.5 rounded-xl text-xs font-bold transition flex items-center gap-2 cursor-pointer shadow-lg">
                        <i class="fa-solid fa-cloud-arrow-up"></i> رفع ملف خارجي جديد
                        <input type="file" id="externalFileInput" onchange="uploadExternalFile(event)" class="hidden">
                    </label>
                </div>
                <div class="flex flex-col md:flex-row gap-3 border-t border-slate-800 pt-4">
                    <div class="flex flex-1 gap-2">
                        <input type="text" id="newFolderName" placeholder="اسم المجلد الجديد" class="flex-1 min-w-0 bg-slate-900 border border-slate-700 rounded-xl px-3 py-2.5 text-xs text-white">
                        <button onclick="createFileFolder()" class="bg-blue-600 hover:bg-blue-500 text-white px-4 py-2.5 rounded-xl text-xs font-bold flex items-center gap-2 whitespace-nowrap">
                            <i class="fa-solid fa-folder-plus"></i> إضافة مجلد
                        </button>
                    </div>
                    <select id="fileFolderFilter" onchange="renderExternalFiles()" class="bg-slate-900 border border-slate-700 rounded-xl px-3 py-2.5 text-xs text-slate-200 md:w-56">
                        <option value="all">عرض جميع المجلدات</option>
                    </select>
                    <select id="fileUploadFolder" class="bg-slate-900 border border-slate-700 rounded-xl px-3 py-2.5 text-xs text-slate-200 md:w-56">
                        <option value="غير مصنف">رفع إلى: غير مصنف</option>
                    </select>
                </div>
            </div>

            <div id="filesContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4"></div>
        </section>

        <!-- TAB 10: SCHOOL & STAFF DATA (صفحة بيانات وإحصائيات المدرسة) -->
        <section id="tab-data" class="tab-panel hidden space-y-6">
            <div class="bg-brand-card p-6 rounded-2xl border border-brand-border space-y-4">
                <div class="flex justify-between items-center border-b border-slate-800 pb-4">
                    <div>
                        <h2 class="text-xl font-black text-white flex items-center gap-2">
                            <i class="fa-solid fa-school text-emerald-400"></i> بيانات وإحصائيات المدرسة والكادر الإداري والتعليمي
                        </h2>
                        <p class="text-xs text-slate-400 mt-1">تصفح البيانات الإحصائية التفصيلية وسجلات الكادر مع إمكانية التعديل والحفظ المباشر</p>
                    </div>
                </div>

                <!-- SUB TABS NAVIGATION -->
                <div class="flex border-b border-slate-800 text-xs font-bold gap-2 overflow-x-auto pb-2">
                    <button onclick="switchSubTab('school-stats')" id="subtab-btn-school-stats" class="subtab-btn active px-4 py-2.5 rounded-xl bg-emerald-600 text-white transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-chart-line"></i> 1. بيانات المدرسة والفصول
                    </button>
                    <button onclick="switchSubTab('admin-staff')" id="subtab-btn-admin-staff" class="subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-user-tie text-teal-400"></i> 2. الكادر الإداري
                    </button>
                    <button onclick="switchSubTab('teachers-staff')" id="subtab-btn-teachers-staff" class="subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-chalkboard-user text-emerald-400"></i> 3. الكادر التعليمي
                    </button>
                    <button onclick="switchSubTab('assistants-staff')" id="subtab-btn-assistants-staff" class="subtab-btn px-4 py-2.5 rounded-xl bg-slate-800 text-slate-300 hover:bg-slate-700 transition flex items-center gap-2 flex-shrink-0">
                        <i class="fa-solid fa-users-gear text-brand-gold"></i> 4. المساعدين الإداريين
                    </button>
                </div>

                <!-- SUB TAB 1: EDITABLE SCHOOL & CLASSES STATS -->
                <div id="subtab-school-stats" class="subtab-panel space-y-6 pt-2">
                    <!-- School 1: Bishr Bin Asim -->
                    <div class="bg-slate-900 p-5 rounded-2xl border border-slate-800 space-y-4">
                        <div class="flex justify-between items-center border-b border-slate-800 pb-3">
                            <div>
                                <h4 class="font-black text-emerald-400 text-base">مدرسة بشر بن عاصم الابتدائية (الرقم الوزاري: 133522)</h4>
                                <p class="text-xs text-slate-400 mt-0.5">انقر على الأرقام للتعديل المباشر، وسيتم احتساب المجاميع آلياً</p>
                            </div>
                            <button onclick="addClassRow('eid_school1_classes', renderSchool1Stats)" class="bg-slate-800 hover:bg-slate-700 text-emerald-400 px-3 py-1.5 rounded-xl text-xs font-bold border border-slate-700">+ إضافة صف جديد</button>
                        </div>

                        <div class="overflow-x-auto">
                            <table class="w-full text-xs text-right border-collapse">
                                <thead>
                                    <tr class="bg-slate-800/80 text-slate-300 font-bold border-b border-slate-700">
                                        <th class="p-2.5">الصف الدراسي</th>
                                        <th class="p-2.5 text-center">عدد الفصول</th>
                                        <th class="p-2.5 text-center">عدد الطلاب</th>
                                        <th class="p-2.5 text-center">حذف</th>
                                    </tr>
                                </thead>
                                <tbody id="school1TableBody" class="divide-y divide-slate-800/80 text-slate-200"></tbody>
                                <tfoot>
                                    <tr class="bg-emerald-950/40 text-emerald-300 font-black border-t border-emerald-800">
                                        <td class="p-3 text-sm">المجموع الإجمالي</td>
                                        <td class="p-3 text-center text-sm" id="school1TotalClasses">0 فصل</td>
                                        <td class="p-3 text-center text-sm" id="school1TotalStudents">0 طالب</td>
                                        <td></td>
                                    </tr>
                                </tfoot>
                            </table>
                        </div>
                    </div>

                    <!-- School 2: Tahfeez Quran -->
                    <div class="bg-slate-900 p-5 rounded-2xl border border-slate-800 space-y-4">
                        <div class="flex justify-between items-center border-b border-slate-800 pb-3">
                            <div>
                                <h4 class="font-black text-teal-400 text-base">مدرسة تحفيظ القرآن الكريم برابغ (الرقم الوزاري: 32375)</h4>
                                <p class="text-xs text-slate-400 mt-0.5">انقر على الأرقام للتعديل المباشر، وسيتم احتساب المجاميع آلياً</p>
                            </div>
                            <button onclick="addClassRow('eid_school2_classes', renderSchool2Stats)" class="bg-slate-800 hover:bg-slate-700 text-teal-400 px-3 py-1.5 rounded-xl text-xs font-bold border border-slate-700">+ إضافة صف جديد</button>
                        </div>

                        <div class="overflow-x-auto">
                            <table class="w-full text-xs text-right border-collapse">
                                <thead>
                                    <tr class="bg-slate-800/80 text-slate-300 font-bold border-b border-slate-700">
                                        <th class="p-2.5">الصف الدراسي</th>
                                        <th class="p-2.5 text-center">عدد الفصول</th>
                                        <th class="p-2.5 text-center">عدد الطلاب</th>
                                        <th class="p-2.5 text-center">حذف</th>
                                    </tr>
                                </thead>
                                <tbody id="school2TableBody" class="divide-y divide-slate-800/80 text-slate-200"></tbody>
                                <tfoot>
                                    <tr class="bg-teal-950/40 text-teal-300 font-black border-t border-teal-800">
                                        <td class="p-3 text-sm">المجموع الإجمالي</td>
                                        <td class="p-3 text-center text-sm" id="school2TotalClasses">0 فصل</td>
                                        <td class="p-3 text-center text-sm" id="school2TotalStudents">0 طالب</td>
                                        <td></td>
                                    </tr>
                                </tfoot>
                            </table>
                        </div>
                    </div>

                </div>

                <!-- SUB TAB 2: ADMINISTRATIVE STAFF -->
                <div id="subtab-admin-staff" class="subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center">
                        <h3 class="font-black text-sm text-teal-400"><i class="fa-solid fa-user-tie"></i> سجل الكادر الإداري بالمدرسة</h3>
                        <button onclick="addAdminRow()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-3 py-1.5 rounded-xl text-xs font-bold">+ إضافة إداري جديد</button>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="w-full text-xs text-right border-collapse">
                            <thead>
                                <tr class="bg-slate-800 text-slate-300 font-bold border-b border-slate-700">
                                    <th class="p-3">م</th>
                                    <th class="p-3">الاسم الرباعي</th>
                                    <th class="p-3">المسمى الوظيفي</th>
                                    <th class="p-3">التخصص</th>
                                    <th class="p-3">الحصول على الرخصة المهنية</th>
                                    <th class="p-3 text-center">حذف</th>
                                </tr>
                            </thead>
                            <tbody id="adminTableBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                        </table>
                    </div>
                </div>

                <!-- SUB TAB 3: TEACHERS STAFF -->
                <div id="subtab-teachers-staff" class="subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center">
                        <h3 class="font-black text-sm text-emerald-400"><i class="fa-solid fa-chalkboard-user"></i> سجل هيئة التدريس (الكادر التعليمي)</h3>
                        <button onclick="addTeacherRow()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-3 py-1.5 rounded-xl text-xs font-bold">+ إضافة معلم جديد</button>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="w-full text-xs text-right border-collapse">
                            <thead>
                                <tr class="bg-slate-800 text-slate-300 font-bold border-b border-slate-700">
                                    <th class="p-3">م</th>
                                    <th class="p-3">الاسم الرباعي</th>
                                    <th class="p-3">المسمى الوظيفي</th>
                                    <th class="p-3">التخصص</th>
                                    <th class="p-3">الحصول على الرخصة المهنية</th>
                                    <th class="p-3 text-center">حذف</th>
                                </tr>
                            </thead>
                            <tbody id="teachersTableBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                        </table>
                    </div>
                </div>

                <!-- SUB TAB 4: ASSISTANTS STAFF -->
                <div id="subtab-assistants-staff" class="subtab-panel hidden space-y-4 pt-2">
                    <div class="flex justify-between items-center">
                        <h3 class="font-black text-sm text-brand-gold"><i class="fa-solid fa-users-gear"></i> سجل المساعدين الإداريين والخدمات المساندة</h3>
                        <button onclick="addAssistantRow()" class="bg-emerald-600 hover:bg-emerald-500 text-white px-3 py-1.5 rounded-xl text-xs font-bold">+ إضافة مساعد إداري</button>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="w-full text-xs text-right border-collapse">
                            <thead>
                                <tr class="bg-slate-800 text-slate-300 font-bold border-b border-slate-700">
                                    <th class="p-3">م</th>
                                    <th class="p-3">الاسم الرباعي</th>
                                    <th class="p-3">المسمى الوظيفي</th>
                                    <th class="p-3">التخصص / المجال</th>
                                    <th class="p-3">الحصول على الرخصة المهنية</th>
                                    <th class="p-3 text-center">حذف</th>
                                </tr>
                            </thead>
                            <tbody id="assistantsTableBody" class="divide-y divide-slate-800 text-slate-300"></tbody>
                        </table>
                    </div>
                </div>

            </div>
        </section>

    </main>

    <!-- MODAL FOR PROGRAM CARD -->
    <div id="programModal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-sm z-50 flex items-center justify-center hidden p-4 no-print">
        <div class="bg-brand-card border border-brand-border rounded-3xl max-w-2xl w-full p-6 shadow-2xl space-y-4 max-h-[90vh] overflow-y-auto custom-scrollbar">
            <h3 id="modalTitle" class="text-lg font-black text-white border-b border-slate-800 pb-3">إضافة / تعديل بطاقة برنامج تشغيلي</h3>
            
            <input type="hidden" id="progModalId">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-3 text-xs font-bold">
                <div>
                    <label class="block mb-1 text-slate-400">اسم البرنامج</label>
                    <input type="text" id="progModalName" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">المجال (ETEC)</label>
                    <select id="progModalDomain" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                        <option value="1">1. المجال الأول: الإدارة المدرسية</option>
                        <option value="2">2. المجال الثاني: التعليم والتعلم</option>
                        <option value="3">3. المجال الثالث: نواتج التعلم</option>
                        <option value="4">4. المجال الرابع: البيئة المدرسية</option>
                    </select>
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">المعيار المرتبط (ETEC)</label>
                    <input type="text" id="progModalStandard" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white" placeholder="مثال: التخطيط (1-1-1)">
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">المبادرة المرتبطة</label>
                    <input type="text" id="progModalInitiative" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">المسؤول عن التنفيذ</label>
                    <input type="text" id="progModalLead" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">الميزانية المرصودة</label>
                    <input type="text" id="progModalCost" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                </div>
                <div class="md:col-span-2">
                    <label class="block mb-1 text-slate-400">الهدف التشغيلي</label>
                    <textarea id="progModalGoal" rows="2" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white"></textarea>
                </div>
                <div class="md:col-span-2">
                    <label class="block mb-1 text-slate-400">آلية وخطوات التنفيذ التفصيلية</label>
                    <textarea id="progModalSteps" rows="3" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white"></textarea>
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">تاريخ/زمن التنفيذ (الفصل الأول)</label>
                    <input type="text" id="progModalTerm1" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                </div>
                <div>
                    <label class="block mb-1 text-slate-400">تاريخ/زمن التنفيذ (الفصل الثاني)</label>
                    <input type="text" id="progModalTerm2" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-white">
                </div>
            </div>

            <div class="flex gap-3 pt-4 border-t border-slate-800 text-xs font-bold">
                <button onclick="saveProgramModal()" class="flex-1 bg-emerald-600 hover:bg-emerald-500 text-white py-3 rounded-xl transition">حفظ البطاقة</button>
                <button onclick="closeProgramModal()" class="px-5 bg-slate-800 text-slate-300 py-3 rounded-xl">إلغاء</button>
            </div>
        </div>
    </div>

    <!-- SCRIPT LOGIC -->
    <script>
        // MASTER PRE-FILLED CLASSES SCHEDULE DATA FROM EXCEL
        const masterClassesData = {
          "ع4-1": [
            {"day": "الأحد", "periods": ["المهارات الحياتية", "التربية البدنية", "الدراسات الإسلامية", "العلوم", "المهارات الرقمية", "اللغة العربية", "الرياضيات"]},
            {"day": "الاثنين", "periods": ["اللغة الإنجليزية", "التربية البدنية", "الرياضيات", "العلوم", "اللغة العربية", "الدراسات الإسلامية", ""]},
            {"day": "الثلاثاء", "periods": ["الرياضيات", "الدراسات الإسلامية", "الدراسات الإجتماعية", "اللغة العربية", "العلوم", "اللغة الإنجليزية", ""]},
            {"day": "الأربعاء", "periods": ["الرياضيات", "الدراسات الإسلامية", "العلوم", "الرياضيات", "اللغة العربية", "اللغة الإنجليزية", ""]},
            {"day": "الخميس", "periods": ["الدراسات الإجتماعية", "المهارات الرقمية", "اللغة العربية", "الرياضيات", "التربية الفنية", "الدراسات الإسلامية", ""]}
          ],
          "ع5-1": [
            {"day": "الأحد", "periods": ["الرياضيات", "المهارات الحياتية", "العلوم", "اللغة العربية", "الدراسات الإسلامية", "التربية البدنية", "المهارات الرقمية"]},
            {"day": "الاثنين", "periods": ["الدراسات الإسلامية", "الرياضيات", "اللغة العربية", "العلوم", "الدراسات الإجتماعية", "التربية الفنية", ""]},
            {"day": "الثلاثاء", "periods": ["العلوم", "المهارات الرقمية", "اللغة الإنجليزية", "الرياضيات", "الدراسات الإسلامية", "اللغة العربية", ""]},
            {"day": "الأربعاء", "periods": ["اللغة العربية", "العلوم", "اللغة الإنجليزية", "الدراسات الإسلامية", "التربية البدنية", "الرياضيات", ""]},
            {"day": "الخميس", "periods": ["اللغة العربية", "الرياضيات", "الدراسات الإسلامية", "اللغة الإنجليزية", "الدراسات الإجتماعية", "الدراسات الإسلامية", ""]}
          ],
          "ع5-2": [
            {"day": "الأحد", "periods": ["العلوم", "الدراسات الإسلامية", "الرياضيات", "المهارات الحياتية", "التربية البدنية", "المهارات الرقمية", "اللغة العربية"]},
            {"day": "الاثنين", "periods": ["الرياضيات", "اللغة العربية", "العلوم", "الدراسات الإسلامية", "التربية الفنية", "الدراسات الإجتماعية", ""]},
            {"day": "الثلاثاء", "periods": ["المهارات الرقمية", "العلوم", "الرياضيات", "اللغة الإنجليزية", "اللغة العربية", "الدراسات الإسلامية", ""]},
            {"day": "الأربعاء", "periods": ["العلوم", "اللغة العربية", "الدراسات الإسلامية", "التربية البدنية", "الرياضيات", "اللغة الإنجليزية", ""]},
            {"day": "الخميس", "periods": ["الرياضيات", "اللغة العربية", "اللغة الإنجليزية", "الدراسات الإسلامية", "الدراسات الإسلامية", "الدراسات الإجتماعية", ""]}
          ],
          "ع6-1": [
            {"day": "الأحد", "periods": ["الدراسات الإسلامية", "الرياضيات", "اللغة العربية", "المهارات الحياتية", "العلوم", "المهارات الرقمية", "التربية البدنية"]},
            {"day": "الاثنين", "periods": ["اللغة العربية", "العلوم", "الدراسات الإسلامية", "الرياضيات", "التربية البدنية", "التربية الفنية", ""]},
            {"day": "الثلاثاء", "periods": ["الدراسات الإسلامية", "المهارات الحياتية", "العلوم", "الدراسات الإجتماعية", "اللغة الإنجليزية", "الرياضيات", "اللغة العربية"]},
            {"day": "الأربعاء", "periods": ["الدراسات الإسلامية", "الرياضيات", "المهارات الرقمية", "اللغة العربية", "اللغة الإنجليزية", "العلوم", ""]},
            {"day": "الخميس", "periods": ["الرياضيات", "الدراسات الإسلامية", "اللغة العربية", "اللغة الإنجليزية", "الدراسات الإسلامية", "الدراسات الإجتماعية", ""]}
          ],
          "ت3-1": [
            {"day": "الأحد", "periods": ["ت3-1 قرآن وإسلامية", "ت3-1 قرآن وإسلامية", "ت3-1 لغتي", "ت3-1 رياضيات", "ت3-1 بدنية", "ت3-1 إنجليزية", ""]},
            {"day": "الاثنين", "periods": ["ت3-1 قرآن وإسلامية", "ت3-1 لغتي", "ت3-1 رياضيات", "ت3-1 علوم", "ت3-1 تجويد", "ت3-1 إنجليزية", ""]},
            {"day": "الثلاثاء", "periods": ["ت3-1 قرآن وإسلامية", "ت3-1 لغتي", "ت3-1 رياضيات", "ت3-1 علوم", "ت3-1 بدنية", "ت3-1 حياتية", ""]},
            {"day": "الأربعاء", "periods": ["ت3-1 قرآن وإسلامية", "ت3-1 لغتي", "ت3-1 رياضيات", "ت3-1 قرآن وإسلامية", "ت3-1 تجويد", "ت3-1 فنية", ""]},
            {"day": "الخميس", "periods": ["ت3-1 قرآن وإسلامية", "ت3-1 لغتي", "ت3-1 رياضيات", "ت3-1 علوم", "ت3-1 قرآن وإسلامية", "ت3-1 رقمية", ""]}
          ],
          "ت3-2": [
            {"day": "الأحد", "periods": ["ت3-2 لغتي", "ت3-2 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "ت3-2 بدنية", "ت3-2 رياضيات", "ت3-2 إنجليزية", ""]},
            {"day": "الاثنين", "periods": ["ت3-2 لغتي", "ت3-2 قرآن وإسلامية", "ت3-2 علوم", "ت3-2 رياضيات", "ت3-2 إنجليزية", "ت3-2 تجويد", ""]},
            {"day": "الثلاثاء", "periods": ["ت3-2 لغتي", "ت3-2 قرآن وإسلامية", "ت3-2 علوم", "ت3-2 رياضيات", "ت3-2 حياتية", "ت3-2 بدنية", ""]},
            {"day": "الأربعاء", "periods": ["ت3-2 لغتي", "ت3-2 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "ت3-2 رياضيات", "ت3-2 فنية", "ت3-2 تجويد", ""]},
            {"day": "الخميس", "periods": ["ت3-2 لغتي", "ت3-2 قرآن وإسلامية", "ت3-2 علوم", "ت3-2 رياضيات", "ت3-2 رقمية", "ت3-2 قرآن وإسلامية", ""]}
          ],
          "ت4-1": [
            {"day": "الأحد", "periods": ["ت4-1 لغتي", "ت4-1 رياضيات", "ت4-1 قرآن وإسلامية", "ت4-1 إنجليزية", "ت4-1 تجويد", "ت4-1 بدنية", "ت4-1 حياتية"]},
            {"day": "الاثنين", "periods": ["ت4-1 رياضيات", "ت4-1 قرآن وإسلامية", "ت4-1 لغتي", "ت4-1 تجويد", "ت4-1 علوم", "ت4-1 اجتماعيات", ""]},
            {"day": "الثلاثاء", "periods": ["ت4-1 لغتي", "ت4-1 علوم", "ت4-1 قرآن وإسلامية", "ت4-1 رياضيات", "ت4-1 رقمية", "ت4-1 بدنية", ""]},
            {"day": "الأربعاء", "periods": ["ت4-1 رياضيات", "ت4-1 علوم", "ت4-1 لغتي", "ت4-1 قرآن وإسلامية", "ت4-1 إنجليزية", "ت4-1 إنجليزية", ""]},
            {"day": "الخميس", "periods": ["ت4-1 لغتي", "ت4-1 قرآن وإسلامية", "ت4-1 رياضيات", "ت4-1 رقمية", "ت4-1 فنية", "ت4-1 اجتماعيات", ""]}
          ],
          "ت4-2": [
            {"day": "الأحد", "periods": ["ت4-2 رياضيات", "ت4-2 لغتي", "ت4-2 إنجليزية", "ت4-2 قرآن وإسلامية", "ت4-2 بدنية", "ت4-2 تجويد", "ت4-2 حياتية"]},
            {"day": "الاثنين", "periods": ["ت4-2 قرآن وإسلامية", "ت4-2 رياضيات", "ت4-2 تجويد", "ت4-2 لغتي", "ت4-2 اجتماعيات", "ت4-2 علوم", ""]},
            {"day": "الثلاثاء", "periods": ["ت4-2 علوم", "ت4-2 لغتي", "ت4-2 رياضيات", "ت4-2 قرآن وإسلامية", "ت4-2 بدنية", "ت4-2 رقمية", ""]},
            {"day": "الأربعاء", "periods": ["ت4-2 علوم", "ت4-2 رياضيات", "ت4-2 قرآن وإسلامية", "ت4-2 لغتي", "ت4-2 إنجليزية", "ت4-2 إنجليزية", ""]},
            {"day": "الخميس", "periods": ["ت4-2 قرآن وإسلامية", "ت4-2 لغتي", "ت4-2 رقمية", "ت4-2 رياضيات", "ت4-2 اجتماعيات", "ت4-2 فنية", ""]}
          ],
          "ت5-1": [
            {"day": "الأحد", "periods": ["ت5-1 قرآن وإسلامية", "ت5-1 رياضيات", "ت5-1 لغتي", "ت5-1 بدنية", "ت5-1 اجتماعيات", "ت5-1 علوم", "ت5-1 إنجليزية"]},
            {"day": "الاثنين", "periods": ["ت5-1 قرآن وإسلامية", "ت5-1 لغتي", "ت5-1 رياضيات", "ت5-1 تجويد", "ت5-1 علوم", "ت5-1 رقمية", ""]},
            {"day": "الثلاثاء", "periods": ["ت5-1 رياضيات", "ت5-1 قرآن وإسلامية", "ت5-1 إنجليزية", "ت5-1 لغتي", "ت5-1 تجويد", "ت5-1 بدنية", ""]},
            {"day": "الأربعاء", "periods": ["ت5-1 قرآن وإسلامية", "ت5-1 رياضيات", "ت5-1 علوم", "ت5-1 لغتي", "ت5-1 إنجليزية", "ت5-1 فنية", ""]},
            {"day": "الخميس", "periods": ["ت5-1 لغتي", "ت5-1 قرآن وإسلامية", "ت5-1 علوم", "ت5-1 رياضيات", "ت5-1 رقمية", "ت5-1 اجتماعيات", ""]}
          ],
          "ت5-2": [
            {"day": "الأحد", "periods": ["ت5-2 رياضيات", "ت5-2 قرآن وإسلامية", "ت5-2 بدنية", "ت5-2 لغتي", "ت5-2 علوم", "ت5-2 اجتماعيات", "ت5-2 إنجليزية"]},
            {"day": "الاثنين", "periods": ["ت5-2 لغتي", "ت5-2 قرآن وإسلامية", "ت5-2 تجويد", "ت5-2 رياضيات", "ت5-2 رقمية", "ت5-2 علوم", ""]},
            {"day": "الثلاثاء", "periods": ["ت5-2 قرآن وإسلامية", "ت5-2 رياضيات", "ت5-2 لغتي", "ت5-2 إنجليزية", "ت5-2 بدنية", "ت5-2 تجويد", ""]},
            {"day": "الأربعاء", "periods": ["ت5-2 رياضيات", "ت5-2 قرآن وإسلامية", "ت5-2 لغتي", "ت5-2 علوم", "ت5-2 فنية", "ت5-2 إنجليزية", ""]},
            {"day": "الخميس", "periods": ["ت5-2 قرآن وإسلامية", "ت5-2 لغتي", "ت5-2 رياضيات", "ت5-2 علوم", "ت5-2 اجتماعيات", "ت5-2 رقمية", ""]}
          ],
          "ت6-1": [
            {"day": "الأحد", "periods": ["ت6-1 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "ت6-1 رياضيات", "ت6-1 علوم", "ت6-1 قرآن وإسلامية", "ت6-1 إنجليزية", "ت6-1 الحياتية"]},
            {"day": "الاثنين", "periods": ["ت6-1 رياضيات", "ت6-1 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "منتظر 1", "ت6-1 لغتي", "ت6-1 بدنية", "ت6-1 التجويد"]},
            {"day": "الثلاثاء", "periods": ["ت6-1 لغتي", "ع6-1 الحياتية", "ت6-1 علوم", "ت6-1 قرآن وإسلامية", "ت6-1 بدنية", "ت6-1 رياضيات", "ت6-1 قرآن وإسلامية"]},
            {"day": "الأربعاء", "periods": ["ت6-1 لغتي", "ت6-1 علوم", "ت6-1 رقمية", "ت6-1 رياضيات", "ت6-1 قرآن وإسلامية", "ت6-1 اجتماعيات", "ت6-1 إنجليزية"]},
            {"day": "الخميس", "periods": ["ت6-1 إنجليزية", "ت6-1 رياضيات", "ت6-1 لغتي", "ت6-1 اجتماعيات", "منتظر 2", "ت6-1 قرآن وإسلامية", "ت6-1 رقمية"]}
          ],
          "ت6-2": [
            {"day": "الأحد", "periods": ["ت6-2 قرآن وإسلامية", "ت6-2 رياضيات", "ت6-2 علوم", "ت6-2 قرآن وإسلامية", "ت6-2 إنجليزية", "ت6-2 بدنية", "ت6-2 بدنية"]},
            {"day": "الاثنين", "periods": ["ت6-2 قرآن وإسلامية", "ت6-2 رياضيات", "ت6-2 لغتي", "ت6-2 تجويد", "ت6-2 قرآن وإسلامية", "ت6-2 علوم", "ت6-2 اجتماعيات"]},
            {"day": "الثلاثاء", "periods": ["ت6-2 رياضيات", "ت6-2 علوم", "ت6-2 قرآن وإسلامية", "ت6-2 لغتي", "ت6-2 إنجليزية", "ت6-2 قرآن وإسلامية", "ت6-2 اجتماعيات"]},
            {"day": "الأربعاء", "periods": ["ت6-2 رياضيات", "ت6-2 التجويد", "ت6-2 الحياتية", "ت6-2 قرآن وإسلامية", "ت6-2 لغتي", "ت6-2 إنجليزية", "ت6-2 رقمية"]},
            {"day": "الخميس", "periods": ["ت6-2 قرآن وإسلامية", "ت6-2 لغتي", "ت6-2 قرآن وإسلامية", "ت6-2 علوم", "ت6-2 رياضيات", "ت6-2 رقمية", "ت6-2 الفنية"]}
          ]
        };

        // MASTER PRE-FILLED TEACHERS SCHEDULE DATA FROM EXCEL
        const masterTeachersData = {
          "تركي بن مرشود بن مبخوت البلادي": [
            {"day": "الأحد", "periods": ["ت6-2 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "", "ت6-2 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "", "ت6-1 الحياتية"]},
            {"day": "الاثنين", "periods": ["", "ت6-1 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "منتظر 1", "ت6-2 قرآن وإسلامية", "", "ت6-1 التجويد"]},
            {"day": "الثلاثاء", "periods": ["", "ع6-1 الحياتية", "ت6-2 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "", "ت6-2 قرآن وإسلامية", "ت6-1 قرآن وإسلامية"]},
            {"day": "الأربعاء", "periods": ["", "ت6-2 التجويد", "ت6-2 الحياتية", "ت6-2 قرآن وإسلامية", "ت6-1 قرآن وإسلامية", "", ""]},
            {"day": "الخميس", "periods": ["ت6-2 قرآن وإسلامية", "", "ت6-2 قرآن وإسلامية", "", "منتظر 2", "ت6-1 قرآن وإسلامية", "ت6-2 الفنية"]}
          ],
          "ياسر بن عبيدالله بن راجي الكنيدري": [
            {"day": "الأحد", "periods": ["ت5-1 قرآن وإسلامية", "ت5-2 قرآن وإسلامية", "", "", "ت5-1 اجتماعيات", "", "ت5-2 اجتماعيات"]},
            {"day": "الاثنين", "periods": ["ت5-1 قرآن وإسلامية", "ت5-2 قرآن وإسلامية", "ت5-2 تجويد", "ت5-1 تجويد", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["ت5-2 قرآن وإسلامية", "ت5-1 قرآن وإسلامية", "", "", "ت5-1 تجويد", "", "ت5-2 تجويد"]},
            {"day": "الأربعاء", "periods": ["ت5-1 قرآن وإسلامية", "ت5-2 قرآن وإسلامية", "", "", "", "", ""]},
            {"day": "الخميس", "periods": ["ت5-2 قرآن وإسلامية", "ت5-1 قرآن وإسلامية", "", "", "ت5-2 اجتماعيات", "ت5-1 اجتماعيات", ""]}
          ],
          "يوسف مبرك بن حميد اليوبي": [
            {"day": "الأحد", "periods": ["ت3-1 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["ت3-1 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "", "", "ت3-1 تجويد", "ت3-2 تجويد", ""]},
            {"day": "الثلاثاء", "periods": ["ت3-1 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "", "", "", "", "ت3-1 حياتية"]},
            {"day": "الأربعاء", "periods": ["ت3-1 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "ت3-1 قرآن وإسلامية", "ت3-1 تجويد", "ت3-2 تجويد", ""]},
            {"day": "الخميس", "periods": ["ت3-1 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", "", "", "ت3-1 قرآن وإسلامية", "ت3-2 قرآن وإسلامية", ""]}
          ],
          "حمزه ناصر علي الحربي": [
            {"day": "الأحد", "periods": ["ت4-1 لغتي", "ت4-2 لغتي", "ت4-1 قرآن وإسلامية", "ت4-2 قرآن وإسلامية", "ت4-1 تجويد", "ت4-2 تجويد", "ت4-1 حياتية"]},
            {"day": "الاثنين", "periods": ["ت4-2 قرآن وإسلامية", "ت4-1 قرآن وإسلامية", "ت4-1 لغتي", "ت4-1 تجويد", "ت4-2 لغتي", "", "ت4-2 علوم"]},
            {"day": "الثلاثاء", "periods": ["ت4-1 لغتي", "ت4-2 لغتي", "ت4-1 قرآن وإسلامية", "ت4-2 قرآن وإسلامية", "", "", "ت4-2 حياتية"]},
            {"day": "الأربعاء", "periods": ["", "", "ت4-1 لغتي", "ت4-1 قرآن وإسلامية", "ت4-2 لغتي", "", ""]},
            {"day": "الخميس", "periods": ["ت4-2 قرآن وإسلامية", "ت4-1 قرآن وإسلامية", "", "", "", "", ""]}
          ],
          "إبراهيم بن حسن بن خلوفه طياش": [
            {"day": "الأحد", "periods": ["", "", "ت3-1 لغتي", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["", "ت3-1 لغتي", "", "", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["", "ت3-1 لغتي", "", "", "", "", ""]},
            {"day": "الأربعاء", "periods": ["", "ت3-1 لغتي", "", "", "", "", ""]},
            {"day": "الخميس", "periods": ["", "ت3-1 لغتي", "", "", "", "", ""]}
          ],
          "سامي احمد سالم محمد الصبحي": [
            {"day": "الأحد", "periods": ["ت3-2 لغتي", "", "", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["ت3-2 لغتي", "", "", "", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["ت3-2 لغتي", "", "", "", "ت3-2 حياتية", "", ""]},
            {"day": "الأربعاء", "periods": ["ت3-2 لغتي", "", "", "", "", "", ""]},
            {"day": "الخميس", "periods": ["ت3-2 لغتي", "", "", "", "", "", ""]}
          ],
          "خالد بن راشد بن نجم العصلاني": [
            {"day": "الأحد", "periods": ["", "", "", "ت5-2 لغتي", "", "", ""]},
            {"day": "الاثنين", "periods": ["ت5-2 لغتي", "", "", "", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["", "", "ت5-2 لغتي", "", "", "", ""]},
            {"day": "الأربعاء", "periods": ["", "", "ت5-2 لغتي", "", "", "", ""]},
            {"day": "الخميس", "periods": ["", "ت5-2 لغتي", "", "", "", "", ""]}
          ],
          "محمد عبدالله احمد الرايقي": [
            {"day": "الأحد", "periods": ["", "", "ت5-1 لغتي", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["", "ت5-1 لغتي", "", "", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["", "", "", "ت5-1 لغتي", "", "", ""]},
            {"day": "الأربعاء", "periods": ["", "", "", "ت5-1 لغتي", "", "", ""]},
            {"day": "الخميس", "periods": ["ت5-1 لغتي", "", "", "", "", "", ""]}
          ],
          "محمد عبدالصمد خضر المعلم": [
            {"day": "الأحد", "periods": ["", "ت5-1 رياضيات", "", "ت3-1 رياضيات", "ت3-2 رياضيات", "", ""]},
            {"day": "الاثنين", "periods": ["", "", "ت3-1 رياضيات", "ت3-2 رياضيات", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["ت5-1 رياضيات", "", "ت3-1 رياضيات", "ت3-2 رياضيات", "", "", ""]},
            {"day": "الأربعاء", "periods": ["", "ت5-1 رياضيات", "ت3-1 رياضيات", "ت3-2 رياضيات", "", "", ""]},
            {"day": "الخميس", "periods": ["", "", "ت3-1 رياضيات", "ت3-2 رياضيات", "", "", ""]}
          ],
          "عماد الحسن عطية الله المحمدي": [
            {"day": "الأحد", "periods": ["ت5-2 رياضيات", "", "", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["", "", "", "ت5-2 رياضيات", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["", "ت5-2 رياضيات", "", "", "", "", ""]},
            {"day": "الأربعاء", "periods": ["ت5-2 رياضيات", "", "", "", "", "", ""]},
            {"day": "الخميس", "periods": ["", "", "ت5-2 رياضيات", "", "", "", ""]}
          ],
          "وجدي علي مرشد العبيدي": [
            {"day": "الأحد", "periods": ["ت4-2 رياضيات", "ت4-1 رياضيات", "", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["ت4-1 رياضيات", "ت4-2 رياضيات", "", "", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["", "", "ت4-2 رياضيات", "ت4-1 رياضيات", "", "", ""]},
            {"day": "الأربعاء", "periods": ["ت4-1 رياضيات", "ت4-2 رياضيات", "", "", "", "", ""]},
            {"day": "الخميس", "periods": ["", "", "ت4-1 رياضيات", "ت4-2 رياضيات", "", "", ""]}
          ],
          "طلال علي محمد النخلي": [
            {"day": "الأحد", "periods": ["", "ت6-2 رياضيات", "ت6-1 رياضيات", "", "", "", ""]},
            {"day": "الاثنين", "periods": ["ت6-1 رياضيات", "ت6-2 رياضيات", "", "", "", "", ""]},
            {"day": "الثلاثاء", "periods": ["ت6-2 رياضيات", "", "", "", "", "ت6-1 رياضيات", ""]},
            {"day": "الأربعاء", "periods": ["ت6-2 رياضيات", "", "", "ت6-1 رياضيات", "", "", ""]},
            {"day": "الخميس", "periods": ["", "ت6-1 رياضيات", "", "", "ت6-2 رياضيات", "", ""]}
          ],
          "وجدي بن حامد بن محمد الكريثي": [
            {"day": "الأحد", "periods": ["", "", "", "", "ت5-1 علوم", "ت5-2 علوم", ""]},
            {"day": "الاثنين", "periods": ["", "", "ت3-1 علوم", "ت3-2 علوم", "ت5-1 علوم", "ت5-2 علوم", ""]},
            {"day": "الثلاثاء", "periods": ["", "", "ت3-2 علوم", "ت3-1 علوم", "", "", ""]},
            {"day": "الأربعاء", "periods": ["", "", "ت5-1 علوم", "ت5-2 علوم", "", "", ""]},
            {"day": "الخميس", "periods": ["", "", "ت5-1 علوم", "ت5-2 علوم", "", "", ""]}
          ],
          "هتان حمدان حمود العوفي": [
            {"day": "الأحد", "periods": ["", "", "ت6-2 علوم", "ت6-1 علوم", "", "", ""]},
            {"day": "الاثنين", "periods": ["", "", "", "", "", "ت6-2 علوم", ""]},
            {"day": "الثلاثاء", "periods": ["ت4-2 علوم", "ت4-1 علوم", "ت6-1 علوم", "", "", "", ""]},
            {"day": "الأربعاء", "periods": ["ت4-2 علوم", "ت4-1 علوم", "", "", "", "ت6-1 علوم", ""]},
            {"day": "الخميس", "periods": ["", "", "", "ت6-2 علوم", "", "", ""]}
          ],
          "حمدان محمد عيد الغانمي": [
            {"day": "الأحد", "periods": ["", "", "", "", "", "", "ت5-1 رقمية"]},
            {"day": "الاثنين", "periods": ["", "", "", "", "ت5-2 رقمية", "ت5-1 رقمية", ""]},
            {"day": "الثلاثاء", "periods": ["", "", "", "", "ت4-1 رقمية", "ت4-2 رقمية", ""]},
            {"day": "الأربعاء", "periods": ["", "", "ت6-1 رقمية", "", "", "", "ت6-2 رقمية"]},
            {"day": "الخميس", "periods": ["", "", "ت4-2 رقمية", "ت4-1 رقمية", "ت3-2 رقمية", "ت3-1 رقمية", "ت6-1 رقمية"]}
          ],
          "بدر بادي محمد الزبيدي": [
            {"day": "الأحد", "periods": ["", "", "ت5-2 بدنية", "ت3-2 بدنية", "ت3-1 بدنية", "ت4-2 بدنية", "ت6-2 بدنية"]},
            {"day": "الاثنين", "periods": ["", "", "", "", "", "ت6-1 بدنية", ""]},
            {"day": "الثلاثاء", "periods": ["", "", "", "", "ت5-2 بدنية", "ت3-2 بدنية", ""]},
            {"day": "الأربعاء", "periods": ["", "", "", "ت5-1 بدنية", "", "", ""]},
            {"day": "الخميس", "periods": ["", "", "", "", "", "", ""]}
          ]
        };

        // INITIAL WAITING SCHEDULE FROM PDF
        const initialWaitingSched = [
            { day: "الأحد", p1: "1- محمد المعلم<br>2- حمدان الغانمي", p2: "1- ناصر الحربي<br>2- محمد الرايقي", p3: "1- عماد المحمدي<br>2- سامي الصبحي", p4: "1- بدر الزبيدي<br>2- خالد العصلاني", p5: "1- يوسف اليوبي<br>2- عبدالعزيز المولد", p6: "1- خالد العصلاني<br>2- يسار فوريه", p7: "-" },
            { day: "الاثنين", p1: "1- محمد الرايقي<br>2- إبراهيم طياش", p2: "1- خالد العصلاني<br>2- عبدالاله السلمي", p3: "1- حمدان الغانمي<br>2- حمزه الحربي", p4: "1- تركي البلادي<br>2- وجدي العبيدي", p5: "1- عبدالعزيز المولد<br>2- بدر الزبيدي", p6: "1- طلال النخلي<br>2- خالد العصلاني", p7: "-" },
            { day: "الثلاثاء", p1: "1- خالد العصلاني<br>2- بدر الزبيدي", p2: "1- يسار فوريه<br>2- طلال النخلي", p3: "1- ياسر الكنيدري<br>2- عماد المحمدي", p4: "1- حمدان الغانمي<br>2- محمد المعلم", p5: "1- ناصر الحربي<br>2- عبدالعزيز المولد", p6: "1- وجدي العبيدي<br>2- خالد العصلاني", p7: "-" },
            { day: "الأربعاء", p1: "1- طلال النخلي<br>2- محمد المعلم", p2: "1- بدر الزبيدي<br>2- وجدي العبيدي", p3: "1- عماد المحمدي<br>2- احمد الحربي", p4: "1- عبدالله العنزي<br>2- ناصر الحربي", p5: "1- عبدالعزيز المولد<br>2- ياسر الكنيدري", p6: "1- عبدالاله السلمي<br>2- خالد العصلاني", p7: "-" },
            { day: "الخميس", p1: "1- حمزه الحربي<br>2- طلال النخلي", p2: "1- وجدي العبيدي<br>2- خالد العصلاني", p3: "1- إبراهيم طياش<br>2- يوسف اليوبي", p4: "1- احمد الحربي<br>2- عماد المحمدي", p5: "1- سامي الصبحي<br>2- تركي البلادي", p6: "1- محمد المعلم<br>2- خالد العصلاني", p7: "-" }
        ];

        // INITIAL RECESS SUPERVISION SCHEDULE FROM EXCEL (إشراف الفسحة)
        const initialSupervisionSched = [
            { day: "الأحد", text: "طلال علي محمد النخلي (المقصف)<br>وجدي بن حامد الكريثي (الساحة الرئيسية)<br>سامي احمد سالم الصبحي (المقصف)<br>محمد عبدالله احمد الرايقي (الساحة الرئيسية)" },
            { day: "الاثنين", text: "إبراهيم بن حسن طياش (المقصف، الساحة الرئيسية)<br>محمد عبدالصمد المعلم (المقصف)<br>تركي بن مرشود البلادي (المقصف)<br>حمزه ناصر علي الحربي (الساحة الرئيسية)" },
            { day: "الثلاثاء", text: "يسار عبدالرزاق علي موريه (المقصف)<br>ياسر عبيدالله الكنيدري (الساحة الرئيسية)<br>بدر بادي محمد الزبيدي (المقصف)<br>عبدالله فايز فرحان العنزي (الساحة الرئيسية)" },
            { day: "الأربعاء", text: "خالد بن راشد العصلاني (المقصف، الساحة الرئيسية)<br>عبدالاله عبدربه السلمى (الساحة الرئيسية)<br>ناصر علي محسن الحربي (المقصف)<br>عماد الحسن عطية المحمدي (الساحة الرئيسية)" },
            { day: "الخميس", text: "عبدالعزيز حامد المولد (المقصف)<br>احمد حطيحط عواض الحربي (الساحة الرئيسية)<br>يوسف مبرك حميد اليوبي (المقصف)<br>وجدي علي مرشد العبيدي (الساحة الرئيسية)" }
        ];

        // DYNAMIC DUTY LIST (جدول المناوبة)
        const initialMonawabaList = [
            { day: "الأحد", date: "1448/03/17هـ", teacher: "أ. إبراهيم بن حسن طياش", location: "الاصطفاف والساحة الخارجية" },
            { day: "الاثنين", date: "1448/03/18هـ", teacher: "أ. تركي بن مرشود البلادي", location: "المقصف والدور الأرضي" },
            { day: "الثلاثاء", date: "1448/03/19هـ", teacher: "أ. عماد الحسن المحمدي", location: "الممر الرئيسي والدور العلوي" },
            { day: "الأربعاء", date: "1448/03/20هـ", teacher: "أ. عبدالاله عبدربه السلمي", location: "المخرج الرئيسي وبوابة الخروج" },
            { day: "الخميس", date: "1448/03/21هـ", teacher: "أ. بدر بادي الزبيدي", location: "الملعب والساحات الداخلية" }
        ];

        // SCHEDULES SUBTAB CONTROLLER
        function switchSchedSubTab(schedSubTabId) {
            document.querySelectorAll('.sched-subtab-panel').forEach(el => el.classList.add('hidden'));
            document.getElementById(`sched-${schedSubTabId}`).classList.remove('hidden');

            document.querySelectorAll('.sched-subtab-btn').forEach(btn => {
                btn.classList.remove('bg-emerald-600', 'text-white', 'active');
                btn.classList.add('bg-slate-800', 'text-slate-300', 'hover:bg-slate-700');
            });

            const activeSubBtn = document.getElementById(`sched-btn-${schedSubTabId}`);
            if(activeSubBtn) {
                activeSubBtn.classList.add('bg-emerald-600', 'text-white', 'active');
                activeSubBtn.classList.remove('bg-slate-800', 'text-slate-300', 'hover:bg-slate-700');
            }
        }

        // PRINT SINGLE SECTION FUNCTION
        function printSingleSection(sectionId) {
            document.querySelectorAll('.tab-panel, .subtab-panel, .sched-subtab-panel').forEach(el => el.classList.remove('active-print'));
            const target = document.getElementById(sectionId);
            if(target) target.classList.add('active-print');
            window.print();
        }

        // POPULATE TEACHER SELECT & RENDER
        function populateTeacherSelect() {
            const select = document.getElementById('teacherSelectFilter');
            const teacherNames = Object.keys(masterTeachersData);
            select.innerHTML = teacherNames.map(name => `<option value="${name}">${name}</option>`).join('');
            renderTeacherIndividualSchedule();
        }

        function renderTeacherIndividualSchedule() {
            const teacherName = document.getElementById('teacherSelectFilter').value;
            document.getElementById('printTeacherTitle').innerText = `جدول حصص المعلم: ${teacherName}`;
            const sched = masterTeachersData[teacherName] || [];
            const body = document.getElementById('individualTeacherSchedBody');

            body.innerHTML = sched.map((row, idx) => `
                <tr class="hover:bg-slate-800/40">
                    <td class="p-2.5 font-bold text-emerald-400 border border-slate-700">${row.day}</td>
                    ${row.periods.map((p, pIdx) => `<td class="p-2.5 border border-slate-700 font-medium" contenteditable="true" onblur="updateMasterTeacherPeriod('${teacherName}', ${idx}, ${pIdx}, this.innerText)">${p}</td>`).join('')}
                </tr>
            `).join('');
        }

        function updateMasterTeacherPeriod(tName, dIdx, pIdx, val) {
            if(masterTeachersData[tName] && masterTeachersData[tName][dIdx]) {
                masterTeachersData[tName][dIdx].periods[pIdx] = val;
                localStorage.setItem('eid_teachers_grid', JSON.stringify(masterTeachersData));
            }
        }

        // RENDER CLASS INDIVIDUAL SCHEDULE
        function renderClassIndividualSchedule() {
            const className = document.getElementById('classSelectFilter').value;
            document.getElementById('printClassTitle').innerText = `جدول الحصص المعتمد للفصل - ${className}`;
            const sched = masterClassesData[className] || [];
            const body = document.getElementById('individualClassSchedBody');

            body.innerHTML = sched.map((row, idx) => `
                <tr class="hover:bg-slate-800/40">
                    <td class="p-2.5 font-bold text-blue-400 border border-slate-700">${row.day}</td>
                    ${row.periods.map((p, pIdx) => `<td class="p-2.5 border border-slate-700 font-medium" contenteditable="true" onblur="updateMasterClassPeriod('${className}', ${idx}, ${pIdx}, this.innerText)">${p}</td>`).join('')}
                </tr>
            `).join('');
        }

        function updateMasterClassPeriod(cName, dIdx, pIdx, val) {
            if(masterClassesData[cName] && masterClassesData[cName][dIdx]) {
                masterClassesData[cName][dIdx].periods[pIdx] = val;
                localStorage.setItem('eid_classes_grid', JSON.stringify(masterClassesData));
            }
        }

        // RENDER WAITING SCHEDULE
        function renderWaitingSchedule() {
            const list = JSON.parse(localStorage.getItem('eid_waiting_sched')) || initialWaitingSched;
            const body = document.getElementById('waitingSchedBody');
            body.innerHTML = list.map((item, idx) => `
                <tr class="hover:bg-slate-800/40">
                    <td class="p-2.5 font-bold text-amber-400 border border-slate-700">${item.day}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p1', this.innerHTML)">${item.p1}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p2', this.innerHTML)">${item.p2}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p3', this.innerHTML)">${item.p3}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p4', this.innerHTML)">${item.p4}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p5', this.innerHTML)">${item.p5}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p6', this.innerHTML)">${item.p6}</td>
                    <td class="p-2.5 border border-slate-700" contenteditable="true" onblur="updateSchedData('eid_waiting_sched', ${idx}, 'p7', this.innerHTML)">${item.p7}</td>
                </tr>
            `).join('');
        }

        // RENDER SUPERVISION SCHEDULE
        function renderSupervisionSchedule() {
            const list = JSON.parse(localStorage.getItem('eid_supervision_sched')) || initialSupervisionSched;
            const body = document.getElementById('supervisionSchedBody');
            body.innerHTML = list.map((item, idx) => `
                <tr class="hover:bg-slate-800/40">
                    <td class="p-3 font-bold text-purple-400 border border-slate-700">${item.day}</td>
                    <td class="p-3 border border-slate-700 text-slate-200 leading-relaxed font-bold" contenteditable="true" onblur="updateSchedData('eid_supervision_sched', ${idx}, 'text', this.innerHTML)">${item.text}</td>
                </tr>
            `).join('');
        }

        // RENDER MONAWABA SCHEDULE (LIST WITH ADD/DELETE ROWS)
        function renderMonawabaSchedule() {
            const list = JSON.parse(localStorage.getItem('eid_monawaba_list')) || initialMonawabaList;
            const body = document.getElementById('monawabaSchedBody');
            body.innerHTML = list.map((item, idx) => `
                <tr class="hover:bg-slate-800/40">
                    <td class="p-2.5 text-center font-bold text-slate-500 border border-slate-700">${idx+1}</td>
                    <td class="p-2.5 font-bold text-teal-400 border border-slate-700" contenteditable="true" onblur="updateMonawabaRow(${idx}, 'day', this.innerText)">${item.day}</td>
                    <td class="p-2.5 text-slate-300 border border-slate-700" contenteditable="true" onblur="updateMonawabaRow(${idx}, 'date', this.innerText)">${item.date}</td>
                    <td class="p-2.5 font-bold text-white border border-slate-700" contenteditable="true" onblur="updateMonawabaRow(${idx}, 'teacher', this.innerText)">${item.teacher}</td>
                    <td class="p-2.5 text-slate-300 border border-slate-700" contenteditable="true" onblur="updateMonawabaRow(${idx}, 'location', this.innerText)">${item.location}</td>
                    <td class="p-2.5 text-center border border-slate-700 no-print">
                        <button onclick="deleteMonawabaRow(${idx})" class="text-rose-400 hover:text-rose-300 font-bold"><i class="fa-solid fa-trash"></i></button>
                    </td>
                </tr>
            `).join('');
        }

        function updateMonawabaRow(idx, field, val) {
            let list = JSON.parse(localStorage.getItem('eid_monawaba_list')) || initialMonawabaList;
            if(list[idx]) {
                list[idx][field] = val;
                localStorage.setItem('eid_monawaba_list', JSON.stringify(list));
            }
        }

        function addMonawabaRow() {
            let list = JSON.parse(localStorage.getItem('eid_monawaba_list')) || initialMonawabaList;
            list.push({ day: "الأحد", date: "1448/03/...هـ", teacher: "اسم المعلم المناوب", location: "الموقع" });
            localStorage.setItem('eid_monawaba_list', JSON.stringify(list));
            renderMonawabaSchedule();
        }

        function deleteMonawabaRow(idx) {
            let list = JSON.parse(localStorage.getItem('eid_monawaba_list')) || initialMonawabaList;
            list.splice(idx, 1);
            localStorage.setItem('eid_monawaba_list', JSON.stringify(list));
            renderMonawabaSchedule();
        }

        function updateSchedData(key, idx, field, val) {
            let list = JSON.parse(localStorage.getItem(key)) || (key==='eid_waiting_sched'?initialWaitingSched:initialSupervisionSched);
            if(list[idx]) {
                list[idx][field] = val;
                localStorage.setItem(key, JSON.stringify(list));
            }
        }

        // --- MASTER INITIAL CLASSES DATA ---
        const initialSchool1Classes = [
            { grade: "الثالث ابتدائي", classes: 1, students: 39 },
            { grade: "الرابع ابتدائي", classes: 2, students: 71 },
            { grade: "الخامس ابتدائي", classes: 2, students: 44 },
            { grade: "السادس ابتدائي", classes: 1, students: 37 }
        ];

        const initialSchool2Classes = [
            { grade: "الثالث ابتدائي", classes: 2, students: 50 },
            { grade: "الرابع ابتدائي", classes: 2, students: 51 },
            { grade: "الخامس ابتدائي", classes: 3, students: 76 },
            { grade: "السادس ابتدائي", classes: 2, students: 50 }
        ];

        const initialAdminStaff = [
            { name: "خالد بن عطيه بن محمد السيد", role: "مدير المدرسة", major: "إدارة تعليمية", license: "حاصل على الرخصة (خبير)" },
            { name: "حاتم بن أحمد أبو خضير", role: "وكيل الشؤون التعليمية", major: "علوم", license: "حاصل على الرخصة (متقدم)" },
            { name: "عيد بن عايد المحمدي", role: "وكيل شؤون الطلاب", major: "إدارة وتخطيط", license: "حاصل على الرخصة (متقدم)" },
            { name: "أحمد صالح أحمد الغانمي", role: "الموجه الطلابي", major: "علم نفس / توجيه", license: "حاصل على الرخصة" },
            { name: "بدر بادي محمد الزبيدي", role: "رائد النشاط المدرسي", major: "تربية بدنية", license: "حاصل على الرخصة" },
            { name: "وجدي بن حامد الكريثي", role: "المرشد الصحي", major: "علوم صحية", license: "حاصل على الرخصة" },
            { name: "بدر بن محمد علي الذروي", role: "مسؤول الأمن والسلامة", major: "إداري", license: "غير متاح" }
        ];

        const initialTeachersStaff = [
            { name: "إبراهيم بن حسن طياش", role: "معلم", major: "دراسات إسلامية", license: "حاصل على الرخصة" },
            { name: "أحمد حطيبح عواض الحربي", role: "معلم", major: "لغة عربية", license: "حاصل على الرخصة" },
            { name: "بدر بادي محمد الزبيدي", role: "معلم / رائد نشاط", major: "تربية بدنية", license: "حاصل على الرخصة" },
            { name: "تركي بن مرشود البلادي", role: "معلم", major: "دراسات إسلامية", license: "حاصل على الرخصة" },
            { name: "حمدان محمد عبد الغانمي", role: "معلم / حاسب آلي", major: "حاسب آلي وتقنية", license: "حاصل على الرخصة (متقدم)" },
            { name: "محمد عبدالصمد المعلم", role: "معلم", major: "رياضيات", license: "حاصل على الرخصة (متقدم)" },
            { name: "حمزه ناصر علي الحربي", role: "معلم", major: "دراسات إسلامية", license: "حاصل على الرخصة" },
            { name: "خالد بن راشد بن نجم العصلاني", role: "معلم", major: "لغة عربية", license: "حاصل على الرخصة" },
            { name: "سامي أحمد سالم محمد الصبحي", role: "معلم", major: "لغة عربية", license: "حاصل على الرخصة" },
            { name: "طلال علي محمد النخلي", role: "معلم", major: "رياضيات", license: "حاصل على الرخصة" },
            { name: "عادل حمد مصلح العصلاني", role: "معلم", major: "اجتماعيات", license: "حاصل على الرخصة" },
            { name: "عبدالإله عبدربه بن رابح السلمي", role: "معلم", major: "لغة عربية", license: "حاصل على الرخصة" },
            { name: "عبدالعزيز حامد هلال المولد", role: "معلم", major: "تربية بدنية", license: "حاصل على الرخصة" },
            { name: "عبدالله فايز فرحان العنزي", role: "معلم", major: "لغة إنجليزية", license: "حاصل على الرخصة" },
            { name: "علي عبدالرحمن الزهراني", role: "معلم", major: "لغة إنجليزية", license: "حاصل على الرخصة" },
            { name: "عماد الحسن المحمدي", role: "معلم", major: "رياضيات", license: "حاصل على الرخصة" },
            { name: "محمد عبدالله أحمد الرايقي", role: "معلم", major: "لغة عربية", license: "حاصل على الرخصة" },
            { name: "هتان حمدان حمود العوفي", role: "معلم", major: "علوم", license: "حاصل على الرخصة" },
            { name: "وجدي بن حامد الكريثي", role: "معلم / موجه صحي", major: "علوم", license: "حاصل على الرخصة" },
            { name: "وجدي علي مرشد العبيدي", role: "معلم", major: "رياضيات", license: "حاصل على الرخصة" },
            { name: "ياسر بن عبيدالله الكنيدري", role: "معلم", major: "دراسات إسلامية", license: "حاصل على الرخصة" },
            { name: "يسار عبدالرزاق علي فوريه", role: "معلم", major: "دراسات إسلامية", license: "حاصل على الرخصة" },
            { name: "يوسف مبروك بن حميد اليوبي", role: "معلم", major: "دراسات إسلامية", license: "حاصل على الرخصة" }
        ];

        const initialAssistantsStaff = [
            { name: "مساعد إداري 1", role: "مساعد إداري", major: "إدارة مكتبية", license: "غير حاصل" },
            { name: "مساعد إداري 2", role: "مسجل معلومات", major: "تقنية معلومات", license: "غير حاصل" }
        ];

        let defaultCommitteesData = [
            {
                id: 1, title: "1. لجنة التميز والتحصيل الدراسي",
                members: [
                    { id: 101, name: "أ. خالد بن عطيه السيد", role: "رئيس اللجنة", task: "الإشراف العام واعتماد الخطط ومتابعة مؤشرات الأداء" },
                    { id: 102, name: "أ. حاتم بن أحمد أبو خضير", role: "نائب الرئيس", task: "إدارة البرامج التعليمية ومتابعة نتائج التحصيل والزيارات" },
                    { id: 103, name: "أ. محمد عبدالصمد المعلم", role: "منسق التميز ونافس", task: "متابعة تحسين نواتج اختبارات نافس الوطنية" }
                ]
            },
            {
                id: 2, title: "2. لجنة التوجيه والإنضباط المدرسي",
                members: [
                    { id: 201, name: "أ. عيد بن عايد المحمدي", role: "رئيس اللجنة", task: "الإشراف على قواعد السلوك والمواظبة والتواصل مع الأسر" },
                    { id: 202, name: "أ. أحمد صالح الغانمي", role: "الموجه الطلابي", task: "متابعة الرعاية السلوكية والبرامج الوقائية ودراسة الحالة" }
                ]
            },
            {
                id: 3, title: "3. لجنة الأمن والسلامة والصحة المدرسية",
                members: [
                    { id: 301, name: "أ. بدر بن محمد الذروي", role: "منسق الأمن والسلامة", task: "فحص طفايات الحريق والإشراف على فرضيات الإخلاء" },
                    { id: 302, name: "أ. وجدي بن حامد الكريثي", role: "الموجه الصحي", task: "الفحوصات الطبية المدرسية والتنسيق مع مركز صفا الصحي برابغ" }
                ]
            },
            {
                id: 4, title: "4. لجنة الأنشطة الطلابية والموهبة",
                members: [
                    { id: 401, name: "أ. بدر بادي الزبيدي", role: "رائد النشاط", task: "تنظيم المسابقات والأنشطة الخمسة والمجلس الطلابي والدوري" },
                    { id: 402, name: "منسق الموهوبين", role: "مشرف الموهبة", task: "اكتشاف الطلاب الموهوبين والترشيح لمقياس موهبة" }
                ]
            }
        ];

        let defaultPrograms = [
            { id: 1, domain: 1, name: "برنامج تمكين القيادة والتخطيط المستدام", standard: "التخطيط (1-1-1)", initiative: "مختبر التخطيط القيادي واستدامة التميز", goal: "تأهيل وتمكين فريق التميز المدرسي في مهارات إعداد الخطط التشغيلية وتجويدها وتطوير كفاياتهم القيادية.", steps: "1. إقامة ورش تدريبية لفريق التميز حول أدوات التخطيط التشغيلي.\n2. تطبيق الممارسة العملية في تحليل البيانات وتشخيص الواقع.\n3. توزيع المسؤوليات القيادية في متابعة الخطة طوال العام.", lead: "أ. خالد بن عطيه السيد (مدير المدرسة)", cost: "0 ريال", term1: "من 17 / 3 إلى 13 / 4 / 1448 هـ", term2: "من 9 / 8 إلى 20 / 8 / 1448 هـ", progress: 100, proof: "محاضر الاجتماعات وخطابات التكليف" },
            { id: 2, domain: 1, name: "المدرسة مركز تدريبي", standard: "التطوير المؤسسي (1-4-1)", initiative: "مجتمعات التعلم المهنية التفاعلية", goal: "رفع الكفاءة التدريسية والإدارية للمعلمين من خلال تنفيذ دورات تدريبية داخلية وتفعيل مجتمعات التعلم.", steps: "1. تحديد الاحتياجات التدريبية للمعلمين.\n2. إعداد الحقائب التدريبية.\n3. عقد الورش التدريبية داخل المدرسة.", lead: "أ. حاتم بن أحمد أبو خضير (وكيل الشؤون التعليمية)", cost: "300 ريال", term1: "من 9 / 4 إلى 11 / 5 / 1448 هـ", term2: "من 23 / 8 إلى 10 / 10 / 1448 هـ", progress: 60, proof: "شهادات الحضور وصور الورش" },
            { id: 3, domain: 1, name: "برنامج التواصل المستدام وقياس رضا الأسر", standard: "المجتمع المدرسي (1-3-1)", initiative: "استبانة الرضا الشفاف والرسائل الرقمية", goal: "تفعيل قنوات التواصل الرقمية وسجلات المتابعة مع أولياء الأمور لرفع المتابعة المنزلية ونسبة الرضا إلى 90%.", steps: "1. تحديث بيانات أرقام أولياء الأمور وتفعيل SMS.\n2. إطلاق استبانة رضا الأسر الأولى والثانية.\n3. تفريغ الاستبيانات وإعداد تقرير تحليلي للجنة التميز.", lead: "أ. عيد بن عايد المحمدي (وكيل شؤون الطلاب)", cost: "200 ريال", term1: "الخميس 2 / 6 / 1448 هـ", term2: "الخميس 24 / 10 / 1448 هـ", progress: 85, proof: "تقارير إرسال SMS ونماذج Google Forms" },
            { id: 4, domain: 1, name: "برنامج صحتي وبيئتي برابغ", standard: "المجتمع المدرسي (1-3-1)", initiative: "طبيب في مدرستنا", goal: "عقد شراكات صحية وميدانية مع المركز الصحي والمؤسسات الخدمية برابغ لدعم سلامة وصحة الطلاب.", steps: "1. مخاطبة مركز صفا الصحي برابغ رسمياً.\n2. جدولة زيارات الكادر الطبي للمدرسة.\n3. إجراء الفحوصات وإبلاغ الأسر بالملاحظات.", lead: "أ. وجدي الكريثي (المرشد الصحي)", cost: "0 ريال", term1: "من 16 / 4 إلى 21 / 5 / 1448 هـ", term2: "من 2 / 9 إلى 23 / 10 / 1448 هـ", progress: 50, proof: "تقارير الفحوصات وخطابات الشراكة" },
            { id: 5, domain: 1, name: "برنامج المعلم المتميز", standard: "التطوير المؤسسي (1-4-1)", initiative: "وسام التميز المهني", goal: "تقدير وتكريم المعلمين المتميزين والانضباط الوظيفي والحاصلين على الترقيات المهنية.", steps: "1. وضع معايير الترقيات.\n2. رصد الأداء والتزام المعلمين.\n3. تكريم المتميزين في الإذاعة وتوزيع الشهادات.", lead: "أ. خالد بن عطيه السيد", cost: "500 ريال", term1: "الأربعاء 11 / 6 / 1448 هـ", term2: "الأربعاء 14 / 11 / 1448 هـ", progress: 40, proof: "لوحة الشرف وشهادات التقدير" },
            { id: 6, domain: 1, name: "برنامج تعزيز السلوك الإيجابي", standard: "قيادة العملية التعليمية (1-2-1)", initiative: "بوابة الحضور المبكر", goal: "توفير بيئة مدرسية داعمة للانضباط للحد من المخالفات السلوكية والتأخر الصباحي بنسبة 95%.", steps: "1. رصد الانضباط اليومي عبر منصة نور.\n2. تكريم الفصول والطلاب المنتظمين.\n3. التواصل مع أسر المتغيبين.", lead: "أ. أحمد صالح الغانمي (الموجه الطلابي)", cost: "200 ريال", term1: "مستمر طوال الفصل الأول", term2: "مستمر طوال الفصل الثاني", progress: 90, proof: "سجلات التعزيز ونظام نور" },
            
            { id: 7, domain: 2, name: "برنامج بالإملاء والقراءة ننافس", standard: "بناء خبرات التعلم (2-1-1)", initiative: "عشر دقائق قرائية", goal: "تنفيذ برامج علاجية مكثفة لرفع الطلاقة القرائية والكتابية لدى الطلاب بنسبة تحسن 20%.", steps: "1. فرز الطلاب ضعاف القراءة والإملاء.\n2. تطبيق خطة قرائية 10 دقائق يومياً.\n3. إجراء قياس أسبوعي لمستوى التقدم.", lead: "معلمو اللغة العربية والوكيل", cost: "400 ريال", term1: "من 24 / 3 إلى 23 / 6 / 1448 هـ", term2: "من 9 / 8 إلى 29 / 11 / 1448 هـ", progress: 70, proof: "دفتر القرائية واختبارات الطلاقة" },
            { id: 8, domain: 2, name: "برنامج STEM والعلوم المبتكرة", standard: "بناء خبرات التعلم (2-1-1)", initiative: "مستكشف المستقبل", goal: "إكساب الطلاب مهارات التفكير العليا والتطبيقات العلمية والرياضية التشاركية.", steps: "1. تجهيز المعامل بالخامات.\n2. توزيع الطلاب على فرق عمل.\n3. عرض التجارب في معرض المدرسة.", lead: "معلمو الرياضيات والعلوم", cost: "300 ريال", term1: "من 23 / 4 إلى 2 / 6 / 1448 هـ", term2: "من 7 / 9 إلى 1 / 11 / 1448 هـ", progress: 30, proof: "صور التجارب المعملية والمستكشف" },
            { id: 9, domain: 2, name: "برنامج التقويم التشخيصي المستمر", standard: "تقويم التعلم (2-2-1)", initiative: "بطاقة التحسن الأكاديمي", goal: "تشخيص المستويات التحصيلية بصفة مستمرة وتحليل نتائج الاختبارات لبناء خطط الدعم.", steps: "1. بناء أوراق تقويم لكل مادة.\n2. تطبيق الاختبار وتصحيحه.\n3. تصنيف الطلاب وإعداد خطة الدعم.", lead: "جميع معلمي المواد الدراسية", cost: "400 ريال", term1: "المتابعة 1: 24 / 3 | 2: 7 / 5 / 1448 هـ", term2: "المتابعة 1: 9 / 8 | 2: 13 / 10 / 1448 هـ", progress: 80, proof: "تحليل نواتج الاختبار التشخيصي" },
            { id: 10, domain: 2, name: "برنامج تبادل الزيارات الصفية", standard: "بناء خبرات التعلم (2-1-1)", initiative: "حصص الأقران النموذجية", goal: "تنويع استراتيجيات التدريس وتبادل الزيارات التبادلية بمعدل زيارتين لكل معلم سنوياً.", steps: "1. إعداد جدول الزيارات التبادلية.\n2. حضور الحصة وتسجيل نقاط القوة.\n3. عقد جلسة نقاش بعد الحصة.", lead: "أ. حاتم أبو خضير والمعلمون", cost: "200 ريال", term1: "من 16 / 4 إلى 9 / 6 / 1448 هـ", term2: "من 23 / 8 إلى 8 / 11 / 1448 هـ", progress: 50, proof: "استمارات الزيارات التبادلية" },
            { id: 11, domain: 2, name: "برنامج الحقيبة المهارية الذكية", standard: "بناء خبرات التعلم (2-1-1)", initiative: "حقيبة التعلم الذاتي", goal: "تزويد الطلاب بأنشطة وصفية وحقائب منزلية تعزز الاعتماد على النفس والتحصيل الذاتي.", steps: "1. إعداد الحقيبة المهارية ورقية ورقمية بأكواد QR.\n2. توزيعها على الطلاب ومتابعتها.\n3. تقديم التغذية الراجعة.", lead: "رواد الفصول ورائد النشاط", cost: "0 ريال", term1: "من 2 / 4 إلى 16 / 6 / 1448 هـ", term2: "من 16 / 8 إلى 22 / 11 / 1448 هـ", progress: 60, proof: "استمارات متابعة أوراق عمل QR" },
            { id: 12, domain: 2, name: "برنامج بصيرتي الرقمية", standard: "بناء خبرات التعلم (2-1-1)", initiative: "المواطن الرقمي المبدع", goal: "تفعيل المعمل الرقمي والمنصات الرسمية لتنمية المهارات التقنية والتفاعلية للطلاب بنسبة 90%.", steps: "1. جدولة استخدام المعمل الرقمي.\n2. دمج منصة مدرستي بالأنشطة.\n3. تقييم المهارات التقنية للطلاب.", lead: "أ. حمدان محمد الغانمي (معلم الحاسب)", cost: "200 ريال", term1: "من 2 / 4 إلى 9 / 6 / 1448 هـ", term2: "من 16 / 8 إلى 8 / 11 / 1448 هـ", progress: 75, proof: "سجلات المعمل ومنصة مدرستي" },

            { id: 13, domain: 3, name: "برنامج استعدادات نافس الوطنية", standard: "التحصيل التعليمي (3-1-1)", initiative: "تفكيرنا عالٍ.. وننافس", goal: "رفع متوسط أداء المدرسة في نافس بنسبة 5% وعلاج فجوات التفكير العليا عبر تدريبات أسبوعية.", steps: "1. نشر وتوزيع أسئلة محاكاة نافس الأسبوعية.\n2. تنفيذ اختبار تجريبي محاكي منتصف كل شهر.\n3. تقديم حوافز وتكريم للفصول المتميزة.", lead: "أ. محمد عبدالصمد المعلم (منسق نافس)", cost: "200 ريال", term1: "من 2 / 4 إلى 23 / 6 / 1448 هـ", term2: "من 9 / 8 إلى 15 / 11 / 1448 هـ", progress: 85, proof: "كراسات التدريب واختبارات المحاكاة" },
            { id: 14, domain: 3, name: "برنامج المجلس الطلابي القيادي", standard: "التطور الشخصي والاجتماعي (3-2-1)", initiative: "قادة الغد", goal: "إشراك الطلاب في التنظيم والمشاركة في صناعة القرار المدرسي عبر المجلس الطلابي.", steps: "1. ترشيح طلاب من كل فصل للمجلس.\n2. عقد اجتماعات شهرية مع الإدارة.\n3. إسناد تنظيم الفعاليات للطلاب.", lead: "أ. بدر بادي الزبيدي (رائد النشاط)", cost: "400 ريال", term1: "الأحد الأول من كل شهر هجري", term2: "الأحد الأول من كل شهر هجري", progress: 60, proof: "محاضر اجتماعات قادة الغد" },
            { id: 15, domain: 3, name: "القدوة الحسنة والقيم واليوم الوطني", standard: "التطور الشخصي (3-2-1)", initiative: "قيمنا نماء.. ووطننا اعتزاز", goal: "ترسيخ الهوية الوطنية والاعتزاز بالتاريخ السعودي عبر الفعاليات والمعارض والإذاعة.", steps: "1. تشكيل لجنة الفعاليات برئاسة رائد النشاط.\n2. تحديد قيمة أسبوعية وإبرازها بالإذاعة.\n3. إقامة المعارض الفنية وتوثيق الفعاليات.", lead: "الموجه الطلابي ورائد النشاط", cost: "200 ريال", term1: "احتفال اليوم الوطني (12-13 / 4 / 1448 هـ)", term2: "احتفال يوم التأسيس (14-15 / 9 / 1448 هـ)", progress: 95, proof: "ملف الشواهد والمعارض الفنية" },
            { id: 16, domain: 3, name: "برنامج سفراء الموهبة والابتكار", standard: "التطور الشخصي (3-2-1)", initiative: "طريق الموهبة", goal: "اكتشاف الطلاب الموهوبين ورعايتهم مهارياً وتهيئتهم للمشاركات الوطنية التنافسية.", steps: "1. تطبيق مقياس الموهبة على الطلاب.\n2. إعداد برنامج رعاية أسبوعي لهم.\n3. إشراكهم بالمنافسات والمسابقات المحلية.", lead: "منسق الموهوبين بالمدرسة", cost: "200 ريال", term1: "من 9 / 4 إلى 9 / 6 / 1448 هـ", term2: "من 16 / 8 إلى 1 / 11 / 1448 هـ", progress: 40, proof: "سجل الترشيح لمقياس موهبة" },
            { id: 17, domain: 3, name: "برنامج ورتل (مسابقة الترتيل)", standard: "التطور الشخصي (3-2-1)", initiative: "ماهر بالقرآن", goal: "تشجيع وتنمية مهارات ترتيل وتجويد القرآن الكريم ودعم الأنشطة الإثرائية لحفاظ كتاب الله.", steps: "1. الإعلان عن المسابقة وشروطها.\n2. فرز وتصفية المتقدمين.\n3. التحكيم وتكريم الفائزين بطابور الصباح.", lead: "معلمو الدراسات الإسلامية ورائد النشاط", cost: "300 ريال", term1: "من 16 / 4 إلى 11 / 5 / 1448 هـ", term2: "من 2 / 9 إلى 10 / 10 / 1448 هـ", progress: 50, proof: "سجلات المتسابقين وتصفيات القرآن" },
            { id: 18, domain: 3, name: "برنامج التطوع المباشر", standard: "التطور الشخصي والصحي (3-2-1)", initiative: "سفراء التطوع المدرسي", goal: "غرس ثقافة العمل التطوعي لدى الطلاب عبر إشراكهم في المبادرات المدرسية والمجتمعية.", steps: "1. إعداد خطة البرامج التطوعية.\n2. تسجيل الطلاب الراغبين.\n3. تنفيذ المبادرات وتوثيقها.", lead: "أ. بدر الزبيدي والمرشد الصحي", cost: "500 ريال", term1: "من 23 / 4 إلى 18 / 5 / 1448 هـ", term2: "من 7 / 9 إلى 17 / 10 / 1448 هـ", progress: 45, proof: "كشوفات الساعات الطلابية التطوعية" },
            { id: 19, domain: 3, name: "برنامج باحث المستقبل", standard: "التطور الشخصي (3-2-1)", initiative: "استثمر وقتك بالبحث", goal: "تدريب الطلاب على المهارات الأساسية للبحث العلمي الميسر والتعلم الذاتي.", steps: "1. تقديم ورش مصغرة لمهارات البحث.\n2. تكليف الطلاب بمشاريع بحثية بسيطة.\n3. تقييم وعرض الأبحاث المتميزة.", lead: "أمين مصادر التعلم والمعلمون", cost: "200 ريال", term1: "من 30 / 4 إلى 2 / 6 / 1448 هـ", term2: "من 14 / 9 إلى 1 / 11 / 1448 هـ", progress: 30, proof: "ملف إنجاز أبحاث الطلاب" },

            { id: 20, domain: 4, name: "برنامج سلامتنا أولاً (فرضيات الإخلاء)", standard: "الأمن والسلامة (4-2-1)", initiative: "إخلاء آمن", goal: "رفع جاهزية وسائل السلامة وصيانتها وتدريب الجميع عبر تنفيذ 2 فرضية إخلاء ناجحة سنوياً.", steps: "1. فحص طفايات الحريق وصافرات الإنذار.\n2. تدريب الطلاب على مهارات الإخلاء.\n3. تنفيذ خطة إخلاء وهمية مفاجئة.", lead: "أ. بدر بن محمد الذروي (الأمن والسلامة)", cost: "400 ريال", term1: "الإخلاء 1 (الأربعاء 5 / 4 / 1448 هـ)", term2: "الإخلاء 2 (الأربعاء 5 / 9 / 1448 هـ)", progress: 100, proof: "تقارير فرضية الإخلاء الناجحة" },
            { id: 21, domain: 4, name: "برنامج مدرستي الخضراء الجاذبة", standard: "المبنى المدرسي (4-1-1)", initiative: "حديقتنا المستدامة", goal: "تحسين وتجميل البيئة الفيزيقية للمدرسة من خلال حملات التشجير والتخضير وأسبوع البيئة.", steps: "1. مسح وتحديد المساحات القابلة للزراعة.\n2. تنظيم حملة تطوعية طلابية لزراعة الشتلات.\n3. تفعيل أسبوع البيئة والتطوع بالمدرسة.", lead: "أ. بدر الزبيدي والكشافة", cost: "500 ريال", term1: "من 23 / 4 إلى 18 / 5 / 1448 هـ", term2: "أسبوع البيئة (17-21 / 12 / 1448 هـ)", progress: 65, proof: "صور التشجير والجداريات البيئية" },
            { id: 22, domain: 4, name: "برنامج دوري الرياضة والتميز", standard: "التطور الشخصي والصحي (3-2-1)", initiative: "بطولة التنافس الشريف", goal: "تشجيع النشاط الرياضي والصحة البدنية للطلاب ونشر الروح الرياضية عبر البطولات المدرسية.", steps: "1. إعداد جدول مباريات الدوري المدرسي.\n2. تجهيز الملاعب والأدوات الرياضية.\n3. تنظيم المباراة النهائية وتتويج الفائزين.", lead: "معلم التربية البدنية ورائد النشاط", cost: "800 ريال", term1: "من 23 / 4 إلى 9 / 6 / 1448 هـ", term2: "من 2 / 9 إلى 1 / 11 / 1448 هـ", progress: 70, proof: "جدول المباريات وصور التتويج" },
            { id: 23, domain: 4, name: "برنامج الفصل النموذجي الجاذب", standard: "المبنى المدرسي (4-1-1)", initiative: "فصلي أجمل وأنظف", goal: "إذكاء روح التنافس بين الفصول للمحافظة على الأثاث والنظافة وترشيد الموارد بنسبة 90%.", steps: "1. تشكيل لجنة تقييم الفصول أسبوعياً.\n2. منح درع الفصل النموذجي للفائز.\n3. تقديم مكافأة ترفيهية لطلاب الفصل الفائز.", lead: "رائد النشاط واللجنة التقييمية", cost: "400 ريال", term1: "تقييم أسبوعي طوال الفصل الأول", term2: "تقييم أسبوعي وتكريم شهري بالفصل الثاني", progress: 80, proof: "درع الفصل النموذجي واستمارات النظافة" },
            { id: 24, domain: 4, name: "برنامج الوصول الشامل", standard: "المبنى المدرسي (4-1-1)", initiative: "مدرسة ميسرة للجميع", goal: "تهيئة المبنى المدرسي والمرافق الفيزيقية لتسهيل حركة وتكامل الطلاب والزوار من ذوي الإعاقة.", steps: "1. مسح الاحتياجات المكانية (منحدرات، مسارات، مواقف).\n2. تركيب اللوحات الإرشادية وتهيئة المداخل.\n3. تنفيذ التعديلات البيئية الميدانية.", lead: "أ. عيد بن عايد المحمدي ومسؤول السلامة", cost: "400 ريال", term1: "من 24 / 3 إلى 20 / 4 / 1448 هـ", term2: "من 16 / 8 إلى 6 / 9 / 1448 هـ", progress: 100, proof: "صور تهيئة المنحدرات والمسارات" }
        ];

        // --- NAVIGATION CONTROLLER ---
        function switchTab(tabId) {
            document.querySelectorAll('.tab-panel').forEach(el => el.classList.add('hidden'));
            document.getElementById(`tab-${tabId}`).classList.remove('hidden');

            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('bg-emerald-600', 'text-white');
                btn.classList.add('text-slate-300', 'hover:bg-slate-800');
            });

            const activeBtn = document.getElementById(`nav-${tabId}`);
            if(activeBtn) {
                activeBtn.classList.add('bg-emerald-600', 'text-white');
                activeBtn.classList.remove('text-slate-300', 'hover:bg-slate-800');
            }
        }

        // --- SUB TABS NAVIGATION ---
        function switchSubTab(subTabId) {
            document.querySelectorAll('.subtab-panel').forEach(el => el.classList.add('hidden'));
            document.getElementById(`subtab-${subTabId}`).classList.remove('hidden');

            document.querySelectorAll('.subtab-btn').forEach(btn => {
                btn.classList.remove('bg-emerald-600', 'text-white');
                btn.classList.add('bg-slate-800', 'text-slate-300', 'hover:bg-slate-700');
            });

            const activeSubBtn = document.getElementById(`subtab-btn-${subTabId}`);
            if(activeSubBtn) {
                activeSubBtn.classList.add('bg-emerald-600', 'text-white');
                activeSubBtn.classList.remove('bg-slate-800', 'text-slate-300', 'hover:bg-slate-700');
            }
        }

        // --- SCHOOL CLASSES & STATS FUNCTIONS (DYNAMIC EDITABLE) ---
        function renderSchool1Stats() {
            const list = JSON.parse(localStorage.getItem('eid_school1_classes')) || initialSchool1Classes;
            const body = document.getElementById('school1TableBody');
            let totalCls = 0;
            let totalStd = 0;

            body.innerHTML = list.map((item, idx) => {
                totalCls += parseInt(item.classes || 0);
                totalStd += parseInt(item.students || 0);
                return `
                    <tr class="hover:bg-slate-800/40">
                        <td class="p-2.5 font-bold text-white" contenteditable="true" onblur="updateClassData('eid_school1_classes', ${idx}, 'grade', this.innerText, renderSchool1Stats)">${item.grade}</td>
                        <td class="p-2.5 text-center font-black text-emerald-400" contenteditable="true" onblur="updateClassData('eid_school1_classes', ${idx}, 'classes', this.innerText, renderSchool1Stats)">${item.classes}</td>
                        <td class="p-2.5 text-center font-black text-white" contenteditable="true" onblur="updateClassData('eid_school1_classes', ${idx}, 'students', this.innerText, renderSchool1Stats)">${item.students}</td>
                        <td class="p-2.5 text-center">
                            <button onclick="deleteClassRow('eid_school1_classes', ${idx}, renderSchool1Stats)" class="text-rose-400 hover:text-rose-300"><i class="fa-solid fa-trash"></i></button>
                        </td>
                    </tr>
                `;
            }).join('');

            document.getElementById('school1TotalClasses').innerText = `${totalCls} فصل`;
            document.getElementById('school1TotalStudents').innerText = `${totalStd} طالباً`;
        }

        function renderSchool2Stats() {
            const list = JSON.parse(localStorage.getItem('eid_school2_classes')) || initialSchool2Classes;
            const body = document.getElementById('school2TableBody');
            let totalCls = 0;
            let totalStd = 0;

            body.innerHTML = list.map((item, idx) => {
                totalCls += parseInt(item.classes || 0);
                totalStd += parseInt(item.students || 0);
                return `
                    <tr class="hover:bg-slate-800/40">
                        <td class="p-2.5 font-bold text-white" contenteditable="true" onblur="updateClassData('eid_school2_classes', ${idx}, 'grade', this.innerText, renderSchool2Stats)">${item.grade}</td>
                        <td class="p-2.5 text-center font-black text-teal-400" contenteditable="true" onblur="updateClassData('eid_school2_classes', ${idx}, 'classes', this.innerText, renderSchool2Stats)">${item.classes}</td>
                        <td class="p-2.5 text-center font-black text-white" contenteditable="true" onblur="updateClassData('eid_school2_classes', ${idx}, 'students', this.innerText, renderSchool2Stats)">${item.students}</td>
                        <td class="p-2.5 text-center">
                            <button onclick="deleteClassRow('eid_school2_classes', ${idx}, renderSchool2Stats)" class="text-rose-400 hover:text-rose-300"><i class="fa-solid fa-trash"></i></button>
                        </td>
                    </tr>
                `;
            }).join('');

            document.getElementById('school2TotalClasses').innerText = `${totalCls} فصل`;
            document.getElementById('school2TotalStudents').innerText = `${totalStd} طالباً`;
        }

        function updateClassData(key, idx, field, val, renderFn) {
            let list = JSON.parse(localStorage.getItem(key)) || (key==='eid_school1_classes'?initialSchool1Classes:initialSchool2Classes);
            if(list[idx]) {
                list[idx][field] = field==='grade'? val : (parseInt(val) || 0);
                localStorage.setItem(key, JSON.stringify(list));
                renderFn();
            }
        }

        function deleteClassRow(key, idx, renderFn) {
            let list = JSON.parse(localStorage.getItem(key)) || (key==='eid_school1_classes'?initialSchool1Classes:initialSchool2Classes);
            list.splice(idx, 1);
            localStorage.setItem(key, JSON.stringify(list));
            renderFn();
        }

        function addClassRow(key, renderFn) {
            let list = JSON.parse(localStorage.getItem(key)) || (key==='eid_school1_classes'?initialSchool1Classes:initialSchool2Classes);
            list.push({ grade: "صف جديد", classes: 1, students: 30 });
            localStorage.setItem(key, JSON.stringify(list));
            renderFn();
        }

        // --- RENDER TABLES (ADMIN, TEACHERS, ASSISTANTS) ---
        function renderAdminStaff() {
            const list = JSON.parse(localStorage.getItem('eid_admin_staff')) || initialAdminStaff;
            const body = document.getElementById('adminTableBody');
            body.innerHTML = list.map((item, idx) => `
                <tr class="hover:bg-slate-900/50">
                    <td class="p-3 font-bold text-slate-500">${idx+1}</td>
                    <td class="p-3 font-bold text-white" contenteditable="true" onblur="updateStaffData('eid_admin_staff', ${idx}, 'name', this.innerText)">${item.name}</td>
                    <td class="p-3 text-teal-400 font-bold" contenteditable="true" onblur="updateStaffData('eid_admin_staff', ${idx}, 'role', this.innerText)">${item.role}</td>
                    <td class="p-3 text-slate-300" contenteditable="true" onblur="updateStaffData('eid_admin_staff', ${idx}, 'major', this.innerText)">${item.major}</td>
                    <td class="p-3 font-bold text-emerald-400" contenteditable="true" onblur="updateStaffData('eid_admin_staff', ${idx}, 'license', this.innerText)">${item.license}</td>
                    <td class="p-3 text-center">
                        <button onclick="deleteStaffData('eid_admin_staff', ${idx}, renderAdminStaff)" class="text-rose-400 hover:text-rose-300"><i class="fa-solid fa-trash"></i></button>
                    </td>
                </tr>
            `).join('');
        }

        function renderTeachersStaff() {
            const list = JSON.parse(localStorage.getItem('eid_teachers_staff')) || initialTeachersStaff;
            const body = document.getElementById('teachersTableBody');
            body.innerHTML = list.map((item, idx) => `
                <tr class="hover:bg-slate-900/50">
                    <td class="p-3 font-bold text-slate-500">${idx+1}</td>
                    <td class="p-3 font-bold text-white" contenteditable="true" onblur="updateStaffData('eid_teachers_staff', ${idx}, 'name', this.innerText)">${item.name}</td>
                    <td class="p-3 text-slate-400" contenteditable="true" onblur="updateStaffData('eid_teachers_staff', ${idx}, 'role', this.innerText)">${item.role}</td>
                    <td class="p-3 text-emerald-400 font-bold" contenteditable="true" onblur="updateStaffData('eid_teachers_staff', ${idx}, 'major', this.innerText)">${item.major}</td>
                    <td class="p-3 font-bold text-emerald-300" contenteditable="true" onblur="updateStaffData('eid_teachers_staff', ${idx}, 'license', this.innerText)">${item.license}</td>
                    <td class="p-3 text-center">
                        <button onclick="deleteStaffData('eid_teachers_staff', ${idx}, renderTeachersStaff)" class="text-rose-400 hover:text-rose-300"><i class="fa-solid fa-trash"></i></button>
                    </td>
                </tr>
            `).join('');
        }

        function renderAssistantsStaff() {
            const list = JSON.parse(localStorage.getItem('eid_assistants_staff')) || initialAssistantsStaff;
            const body = document.getElementById('assistantsTableBody');
            body.innerHTML = list.map((item, idx) => `
                <tr class="hover:bg-slate-900/50">
                    <td class="p-3 font-bold text-slate-500">${idx+1}</td>
                    <td class="p-3 font-bold text-white" contenteditable="true" onblur="updateStaffData('eid_assistants_staff', ${idx}, 'name', this.innerText)">${item.name}</td>
                    <td class="p-3 text-brand-gold font-bold" contenteditable="true" onblur="updateStaffData('eid_assistants_staff', ${idx}, 'role', this.innerText)">${item.role}</td>
                    <td class="p-3 text-slate-300" contenteditable="true" onblur="updateStaffData('eid_assistants_staff', ${idx}, 'major', this.innerText)">${item.major}</td>
                    <td class="p-3 font-bold text-slate-400" contenteditable="true" onblur="updateStaffData('eid_assistants_staff', ${idx}, 'license', this.innerText)">${item.license}</td>
                    <td class="p-3 text-center">
                        <button onclick="deleteStaffData('eid_assistants_staff', ${idx}, renderAssistantsStaff)" class="text-rose-400 hover:text-rose-300"><i class="fa-solid fa-trash"></i></button>
                    </td>
                </tr>
            `).join('');
        }

        function updateStaffData(key, idx, field, val) {
            let list = JSON.parse(localStorage.getItem(key)) || (key==='eid_admin_staff'?initialAdminStaff:key==='eid_teachers_staff'?initialTeachersStaff:initialAssistantsStaff);
            if(list[idx]) {
                list[idx][field] = val;
                localStorage.setItem(key, JSON.stringify(list));
            }
        }

        function deleteStaffData(key, idx, renderFn) {
            let list = JSON.parse(localStorage.getItem(key)) || (key==='eid_admin_staff'?initialAdminStaff:key==='eid_teachers_staff'?initialTeachersStaff:initialAssistantsStaff);
            list.splice(idx, 1);
            localStorage.setItem(key, JSON.stringify(list));
            renderFn();
        }

        function addAdminRow() {
            let list = JSON.parse(localStorage.getItem('eid_admin_staff')) || initialAdminStaff;
            list.push({ name: "إداري جديد", role: "مسمى وظيفي", major: "تخصص", license: "حاصل على الرخصة" });
            localStorage.setItem('eid_admin_staff', JSON.stringify(list));
            renderAdminStaff();
        }

        function addTeacherRow() {
            let list = JSON.parse(localStorage.getItem('eid_teachers_staff')) || initialTeachersStaff;
            list.push({ name: "معلم جديد", role: "معلم", major: "التخصص المعتمد", license: "حاصل على الرخصة" });
            localStorage.setItem('eid_teachers_staff', JSON.stringify(list));
            renderTeachersStaff();
            populateTeacherSelect();
        }

        function addAssistantRow() {
            let list = JSON.parse(localStorage.getItem('eid_assistants_staff')) || initialAssistantsStaff;
            list.push({ name: "مساعد جديد", role: "مساعد إداري", major: "إدارة", license: "غير حاصل" });
            localStorage.setItem('eid_assistants_staff', JSON.stringify(list));
            renderAssistantsStaff();
        }

        // --- FULL PROGRAM CARDS FUNCTIONS ---
        function renderProgramCards() {
            const list = JSON.parse(localStorage.getItem('eid_programs')) || defaultPrograms;
            const filter = document.getElementById('cardDomainFilter').value;
            const container = document.getElementById('fullCardsGrid');
            container.innerHTML = '';

            const filtered = filter === 'all' ? list : list.filter(p => p.domain == filter);

            filtered.forEach(p => {
                const card = document.createElement('div');
                card.className = "bg-brand-card p-6 rounded-3xl border border-brand-border shadow-xl space-y-4 relative hover:border-emerald-500/50 transition";
                card.innerHTML = `
                    <div class="flex flex-col md:flex-row justify-between items-start border-b border-slate-800 pb-4 gap-2">
                        <div>
                            <span class="text-[10px] font-black bg-emerald-950 text-emerald-400 border border-emerald-800 px-3 py-1 rounded-full">برنامج #${p.id}</span>
                            <h3 class="font-black text-xl text-white mt-2">${p.name}</h3>
                            <p class="text-xs text-brand-gold font-bold mt-1"><i class="fa-solid fa-ribbon"></i> المعيار المرتبط: ${p.standard || 'غير محدد'}</p>
                        </div>
                        <div class="flex items-center gap-2">
                            <button onclick="editProgramCard(${p.id})" class="bg-blue-600/20 text-blue-400 hover:bg-blue-600 hover:text-white px-3 py-1.5 rounded-xl text-xs font-bold border border-blue-500/30 transition"><i class="fa-solid fa-pen-to-square"></i> تعديل البطاقة</button>
                            <button onclick="deleteProgramCard(${p.id})" class="bg-rose-600/20 text-rose-400 hover:bg-rose-600 hover:text-white px-3 py-1.5 rounded-xl text-xs font-bold border border-rose-500/30 transition"><i class="fa-solid fa-trash"></i> حذف</button>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 text-xs font-bold">
                        <div class="bg-slate-900/80 p-3.5 rounded-2xl border border-slate-800/80">
                            <span class="text-slate-400 block mb-1 font-normal"><i class="fa-solid fa-bullseye text-emerald-400"></i> المبادرة الميدانية المرتبطة:</span>
                            <span class="text-emerald-300 text-sm font-black">${p.initiative || 'لم تُحدد'}</span>
                        </div>
                        <div class="bg-slate-900/80 p-3.5 rounded-2xl border border-slate-800/80">
                            <span class="text-slate-400 block mb-1 font-normal"><i class="fa-solid fa-user-tie text-teal-400"></i> المسؤول والمشرف المباشر:</span>
                            <span class="text-white text-sm font-black">${p.lead}</span>
                        </div>
                    </div>

                    <div class="bg-slate-900 p-4 rounded-2xl border border-slate-800 text-xs space-y-2">
                        <span class="text-slate-400 font-bold block"><i class="fa-solid fa-crosshairs text-emerald-400"></i> الهدف التشغيلي للبرنامج:</span>
                        <p class="text-slate-200 leading-relaxed">${p.goal}</p>
                    </div>

                    <div class="bg-slate-900 p-4 rounded-2xl border border-slate-800 text-xs space-y-2">
                        <span class="text-slate-400 font-bold block"><i class="fa-solid fa-list-ol text-emerald-400"></i> خطوات وآلية التنفيذ الإجرائية:</span>
                        <p class="text-slate-300 whitespace-pre-line leading-relaxed font-normal">${p.steps}</p>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-3 gap-3 text-xs font-bold">
                        <div class="bg-slate-900/90 p-3 rounded-xl border border-slate-800">
                            <span class="text-brand-gold block text-[11px]"><i class="fa-solid fa-calendar"></i> تاريخ التنفيذ (ف1):</span>
                            <span class="text-slate-200 mt-1 block">${p.term1}</span>
                        </div>
                        <div class="bg-slate-900/90 p-3 rounded-xl border border-slate-800">
                            <span class="text-teal-400 block text-[11px]"><i class="fa-solid fa-calendar-check"></i> تاريخ التنفيذ (ف2):</span>
                            <span class="text-slate-200 mt-1 block">${p.term2}</span>
                        </div>
                        <div class="bg-slate-900/90 p-3 rounded-xl border border-slate-800">
                            <span class="text-purple-400 block text-[11px]"><i class="fa-solid fa-wallet"></i> الميزانية المعتمدة:</span>
                            <span class="text-slate-200 mt-1 block">${p.cost}</span>
                        </div>
                    </div>
                `;
                container.appendChild(card);
            });

            renderTrackingTable();
        }

        // --- TRACKING TABLE FUNCTIONS ---
        function renderTrackingTable() {
            const list = JSON.parse(localStorage.getItem('eid_programs')) || defaultPrograms;
            const term1Body = document.getElementById('term1ProgramsTableBody');
            const term2Body = document.getElementById('term2IndicatorsTableBody');

            let completed = 0;
            let totalProg = 0;

            list.forEach((p, idx) => {
                totalProg += p.progress;
                if(p.progress === 100) completed++;

                const progressControl = `
                    <div class="flex items-center gap-2">
                        <input type="range" min="0" max="100" value="${p.progress}" onchange="updateProgressValue(${p.id}, this.value)" class="w-full accent-emerald-500 bg-slate-800 h-2 rounded-lg cursor-pointer">
                        <span class="font-bold text-emerald-400 w-10 text-left">${p.progress}%</span>
                    </div>`;

                if(term1Body) {
                    const term1Row = document.createElement('tr');
                    term1Row.className = "hover:bg-slate-900/50 transition";
                    term1Row.innerHTML = `
                    <td class="p-3 font-bold text-slate-500">${idx+1}</td>
                    <td class="p-3 font-bold text-white">${p.name}</td>
                    <td class="p-3 text-emerald-400 font-bold">${p.lead}</td>
                    <td class="p-3 text-slate-300 text-[11px]">${p.term1}</td>
                    <td class="p-3 text-slate-400 text-[11px]">${p.proof}</td>
                    <td class="p-3">${progressControl}</td>`;
                    term1Body.appendChild(term1Row);
                }

                if(term2Body) {
                    const term2Row = document.createElement('tr');
                    term2Row.className = "hover:bg-slate-900/50 transition";
                    term2Row.innerHTML = `
                    <td class="p-3 font-bold text-slate-500">${idx+1}</td>
                    <td class="p-3 font-bold text-white">${p.name}</td>
                    <td class="p-3 text-blue-300 text-[11px]">${p.goal}</td>
                    <td class="p-3 text-slate-300 text-[11px]">${p.term2}</td>
                    <td class="p-3 text-slate-400 text-[11px]">${p.proof}</td>
                    <td class="p-3">${progressControl}</td>`;
                    term2Body.appendChild(term2Row);
                }
            });

            const avg = list.length ? Math.round(totalProg / list.length) : 0;
            const overallProgress = document.getElementById('overallProgress');
            const overallBar = document.getElementById('overallBar');
            const completedCount = document.getElementById('completedCount');
            const totalProgramsCount = document.getElementById('totalProgramsCount');
            const term2OverallProgress = document.getElementById('term2OverallProgress');
            const term2CompletedCount = document.getElementById('term2CompletedCount');
            const term2TotalCount = document.getElementById('term2TotalCount');

            if(overallProgress) overallProgress.innerText = `${avg}%`;
            if(overallBar) overallBar.style.width = `${avg}%`;
            if(completedCount) completedCount.innerText = `${completed} / ${list.length}`;
            if(totalProgramsCount) totalProgramsCount.innerText = `${list.length} برنامجاً`;
            if(term2OverallProgress) term2OverallProgress.innerText = `${avg}%`;
            if(term2CompletedCount) term2CompletedCount.innerText = completed;
            if(term2TotalCount) term2TotalCount.innerText = list.length;
        }

        function updateProgressValue(id, val) {
            let list = JSON.parse(localStorage.getItem('eid_programs')) || defaultPrograms;
            const item = list.find(p => p.id === id);
            if(item) {
                item.progress = parseInt(val);
                localStorage.setItem('eid_programs', JSON.stringify(list));
                renderTrackingTable();
            }
        }

        // --- EXTERNAL FILES MANAGEMENT FUNCTIONS ---
        function getFileFolders() {
            return JSON.parse(localStorage.getItem('eid_file_folders')) || ['غير مصنف'];
        }

        function createFileFolder() {
            const input = document.getElementById('newFolderName');
            const name = input.value.trim();
            if(!name) {
                alert('اكتب اسم المجلد أولاً.');
                return;
            }

            const folders = getFileFolders();
            if(folders.includes(name)) {
                alert('هذا المجلد موجود مسبقاً.');
                return;
            }

            folders.push(name);
            localStorage.setItem('eid_file_folders', JSON.stringify(folders));
            input.value = '';
            renderExternalFiles();
        }

        function deleteFileFolder(name) {
            if(name === 'غير مصنف') return;
            if(!confirm(`سيتم نقل الملفات داخل مجلد "${name}" إلى "غير مصنف". هل تريد حذف المجلد؟`)) return;

            const folders = getFileFolders().filter(folder => folder !== name);
            const filesList = JSON.parse(localStorage.getItem('eid_files')) || [];
            filesList.forEach(file => {
                if((file.folder || 'غير مصنف') === name) file.folder = 'غير مصنف';
            });
            localStorage.setItem('eid_file_folders', JSON.stringify(folders));
            localStorage.setItem('eid_files', JSON.stringify(filesList));
            renderExternalFiles();
        }

        function uploadExternalFile(e) {
            const file = e.target.files[0];
            if(!file) return;

            const namePrompt = prompt("أدخل اسماً أو عنواناً للملف الخارجي المرفق:", file.name);
            if(!namePrompt) return;

            const reader = new FileReader();
            reader.onload = function(event) {
                let filesList = JSON.parse(localStorage.getItem('eid_files')) || [];
                filesList.push({
                    id: Date.now(),
                    title: namePrompt,
                    fileName: file.name,
                    folder: document.getElementById('fileUploadFolder').value || 'غير مصنف',
                    size: (file.size / 1024).toFixed(1) + ' KB',
                    date: new Date().toLocaleDateString('ar-SA'),
                    data: event.target.result
                });
                localStorage.setItem('eid_files', JSON.stringify(filesList));
                e.target.value = '';
                renderExternalFiles();
            };
            reader.readAsDataURL(file);
        }

        function renderExternalFiles() {
            const folders = getFileFolders();
            const filesList = (JSON.parse(localStorage.getItem('eid_files')) || []).map(file => ({
                ...file,
                folder: file.folder || 'غير مصنف'
            }));
            const container = document.getElementById('filesContainer');
            const filter = document.getElementById('fileFolderFilter');
            const uploadFolder = document.getElementById('fileUploadFolder');
            const selectedFolder = filter.value;

            filter.innerHTML = '<option value="all">عرض جميع المجلدات</option>' + folders.map(folder => `<option value="${folder}">${folder}</option>`).join('');
            uploadFolder.innerHTML = folders.map(folder => `<option value="${folder}">رفع إلى: ${folder}</option>`).join('');
            filter.value = selectedFolder === 'all' || folders.includes(selectedFolder) ? selectedFolder : 'all';
            if(!folders.includes(uploadFolder.value)) uploadFolder.value = 'غير مصنف';

            container.innerHTML = '';

            const visibleFiles = selectedFolder === 'all' ? filesList : filesList.filter(file => file.folder === selectedFolder);

            const foldersBar = `
                <div class="col-span-full flex flex-wrap gap-2 items-center mb-1">
                    ${folders.map(folder => `
                        <div class="flex items-center gap-2 bg-slate-900 border border-slate-800 rounded-xl px-3 py-2 text-xs font-bold text-slate-300">
                            <i class="fa-solid fa-folder text-amber-400"></i><span>${folder}</span>
                            ${folder !== 'غير مصنف' ? `<button onclick="deleteFileFolder('${folder.replace(/'/g, "\\'")}')" class="text-rose-400 hover:text-rose-300" title="حذف المجلد"><i class="fa-solid fa-xmark"></i></button>` : ''}
                        </div>
                    `).join('')}
                </div>`;
            container.innerHTML = foldersBar;

            if(visibleFiles.length === 0) {
                container.innerHTML = `
                    ${foldersBar}
                    <div class="col-span-full p-8 text-center text-slate-500 bg-slate-900/50 rounded-2xl border border-slate-800 font-bold">
                        لا توجد ملفات في هذا المجلد حتى الآن. اختر مجلدًا ثم ارفع ملفًا جديدًا.
                    </div>
                `;
                return;
            }

            visibleFiles.forEach((f) => {
                const card = document.createElement('div');
                card.className = "bg-brand-card p-5 rounded-2xl border border-brand-border space-y-3 flex flex-col justify-between shadow-xl";
                card.innerHTML = `
                    <div class="space-y-2">
                        <div class="flex justify-between items-start">
                            <div class="w-10 h-10 rounded-xl bg-amber-500/10 text-amber-400 flex items-center justify-center font-bold text-lg">
                                <i class="fa-solid fa-file-pdf"></i>
                            </div>
                            <button onclick="deleteExternalFile(${f.id})" class="text-rose-400 hover:text-rose-300 text-xs font-bold p-1"><i class="fa-solid fa-trash"></i></button>
                        </div>
                        <h4 class="font-black text-white text-sm line-clamp-1">${f.title}</h4>
                        <p class="text-[11px] text-amber-400 font-bold"><i class="fa-solid fa-folder"></i> ${f.folder}</p>
                        <p class="text-[11px] text-slate-400">${f.fileName} • ${f.size}</p>
                    </div>
                    <div class="pt-3 border-t border-slate-800 flex justify-between items-center text-xs">
                        <span class="text-[10px] text-slate-500 font-bold">${f.date}</span>
                        <a href="${f.data}" download="${f.fileName}" class="bg-emerald-600 hover:bg-emerald-500 text-white font-bold px-3 py-1.5 rounded-xl transition flex items-center gap-1.5">
                            <i class="fa-solid fa-download"></i> تحميل الملف
                        </a>
                    </div>
                `;
                container.appendChild(card);
            });
        }

        function deleteExternalFile(id) {
            if(confirm("هل أنت تأكد من رغبتك في حذف هذا الملف؟")) {
                let filesList = JSON.parse(localStorage.getItem('eid_files')) || [];
                filesList = filesList.filter(f => f.id !== id);
                localStorage.setItem('eid_files', JSON.stringify(filesList));
                renderExternalFiles();
            }
        }

        // --- PROGRAM MODAL FUNCTIONS ---
        function openProgramModal(id = null) {
            document.getElementById('programModal').classList.remove('hidden');
            if(id) {
                const list = JSON.parse(localStorage.getItem('eid_programs')) || defaultPrograms;
                const p = list.find(item => item.id === id);
                if(p) {
                    document.getElementById('modalTitle').innerText = "تعديل بطاقة البرنامج التشغيلي";
                    document.getElementById('progModalId').value = p.id;
                    document.getElementById('progModalName').value = p.name;
                    document.getElementById('progModalDomain').value = p.domain;
                    document.getElementById('progModalStandard').value = p.standard || '';
                    document.getElementById('progModalInitiative').value = p.initiative || '';
                    document.getElementById('progModalGoal').value = p.goal || '';
                    document.getElementById('progModalSteps').value = p.steps || '';
                    document.getElementById('progModalLead').value = p.lead || '';
                    document.getElementById('progModalCost').value = p.cost || '0 ريال';
                    document.getElementById('progModalTerm1').value = p.term1 || '';
                    document.getElementById('progModalTerm2').value = p.term2 || '';
                }
            } else {
                document.getElementById('modalTitle').innerText = "إضافة بطاقة برنامج تشغيلي جديد";
                document.getElementById('progModalId').value = '';
                document.getElementById('progModalName').value = '';
                document.getElementById('progModalStandard').value = '';
                document.getElementById('progModalInitiative').value = '';
                document.getElementById('progModalGoal').value = '';
                document.getElementById('progModalSteps').value = '';
                document.getElementById('progModalLead').value = '';
                document.getElementById('progModalCost').value = '200 ريال';
                document.getElementById('progModalTerm1').value = '';
                document.getElementById('progModalTerm2').value = '';
            }
        }

        function closeProgramModal() { document.getElementById('programModal').classList.add('hidden'); }

        function saveProgramModal() {
            let list = JSON.parse(localStorage.getItem('eid_programs')) || defaultPrograms;
            const id = document.getElementById('progModalId').value;

            const newCard = {
                id: id ? parseInt(id) : Date.now(),
                domain: parseInt(document.getElementById('progModalDomain').value),
                name: document.getElementById('progModalName').value || 'برنامج جديد',
                standard: document.getElementById('progModalStandard').value,
                initiative: document.getElementById('progModalInitiative').value,
                goal: document.getElementById('progModalGoal').value,
                steps: document.getElementById('progModalSteps').value,
                lead: document.getElementById('progModalLead').value,
                cost: document.getElementById('progModalCost').value,
                term1: document.getElementById('progModalTerm1').value,
                term2: document.getElementById('progModalTerm2').value,
                progress: 0,
                proof: "توثيق الشواهد المعتمدة"
            };

            if(id) {
                const idx = list.findIndex(p => p.id === parseInt(id));
                if(idx !== -1) { newCard.progress = list[idx].progress; list[idx] = newCard; }
            } else {
                list.push(newCard);
            }

            localStorage.setItem('eid_programs', JSON.stringify(list));
            closeProgramModal();
            renderProgramCards();
        }

        function editProgramCard(id) { openProgramModal(id); }

        function deleteProgramCard(id) {
            if(confirm("هل أنت تأكد من رغبتك في حذف بطاقة هذا البرنامج؟")) {
                let list = JSON.parse(localStorage.getItem('eid_programs')) || defaultPrograms;
                list = list.filter(p => p.id !== id);
                localStorage.setItem('eid_programs', JSON.stringify(list));
                renderProgramCards();
            }
        }

        // --- COMMITTEES FUNCTIONS ---
        function renderCommittees() {
            const committees = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
            const container = document.getElementById('committeesContainer');
            container.innerHTML = '';

            committees.forEach((c) => {
                const box = document.createElement('div');
                box.className = "bg-slate-900 p-5 rounded-2xl border border-slate-800 space-y-4";
                box.innerHTML = `
                    <div class="flex justify-between items-center border-b border-slate-800 pb-3">
                        <h4 class="font-black text-brand-gold text-base" contenteditable="true" onblur="updateCommitteeTitle(${c.id}, this.innerText)">${c.title}</h4>
                        <div class="flex gap-2">
                            <button onclick="addMemberToCommittee(${c.id})" class="bg-slate-800 hover:bg-slate-700 text-emerald-400 px-3 py-1 rounded-lg text-xs font-bold border border-slate-700">+ إضافة عضو</button>
                            <button onclick="deleteCommittee(${c.id})" class="text-rose-400 hover:text-rose-300 text-xs font-bold px-2"><i class="fa-solid fa-trash"></i></button>
                        </div>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="w-full text-xs text-right border-collapse">
                            <thead>
                                <tr class="bg-slate-800/60 text-slate-400 font-bold">
                                    <th class="p-2">الاسم الرباعي</th>
                                    <th class="p-2">الصفة / الموقع</th>
                                    <th class="p-2">المهام والتكليف باللجنة</th>
                                    <th class="p-2 text-center">حذف</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-slate-800 text-slate-300">
                                ${c.members.map(m => `
                                    <tr>
                                        <td class="p-2 font-bold text-white" contenteditable="true" onblur="updateMember(${c.id}, ${m.id}, 'name', this.innerText)">${m.name}</td>
                                        <td class="p-2 text-emerald-400 font-bold" contenteditable="true" onblur="updateMember(${c.id}, ${m.id}, 'role', this.innerText)">${m.role}</td>
                                        <td class="p-2 text-slate-300" contenteditable="true" onblur="updateMember(${c.id}, ${m.id}, 'task', this.innerText)">${m.task}</td>
                                        <td class="p-2 text-center">
                                            <button onclick="deleteMember(${c.id},${m.id})" class="text-rose-400 hover:text-rose-300"><i class="fa-solid fa-trash"></i></button>
                                        </td>
                                    </tr>
                                `).join('')}
                            </tbody>
                        </table>
                    </div>
                `;
                container.appendChild(box);
            });
        }

        function updateCommitteeTitle(cId, newTitle) {
            let list = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
            const item = list.find(c => c.id === cId);
            if(item) { item.title = newTitle; localStorage.setItem('eid_4committees', JSON.stringify(list)); }
        }

        function updateMember(cId, mId, field, val) {
            let list = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
            const com = list.find(c => c.id === cId);
            if(com) {
                const mem = com.members.find(m => m.id === mId);
                if(mem) { mem[field] = val; localStorage.setItem('eid_4committees', JSON.stringify(list)); }
            }
        }

        function addMemberToCommittee(cId) {
            let list = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
            const com = list.find(c => c.id === cId);
            if(com) {
                com.members.push({ id: Date.now(), name: "عضو جديد", role: "عضو باللجنة", task: "إسناد مهمة إجرائية" });
                localStorage.setItem('eid_4committees', JSON.stringify(list));
                renderCommittees();
            }
        }

        function deleteMember(cId, mId) {
            let list = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
            const com = list.find(c => c.id === cId);
            if(com) {
                com.members = com.members.filter(m => m.id !== mId);
                localStorage.setItem('eid_4committees', JSON.stringify(list));
                renderCommittees();
            }
        }

        function addNewCommittee() {
            let list = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
            list.push({
                id: Date.now(),
                title: `${list.length + 1}. لجنة مدرسية جديدة`,
                members: [{ id: Date.now()+1, name: "اسم المسؤول", role: "رئيس اللجنة", task: "إدارة وتخطيط" }]
            });
            localStorage.setItem('eid_4committees', JSON.stringify(list));
            renderCommittees();
        }

        function deleteCommittee(cId) {
            if(confirm("هل أنت تأكد من حذف هذه اللجنة؟")) {
                let list = JSON.parse(localStorage.getItem('eid_4committees')) || defaultCommitteesData;
                list = list.filter(c => c.id !== cId);
                localStorage.setItem('eid_4committees', JSON.stringify(list));
                renderCommittees();
            }
        }

        window.onload = function() {
            if(!localStorage.getItem('eid_programs')) {
                localStorage.setItem('eid_programs', JSON.stringify(defaultPrograms));
            }
            renderProgramCards();
            renderCommittees();
            renderSchool1Stats();
            renderSchool2Stats();
            renderAdminStaff();
            renderTeachersStaff();
            renderAssistantsStaff();
            renderExternalFiles();

            // Schedules Renders
            populateTeacherSelect();
            renderClassIndividualSchedule();
            renderWaitingSchedule();
            renderSupervisionSchedule();
            renderMonawabaSchedule();
        };
    </script>
</body>
</html>
