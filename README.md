<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>한글 기초 1 | Basic Korean 1</title>
  <style>
    :root {
      --ink: #253247;
      --muted: #66758a;
      --line: #d8e1ec;
      --paper: #ffffff;
      --soft: #f5f8fb;
      --blue: #2f6f88;
      --blue-dark: #1f5267;
      --blue-soft: #e6f3f7;
      --warm: #fff6ea;
      --gold: #a5671f;
      --green: #edf7ef;
      --green-dark: #2f6b43;
      --shadow: 0 18px 40px rgba(37, 50, 71, 0.12);
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: Arial, "Apple SD Gothic Neo", "Noto Sans KR", sans-serif;
      color: var(--ink);
      background:
        radial-gradient(circle at top left, rgba(47, 111, 136, 0.12), transparent 34rem),
        linear-gradient(180deg, #f8fbfd 0%, #eef5f7 46%, #fafafa 100%);
      line-height: 1.55;
    }

    header {
      color: white;
      background:
        linear-gradient(135deg, rgba(31, 82, 103, 0.96), rgba(47, 111, 136, 0.88)),
        repeating-linear-gradient(90deg, transparent 0 26px, rgba(255,255,255,0.08) 26px 27px);
      padding: 50px 20px 42px;
    }

    .wrap {
      width: min(1120px, calc(100% - 36px));
      margin: 0 auto;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.35fr 0.65fr;
      gap: 22px;
      align-items: end;
    }

    .eyebrow {
      display: inline-flex;
      padding: 6px 12px;
      border: 1px solid rgba(255,255,255,0.44);
      border-radius: 999px;
      background: rgba(255,255,255,0.13);
      font-size: 0.92rem;
      font-weight: 700;
    }

    h1 {
      margin: 16px 0 10px;
      font-size: clamp(2.2rem, 5.8vw, 4.7rem);
      line-height: 1.03;
      letter-spacing: 0;
    }

    .hero-copy {
      max-width: 820px;
      margin: 0;
      font-size: 1.08rem;
      color: rgba(255,255,255,0.94);
    }

    .term-card {
      background: rgba(255,255,255,0.14);
      border: 1px solid rgba(255,255,255,0.28);
      border-radius: 8px;
      padding: 18px;
    }

    .term-card h2 {
      margin: 0 0 10px;
      font-size: 1.05rem;
    }

    .term-list {
      list-style: none;
      margin: 0;
      padding: 0;
      display: grid;
      gap: 8px;
      font-size: 0.95rem;
    }

    main {
      margin: -22px auto 56px;
    }

    .cards {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
      margin-bottom: 18px;
    }

    .card,
    .tabs-shell {
      background: var(--paper);
      border: 1px solid var(--line);
      border-radius: 8px;
      box-shadow: var(--shadow);
    }

    .card {
      padding: 22px;
    }

    .card h2,
    .lesson h2 {
      margin: 0 0 10px;
      font-size: 1.38rem;
      line-height: 1.22;
    }

    .card p {
      margin: 0 0 12px;
      color: var(--muted);
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 14px;
    }

    .pill {
      display: inline-flex;
      align-items: center;
      min-height: 32px;
      padding: 6px 11px;
      border-radius: 999px;
      background: var(--blue-soft);
      color: var(--blue-dark);
      font-weight: 700;
      font-size: 0.92rem;
    }

    .routine {
      list-style: none;
      margin: 0;
      padding: 0;
      display: grid;
      gap: 8px;
    }

    .routine li {
      display: grid;
      grid-template-columns: 32px 1fr;
      gap: 10px;
      align-items: start;
    }

    .number {
      width: 28px;
      height: 28px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: var(--warm);
      color: var(--gold);
      font-weight: 800;
    }

    .tabs-shell {
      overflow: hidden;
    }

    .tabs-header {
      padding: 18px 18px 0;
      border-bottom: 1px solid var(--line);
      background: #fbfdfe;
    }

    .tabs-title {
      display: flex;
      justify-content: space-between;
      gap: 12px;
      align-items: center;
      margin-bottom: 12px;
    }

    .tabs-title h2 {
      margin: 0;
      font-size: 1.35rem;
    }

    .small-note {
      color: var(--muted);
      font-size: 0.93rem;
    }

    .tabs {
      display: flex;
      gap: 8px;
      overflow-x: auto;
      padding: 0 0 14px;
      scrollbar-width: thin;
    }

    .tab {
      flex: 0 0 auto;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: white;
      color: var(--ink);
      padding: 10px 13px;
      font: inherit;
      font-weight: 800;
      cursor: pointer;
    }

    .tab[aria-selected="true"] {
      border-color: var(--blue);
      background: var(--blue);
      color: white;
    }

    .lesson {
      padding: 24px;
    }

    .lesson-head {
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 16px;
      align-items: start;
      margin-bottom: 16px;
    }

    .week-tag {
      display: inline-flex;
      padding: 7px 12px;
      border-radius: 999px;
      background: var(--warm);
      color: var(--gold);
      font-weight: 800;
      white-space: nowrap;
    }

    .date {
      color: var(--muted);
      margin: 0;
    }

    .lesson-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }

    .section {
      border: 1px solid var(--line);
      border-radius: 8px;
      padding: 16px;
      background: white;
    }

    .section.full {
      grid-column: 1 / -1;
    }

    .section h3 {
      margin: 0 0 10px;
      color: var(--blue-dark);
      font-size: 1.04rem;
    }

    .ko-en {
      display: grid;
      gap: 12px;
    }

    .lang-block {
      border-left: 4px solid var(--blue);
      padding-left: 12px;
    }

    .lang-block strong {
      display: inline-block;
      margin-bottom: 4px;
      color: var(--blue-dark);
    }

    .parent {
      background: var(--blue-soft);
      border-color: #c7e0e8;
    }

    .homework {
      background: var(--warm);
      border-color: #edd5b8;
    }

    .standards {
      background: var(--green);
      border-color: #c9e6d0;
    }

    ul, ol {
      margin: 0;
      padding-left: 20px;
    }

    li + li {
      margin-top: 5px;
    }

    .actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 16px;
    }

    button.action {
      border: 1px solid var(--blue);
      border-radius: 999px;
      background: white;
      color: var(--blue-dark);
      padding: 9px 13px;
      font: inherit;
      font-weight: 800;
      cursor: pointer;
    }

    button.action.primary {
      background: var(--blue);
      color: white;
    }

    button.action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    footer {
      width: min(1120px, calc(100% - 36px));
      margin: 18px auto 0;
      color: var(--muted);
      font-size: 0.95rem;
    }

    @media (max-width: 860px) {
      .hero-grid,
      .cards,
      .lesson-grid,
      .lesson-head {
        grid-template-columns: 1fr;
      }

      header {
        padding-top: 36px;
      }

      .tabs-title {
        display: block;
      }
    }

    @media print {
      body { background: white; }
      header, .cards, .tabs-header, .actions, footer { display: none; }
      main, .wrap { width: auto; margin: 0; }
      .tabs-shell, .section { box-shadow: none; border-color: #bbb; }
      .lesson { display: block !important; break-after: page; }
    }
  </style>
</head>
<body>
  <header>
    <div class="wrap hero-grid">
      <div>
        <span class="eyebrow">2026 Fall 뿌리교육 프로그램</span>
        <h1>한글 기초 1<br>Basic Korean 1</h1>
        <p class="hero-copy">A bilingual parent website for weekly lesson summaries, homework, activities, and family guidance for Korean Basic 1.</p>
      </div>
      <aside class="term-card" aria-label="Course information">
        <h2>Course Information</h2>
        <ul class="term-list">
          <li><strong>Term:</strong> 2026. 8. 22 - 12. 12</li>
          <li><strong>Schedule:</strong> 15 weeks</li>
          <li><strong>No class:</strong> 10/17 TOPIK, 11/28 Thanksgiving</li>
          <li><strong>Level:</strong> Novice Low</li>
          <li><strong>Instructor:</strong> 미정 코나코브</li>
        </ul>
      </aside>
    </div>
  </header>

  <main class="wrap">
    <section class="cards" aria-label="Course overview">
      <article class="card">
        <h2>수업 목적 | Course Objectives</h2>
        <p>본 과정은 한국어를 처음 접하는 모어 및 비모어 학습자를 위한 놀이 기반, 표준 정렬 한국어 입문 과정입니다.</p>
        <p>This play-based introductory course supports both heritage and non-heritage Korean learners through language, culture, technology, and identity-centered learning.</p>
        <div class="pill-row">
          <span class="pill">ACTFL Standards</span>
          <span class="pill">California World Languages</span>
          <span class="pill">VINU Coding Robot</span>
          <span class="pill">Project-Based Learning</span>
          <span class="pill">Ethnic Studies</span>
        </div>
      </article>

      <article class="card">
        <h2>Weekly Learning Rhythm</h2>
        <ol class="routine">
          <li><span class="number">1</span><span>Greeting, attendance, and warm community opening</span></li>
          <li><span class="number">2</span><span>Review of previous Hangul sounds and words</span></li>
          <li><span class="number">3</span><span>New textbook lesson, sound, or vocabulary focus</span></li>
          <li><span class="number">4</span><span>Hands-on practice with workbook, cards, writing, or reading</span></li>
          <li><span class="number">5</span><span>Culture, story, song, STEAM, art, or VINU activity</span></li>
          <li><span class="number">6</span><span>Closing review and home practice reminder</span></li>
        </ol>
      </article>
    </section>

    <section class="tabs-shell" aria-label="15-week syllabus">
      <div class="tabs-header">
        <div class="tabs-title">
          <h2>15주 수업 지도안 & 학부모 공지사항</h2>
          <span class="small-note">Choose a week to view the parent update.</span>
        </div>
        <div class="tabs" id="tabs" role="tablist" aria-label="Weekly tabs"></div>
      </div>
      <div id="lesson-container"></div>
    </section>
  </main>

  <footer>
    <p><strong>Family practice tip:</strong> Short and joyful practice is best. Five to ten minutes with songs, word cards, workbook pages, or a simple Korean greeting can make a meaningful difference.</p>
  </footer>

  <script>
    const weeks = [
      {
        week: 1, date: "8/22", title: "Orientation and Hangul Chart",
        summaryKo: "첫 시간 오리엔테이션 및 자기 이름 카드 만들기. 기본 모음 10개와 자음 14개 한글 차트 알아보기.",
        summaryEn: "First-day orientation and creating personalized name cards. Learning 10 basic vowels and 14 basic consonants using the Hangul chart.",
        activityKo: "모음/자음 소개 영상 시청 및 이름 카드 활동",
        activityEn: "Introductory vowel/consonant video and name card activity",
        language: ["아, 야, 어, 여, 오, 요, 우, 유, 으, 이", "가, 나, 다, 라, 마, 바, 사, 아, 자, 차, 카, 타, 파, 하", "안녕하세요"],
        homeworkKo: "기본 모음(아-이)과 기본 자음(가-하)을 외울 수 있도록 격려해 주세요.",
        homeworkEn: "Please help your child memorize the basic vowels and consonant syllables.",
        parent: "Students began Korean Basic 1 by learning the Hangul chart and making name cards."
      },
      {
        week: 2, date: "8/29", title: "Vowel Review and Articulation",
        summaryKo: "조음 위치와 발성 원리에 따라 자음 ㄱ, ㄴ, ㅁ, ㅅ, ㅇ을 익히고 교과서 1과 p.28-37을 학습합니다.",
        summaryEn: "Students learn consonants ㄱ, ㄴ, ㅁ, ㅅ, ㅇ based on articulation and study textbook Lesson 1, pp. 28-37.",
        activityKo: "풍선 아트 활용 자음 모양 만들기",
        activityEn: "Creating consonant shapes with balloon art",
        language: ["ㄱ, ㄴ", "ㅁ", "ㅅ", "ㅇ"],
        homeworkKo: "익힘책 1과 p.6-11을 지도해 주세요. 두꺼운 주교재는 교실에 보관하고 얇은 익힘책으로 복습합니다.",
        homeworkEn: "Please guide your child through Workbook pp. 6-11. The main textbook is kept in class; use the workbook at home.",
        parent: "Students connected Korean sounds to mouth position and letter shape."
      },
      {
        week: 3, date: "9/5", title: "Lesson 2 and Simple Conversation",
        summaryKo: "1과 단어(엄마, 아빠, 고양이, 강아지 등)를 복습하고 2과 교과서 p.38-47을 학습합니다.",
        summaryEn: "Students review Lesson 1 words such as mom, dad, cat, and puppy, then cover Lesson 2, pp. 38-47.",
        activityKo: "AI 블록 코딩 로봇 VINU 도입 및 동화책 「엉망진창 로드니의 방」 읽기",
        activityEn: "Introducing the VINU coding robot and reading the storybook Rodney's Messy Room",
        language: ["엄마, 아빠, 고양이, 강아지", "이름이 뭐예요?", "비누예요", "___이에요/예요"],
        homeworkKo: "익힘책 2과 읽고 쓰기 p.12-17을 완료합니다.",
        homeworkEn: "Homework: Workbook Lesson 2 Reading and Writing, pp. 12-17.",
        parent: "Try asking 이름이 뭐예요? at home and let your child answer in Korean."
      },
      {
        week: 4, date: "9/12", title: "Lessons 2-3 Review and Music Coding",
        summaryKo: "교과서 2과 및 3과를 종합 복습합니다.",
        summaryEn: "Students complete a comprehensive review of textbook Lessons 2 and 3.",
        activityKo: "VINU로 계이름 도레미파솔라시도를 배우고 녹음하기, 「갈색 곰아, 갈색 곰아」 독서 활동",
        activityEn: "Learning Korean solfege with VINU and reading Brown Bear, Brown Bear, What Do You See?",
        language: ["도, 레, 미, 파, 솔, 라, 시, 도", "Review words from Lessons 2-3"],
        homeworkKo: "수업 시간에 만든 단어 메모리 카드로 가족과 함께 놀이식 단어 게임을 해 주세요.",
        homeworkEn: "Please play a vocabulary memory game at home using the cards students made in class.",
        parent: "Playful review helps children remember words with less pressure."
      },
      {
        week: 5, date: "9/19", title: "ㅗ, ㅛ and Korean American History",
        summaryKo: "ㄱ, ㄴ, ㄷ, ㄹ, ㅁ, ㅇ 연계 단어와 4과 모음 ㅗ, ㅛ를 학습하고 기본 문장 쓰기를 연습합니다.",
        summaryEn: "Students learn words connected to ㄱ, ㄴ, ㄷ, ㄹ, ㅁ, ㅇ and Lesson 4 vowels ㅗ and ㅛ, then practice basic sentence writing.",
        activityKo: "미주 한국 이민 역사와 한인 정체성 토론, VINU로 동요 나비야 컬러 코딩",
        activityEn: "Korean American immigration history, identity discussion, and color-coding Nabiya with VINU",
        language: ["두루미, 거미, 오리, 너구리, 모기", "ㅗ, ㅛ", "안녕하세요", "반가워요", "이름이 뭐예요"],
        homeworkKo: "필수 문장 패턴을 2회씩 쓰고 익힘책 p.18-23을 완료합니다. 가족과 우정의 종각 방문을 추천합니다.",
        homeworkEn: "Write key phrases twice and complete Workbook pp. 18-23. A family visit to the Korean Friendship Bell is recommended.",
        parent: "This week connects Korean language with Korean American history and local community heritage."
      },
      {
        week: 6, date: "9/26", title: "ㅂ, Spring Picnic, and Chuseok",
        summaryKo: "자음 ㅂ과 Ch.5 봄소풍 어휘 및 문형을 학습합니다.",
        summaryEn: "Students learn consonant ㅂ and Chapter 5 Spring Picnic vocabulary and language patterns.",
        activityKo: "추석, 한복, 추석 감사 카드, 딱지접기, VINU 학교종 색상 매칭",
        activityEn: "Chuseok, hanbok, gratitude cards, ttakji folding, and VINU School Bell color-note matching",
        language: ["ㅂ", "봄소풍", "추석", "한복", "딱지"],
        homeworkKo: "익힘책 p.24-29를 완료하고 추석 카드와 딱지를 가족과 함께 공유해 보세요.",
        homeworkEn: "Complete Workbook pp. 24-29 and let your child share the Chuseok card and ttakji game with family.",
        parent: "Students experienced Korean holiday culture through language, art, and play."
      },
      {
        week: 7, date: "10/3", title: "ㅈ, Buses and Taxis",
        summaryKo: "자음 ㅈ 시각 자료를 보고 교과서 6과 버스와 택시 및 7과 종합 문제로 복습합니다.",
        summaryEn: "Students study consonant ㅈ, Chapter 6 Buses and Taxis, and Chapter 7 review exercises.",
        activityKo: "전통 팽이치기 게임 활동",
        activityEn: "Traditional spinning top play activity",
        language: ["ㅈ", "버스", "택시", "기본 모음 복습"],
        homeworkKo: "익힘책 p.30-35를 완료합니다. 다음 주에는 독도 교육 프로젝트를 진행합니다.",
        homeworkEn: "Complete Workbook pp. 30-35. Next week we will begin a Dokdo education project.",
        parent: "Thank you for supporting hands-on cultural learning."
      },
      {
        week: 8, date: "10/10", title: "ㅊ, Train Travel, Taegukgi, and Dokdo",
        summaryKo: "자음 ㅊ과 Ch.8 즐거운 기차 여행을 학습하고 ㄱ, ㄴ, ㄷ 시작 단어를 강화합니다.",
        summaryEn: "Students learn consonant ㅊ, Chapter 8 A Fun Train Trip, and strengthen words beginning with ㄱ, ㄴ, ㄷ.",
        activityKo: "태극기 컬러링, 3.1운동 이해, 대한민국 지도에서 독도 찾기, 독도 3D 퍼즐",
        activityEn: "Taegukgi coloring, March 1st Movement introduction, locating Dokdo on the map, and Dokdo 3D puzzle",
        language: ["ㅊ", "태극기", "독도", "ㄱ, ㄴ, ㄷ words"],
        homeworkKo: "익힘책 p.36-41을 완료합니다. 3D 독도 퍼즐은 필요하면 가정에서 도와주세요. 10/17은 TOPIK 시험으로 휴강입니다.",
        homeworkEn: "Complete Workbook pp. 36-41. Please help with the Dokdo puzzle if needed. No class on 10/17 due to TOPIK.",
        parent: "This week includes Korean history, geography, and identity learning in an age-appropriate way."
      },
      {
        week: 9, date: "10/24", title: "ㅁ, ㅂ, ㅅ, ㅈ Review and Mini Book",
        summaryKo: "주요 자음 ㅁ, ㅂ, ㅅ, ㅈ을 다차원으로 복습하고 교과서 9과 및 10과를 학습합니다.",
        summaryEn: "Students review core consonants ㅁ, ㅂ, ㅅ, ㅈ and cover textbook Chapters 9 and 10.",
        activityKo: "8종 단어 메모리 카드 게임 키트와 나만의 한글 미니북 만들기, 독도 프로젝트 성찰",
        activityEn: "Creating an 8-word memory card kit, Hangul mini-book, and Dokdo project reflection",
        language: ["ㅁ, ㅂ", "ㅅ, ㅈ", "가-하 sequence"],
        homeworkKo: "익힘책 9과 p.42-47 및 10과 p.48-53을 완료하고 미니북을 가족에게 읽어 주세요.",
        homeworkEn: "Complete Workbook Ch. 9 pp. 42-47 and Ch. 10 pp. 48-53. Encourage your child to read the mini-book to family.",
        parent: "The mini-book is a lovely way for students to show what they can read."
      },
      {
        week: 10, date: "10/31", title: "ㅎ, ㅇ, ㄹ and Korean Folk Art",
        summaryKo: "ㅎ, ㅇ, ㄹ 음운 인식 비디오를 보고 11과 허수아비와 친구들 어휘를 확장합니다.",
        summaryEn: "Students watch a phonological awareness video for ㅎ, ㅇ, ㄹ and expand vocabulary through Lesson 11 The Scarecrow and Friends.",
        activityKo: "한국 전통 민화 호작도 3D 퍼즐, VINU 텍스트-그림 매칭 게임",
        activityEn: "Korean folk painting Ho-jak-do 3D puzzle and VINU text-picture matching game",
        language: ["ㅎ, ㅇ, ㄹ", "허수아비와 친구들", "호랑이, 까치, 호작도"],
        homeworkKo: "익힘책 11과 단어 쓰기 p.54-59를 완료합니다.",
        homeworkEn: "Complete Workbook Lesson 11 vocabulary writing, pp. 54-59.",
        parent: "Students connected vocabulary with Korean visual culture."
      },
      {
        week: 11, date: "11/7", title: "Hangul Fairy Tale and Nabiya",
        summaryKo: "디지털 미디어를 활용한 통합적 언어 몰입 수업과 교과서 p.142-151을 학습합니다.",
        summaryEn: "Students experience immersive language learning through digital media and study textbook pp. 142-151.",
        activityKo: "동화, 동요 나비야 가사 분석, 드로잉, 풍선 나비와 꽃을 활용한 음악-신체 통합 활동",
        activityEn: "Fairy tale, Nabiya lyric learning, drawing, and music-movement activity with balloon butterflies and flowers",
        language: ["나비야", "동요 어휘", "Story vocabulary review"],
        homeworkKo: "이번 주는 과제가 없습니다. 가정에서 나비야 동요를 함께 불러보세요.",
        homeworkEn: "No homework this week. Enjoy singing Nabiya together at home.",
        parent: "A gentle music activity at home can help children remember Korean sounds naturally."
      },
      {
        week: 12, date: "11/14", title: "ㅋ, ㅌ and Poem Drawing",
        summaryKo: "교과서 13과 음운 구조와 자음 ㅋ, ㅌ이 들어가는 어휘를 학습합니다.",
        summaryEn: "Students study Chapter 13 phonetic structures and vocabulary containing ㅋ and ㅌ.",
        activityKo: "말놀이 동시 나무야를 읽고 그림으로 표현하기",
        activityEn: "Reading the poem-song Namuya and expressing it through drawing",
        language: ["ㅋ, ㅌ", "토마토", "나무야"],
        homeworkKo: "익힘책 p.60-65를 완료합니다.",
        homeworkEn: "Complete Workbook pp. 60-65.",
        parent: "Students practiced Korean through poetry, sound play, and imagination."
      },
      {
        week: 13, date: "11/21", title: "ㅍ, Birthday Party, and Chaekgado",
        summaryKo: "격음 ㅍ을 인식하고 교과서 14과 생일 축하 파티와 가족 호칭 및 관계 어휘를 학습합니다.",
        summaryEn: "Students recognize consonant ㅍ and study Chapter 14 Birthday Party, family titles, and relationship vocabulary.",
        activityKo: "선물 카드 쓰기, 책가도 3D 퍼즐, VINU 총괄 단어 복습 토너먼트",
        activityEn: "Gift card writing, Chaekgado 3D puzzle, and VINU vocabulary review tournament",
        language: ["ㅍ", "피아노", "생일 축하", "가족 호칭"],
        homeworkKo: "익힘책 14과 p.66-71을 완료합니다. 11/28은 추수감사절 연휴로 휴강입니다.",
        homeworkEn: "Complete Workbook Ch. 14 pp. 66-71. No class on 11/28 due to Thanksgiving Holiday.",
        parent: "Have a wonderful Thanksgiving break."
      },
      {
        week: 14, date: "12/5", title: "Aspirated Consonant Review and Body Words",
        summaryKo: "교과서 p.172-181을 학습하고 격음 자음 ㅋ, ㅌ, ㅍ, ㅊ을 종합 복습하며 신체 부위 어휘를 익힙니다.",
        summaryEn: "Students cover textbook pp. 172-181, review ㅋ, ㅌ, ㅍ, ㅊ, and learn body part vocabulary.",
        activityKo: "머리 어깨 무릎 발 TPR 활동, 민화 전시 관람, VINU 어휘 총괄 복습",
        activityEn: "Head-Shoulders-Knees-Toes TPR, Minhwa exhibit viewing, and VINU cumulative vocabulary review",
        language: ["ㅋ, ㅌ, ㅍ, ㅊ", "머리, 어깨, 무릎, 발", "Review vocabulary"],
        homeworkKo: "이번 주는 공식 과제가 없습니다. 다음 주는 최종 종강일 및 총괄 복습 활동입니다.",
        homeworkEn: "No homework this week. Next week is our final class with cumulative review and celebration.",
        parent: "Please help students come ready for the final class celebration."
      },
      {
        week: 15, date: "12/12", title: "Final Review and Celebration",
        summaryKo: "교과서 마지막 16과 p.182-191을 완료하고 전체 학기 어휘를 총정리합니다.",
        summaryEn: "Students complete final Chapter 16, pp. 182-191, and review vocabulary from the entire semester.",
        activityKo: "한글 이름 팔찌 만들기, 비밀 크레용-물감 단어 발견 놀이, 수료식 및 어워드",
        activityEn: "Korean name bracelet, hidden word reveal activity, completion ceremony, and awards",
        language: ["전체 모음과 자음 복습", "한글 이름", "학기 어휘 총정리"],
        homeworkKo: "15주 동안 자녀의 한국어 성장을 지원해 주셔서 감사합니다. 방학 중에도 교재를 활용해 자연스럽게 복습해 주세요.",
        homeworkEn: "Thank you for supporting your child's Korean learning journey. Please encourage continued exposure during winter break.",
        parent: "Heartfelt gratitude to all parents for your dedication and support throughout the semester."
      }
    ];

    const tabs = document.querySelector("#tabs");
    const container = document.querySelector("#lesson-container");

    function makeList(items, ordered = false) {
      const tag = ordered ? "ol" : "ul";
      return `<${tag}>${items.map(item => `<li>${item}</li>`).join("")}</${tag}>`;
    }

    function renderWeek(index) {
      const item = weeks[index];
      tabs.querySelectorAll(".tab").forEach((tab, tabIndex) => {
        const selected = tabIndex === index;
        tab.setAttribute("aria-selected", selected ? "true" : "false");
        tab.tabIndex = selected ? 0 : -1;
      });

      container.innerHTML = `
        <article class="lesson" role="tabpanel" id="week-panel-${item.week}" aria-labelledby="week-tab-${item.week}">
          <div class="lesson-head">
            <div>
              <h2>${item.title}</h2>
              <p class="date"><strong>Date:</strong> ${item.date} · <strong>Week ${item.week}</strong></p>
            </div>
            <span class="week-tag">${item.week}주차</span>
          </div>

          <div class="lesson-grid">
            <section class="section full">
              <h3>수업 내용 | Lesson Summary</h3>
              <div class="ko-en">
                <div class="lang-block"><strong>KO</strong><br>${item.summaryKo}</div>
                <div class="lang-block"><strong>EN</strong><br>${item.summaryEn}</div>
              </div>
            </section>

            <section class="section">
              <h3>언어 초점 | Language Focus</h3>
              ${makeList(item.language)}
            </section>

            <section class="section">
              <h3>미디어/활동 | Media & Activities</h3>
              <div class="ko-en">
                <div><strong>KO:</strong> ${item.activityKo}</div>
                <div><strong>EN:</strong> ${item.activityEn}</div>
              </div>
            </section>

            <section class="section homework">
              <h3>숙제 | Homework</h3>
              <div class="ko-en">
                <div><strong>KO:</strong> ${item.homeworkKo}</div>
                <div><strong>EN:</strong> ${item.homeworkEn}</div>
              </div>
            </section>

            <section class="section parent">
              <h3>학부모 안내 | Parent Notice</h3>
              <p>${item.parent}</p>
            </section>

            <section class="section standards full">
              <h3>교육과정 기준 | Standards Alignment</h3>
              <p><strong>KO:</strong> 학생들이 듣기, 말하기, 읽기, 쓰기를 직접 경험하도록 설계된 ACTFL Novice Low to Novice Mid 지향 수업입니다.</p>
              <p><strong>EN:</strong> This standards-aligned course supports movement from ACTFL Novice Low toward Novice Mid through performance tasks, creative projects, and cultural learning.</p>
            </section>
          </div>

          <div class="actions">
            <button class="action" type="button" id="prev-week">Previous Week</button>
            <button class="action primary" type="button" id="next-week">Next Week</button>
            <button class="action" type="button" onclick="window.print()">Print</button>
          </div>
        </article>
      `;

      document.querySelector("#prev-week").disabled = index === 0;
      document.querySelector("#next-week").disabled = index === weeks.length - 1;
      document.querySelector("#prev-week").addEventListener("click", () => renderWeek(Math.max(0, index - 1)));
      document.querySelector("#next-week").addEventListener("click", () => renderWeek(Math.min(weeks.length - 1, index + 1)));
    }

    weeks.forEach((item, index) => {
      const button = document.createElement("button");
      button.className = "tab";
      button.type = "button";
      button.setAttribute("role", "tab");
      button.id = `week-tab-${item.week}`;
      button.setAttribute("aria-controls", `week-panel-${item.week}`);
      button.setAttribute("aria-selected", index === 0 ? "true" : "false");
      button.textContent = `Week ${item.week}`;
      button.addEventListener("click", () => renderWeek(index));
      tabs.appendChild(button);
    });

    renderWeek(0);
  </script>
</body>
</html>
