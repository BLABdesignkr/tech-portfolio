<!DOCTYPE html>

<html lang="ko">

<head>

&#x20; <meta charset="UTF-8">

&#x20; <meta name="viewport" content="width=device-width, initial-scale=1.0">

&#x20; <title>BLAB Portfolio | NEXT-GEN DIGITAL MANUFACTURING</title>

&#x20; <!-- 프리미엄 고대비 서체 Inter 및 Pretendard 로드 -->

&#x20; <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.css" />

&#x20; <style>

&#x20;   /\* 1. 디자인 시스템 정의 (Vention Tech 감성) \*/

&#x20;   :root {

&#x20;     --blab-bg-dark: #07090e;

&#x20;     --blab-bg-card: #111622;

&#x20;     --blab-accent-blue: #0066ff;

&#x20;     --blab-accent-cyan: #00f0ff;

&#x20;     --blab-text-primary: #ffffff;

&#x20;     --blab-text-secondary: #8f9cae;

&#x20;     --blab-grid-line: rgba(255, 255, 255, 0.04);

&#x20;   }



&#x20;   \* {

&#x20;     box-sizing: border-box;

&#x20;     margin: 0;

&#x20;     padding: 0;

&#x20;     font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;

&#x20;     -webkit-font-smoothing: antialiased;

&#x20;   }



&#x20;   body {

&#x20;     background-color: var(--blab-bg-dark);

&#x20;     color: var(--blab-text-primary);

&#x20;     overflow-x: hidden;

&#x20;   }



&#x20;   /\* 엔지니어링 모듈러 그리드 배경 패턴 \*/

&#x20;   .blab-grid-bg {

&#x20;     position: fixed;

&#x20;     top: 0;

&#x20;     left: 0;

&#x20;     width: 100%;

&#x20;     height: 100%;

&#x20;     background-image: 

&#x20;       linear-gradient(to right, var(--blab-grid-line) 1px, transparent 1px),

&#x20;       linear-gradient(to bottom, var(--blab-grid-line) 1px, transparent 1px);

&#x20;     background-size: 40px 40px;

&#x20;     z-index: -1;

&#x20;     pointer-events: none;

&#x20;   }



&#x20;   /\* 2. 네비게이션 헤더 \*/

&#x20;   .blab-header {

&#x20;     width: 100%;

&#x20;     padding: 30px 5%;

&#x20;     display: flex;

&#x20;     justify-content: space-between;

&#x20;     align-items: center;

&#x20;     position: absolute;

&#x20;     top: 0;

&#x20;     left: 0;

&#x20;     z-index: 100;

&#x20;   }



&#x20;   .blab-logo {

&#x20;     font-size: 1.5rem;

&#x20;     font-weight: 900;

&#x20;     letter-spacing: -0.05em;

&#x20;     color: var(--blab-text-primary);

&#x20;   }

&#x20;   .blab-logo span { color: var(--blab-accent-blue); }



&#x20;   .blab-nav-badge {

&#x20;     background: rgba(0, 102, 255, 0.1);

&#x20;     border: 1px solid var(--blab-accent-blue);

&#x20;     padding: 6px 16px;

&#x20;     border-radius: 20px;

&#x20;     font-size: 0.85rem;

&#x20;     font-weight: 600;

&#x20;     color: var(--blab-accent-cyan);

&#x20;   }



&#x20;   /\* 3. 히어로 섹션 (Vention 스타일의 구조적 타이포) \*/

&#x20;   .blab-hero {

&#x20;     min-height: 100vh;

&#x20;     display: flex;

&#x20;     align-items: center;

&#x20;     padding: 0 8%;

&#x20;     position: relative;

&#x20;   }



&#x20;   .blab-hero-content {

&#x20;     max-width: 900px;

&#x20;     z-index: 2;

&#x20;   }



&#x20;   .blab-hero-tag {

&#x20;     font-size: 1rem;

&#x20;     font-weight: 700;

&#x20;     color: var(--blab-accent-blue);

&#x20;     letter-spacing: 0.2em;

&#x20;     text-transform: uppercase;

&#x20;     margin-bottom: 20px;

&#x20;   }



&#x20;   .blab-hero-title {

&#x20;     font-size: clamp(3.5rem, 8vw, 7.5rem);

&#x20;     font-weight: 900;

&#x20;     line-height: 0.9;

&#x20;     letter-spacing: -0.05em;

&#x20;     margin-bottom: 30px;

&#x20;     text-transform: uppercase;

&#x20;   }



&#x20;   .blab-hero-title span {

&#x20;     display: inline-block;

&#x20;     opacity: 0;

&#x20;     transform: translateY(50px);

&#x20;     animation: revealUp 1.2s cubic-bezier(0.16, 1, 0.3, 1) forwards;

&#x20;   }

&#x20;   .blab-hero-title .word-1 { animation-delay: 0.1s; }

&#x20;   .blab-hero-title .word-2 { animation-delay: 0.3s; color: var(--blab-accent-blue); }



&#x20;   .blab-hero-desc {

&#x20;     font-size: clamp(1.1rem, 2vw, 1.4rem);

&#x20;     color: var(--blab-text-secondary);

&#x20;     line-height: 1.6;

&#x20;     max-width: 600px;

&#x20;     margin-bottom: 40px;

&#x20;   }



&#x20;   /\* 4. 벤토 그리드 아키텍처 섹션 \*/

&#x20;   .blab-section {

&#x20;     padding: 140px 8%;

&#x20;     position: relative;

&#x20;   }



&#x20;   .blab-section-header {

&#x20;     margin-bottom: 60px;

&#x20;   }



&#x20;   .blab-section-title {

&#x20;     font-size: 2.5rem;

&#x20;     font-weight: 900;

&#x20;     letter-spacing: -0.03em;

&#x20;     margin-bottom: 15px;

&#x20;   }



&#x20;   /\* 고감도 테크 벤토 그리드 \*/

&#x20;   .blab-bento-grid {

&#x20;     display: grid;

&#x20;     grid-template-columns: repeat(3, 1fr);

&#x20;     gap: 25px;

&#x20;   }



&#x20;   .blab-card {

&#x20;     background: var(--blab-bg-card);

&#x20;     border: 1px solid rgba(255, 255, 255, 0.05);

&#x20;     border-radius: 16px;

&#x20;     padding: 40px;

&#x20;     position: relative;

&#x20;     overflow: hidden;

&#x20;     transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);

&#x20;   }



&#x20;   .blab-card::before {

&#x20;     content: '';

&#x20;     position: absolute;

&#x20;     top: 0; left: 0; width: 100%; height: 2px;

&#x20;     background: linear-gradient(90deg, var(--blab-accent-blue), var(--blab-accent-cyan));

&#x20;     opacity: 0;

&#x20;     transition: opacity 0.3s ease;

&#x20;   }



&#x20;   .blab-card:hover {

&#x20;     transform: translateY(-5px);

&#x20;     border-color: rgba(0, 102, 255, 0.3);

&#x20;     box-shadow: 0 20px 40px rgba(0,0,0,0.5);

&#x20;   }



&#x20;   .blab-card:hover::before { opacity: 1; }



&#x20;   .blab-card-num {

&#x20;     font-size: 0.85rem;

&#x20;     font-weight: 700;

&#x20;     color: var(--blab-accent-cyan);

&#x20;     margin-bottom: 30px;

&#x20;   }



&#x20;   .blab-card-title {

&#x20;     font-size: 1.6rem;

&#x20;     font-weight: 800;

&#x20;     margin-bottom: 15px;

&#x20;     letter-spacing: -0.02em;

&#x20;   }



&#x20;   .blab-card-desc {

&#x20;     color: var(--blab-text-secondary);

&#x20;     line-height: 1.6;

&#x20;     font-size: 1rem;

&#x20;   }



&#x20;   /\* 대형 스팬 카드 (Vention 스타일 시뮬레이터 데모 공간) \*/

&#x20;   .grid-col-2 { grid-column: span 2; }



&#x20;   /\* 5. JS 실시간 제어 시뮬레이션 콘솔 모듈 (기술력 증명 장치) \*/

&#x20;   .blab-console {

&#x20;     background: #0d121f;

&#x20;     border: 1px dashed rgba(0, 102, 255, 0.4);

&#x20;     border-radius: 12px;

&#x20;     padding: 25px;

&#x20;     margin-top: 20px;

&#x20;   }



&#x20;   .blab-console-header {

&#x20;     display: flex;

&#x20;     justify-content: space-between;

&#x20;     align-items: center;

&#x20;     margin-bottom: 20px;

&#x20;     border-bottom: 1px solid rgba(255,255,255,0.05);

&#x20;     padding-bottom: 10px;

&#x20;   }



&#x20;   .blab-status-dot {

&#x20;     width: 8px; height: 8px;

&#x20;     background-color: #00ff66;

&#x20;     border-radius: 50%;

&#x20;     display: inline-block;

&#x20;     box-shadow: 0 0 10px #00ff66;

&#x20;     margin-right: 8px;

&#x20;   }



&#x20;   .blab-metric-flex {

&#x20;     display: flex;

&#x20;     justify-content: space-between;

&#x20;     gap: 15px;

&#x20;   }



&#x20;   .blab-metric-box {

&#x20;     background: rgba(255,255,255,0.02);

&#x20;     padding: 15px;

&#x20;     border-radius: 8px;

&#x20;     width: 50%;

&#x20;   }



&#x20;   .blab-metric-label { font-size: 0.75rem; color: var(--blab-text-secondary); text-transform: uppercase; }

&#x20;   .blab-metric-value { font-size: 1.8rem; font-weight: 800; color: var(--blab-accent-cyan); margin-top: 5px; }



&#x20;   /\* 6. 강력한 매출전환 푸터 락업 \*/

&#x20;   .blab-cta-footer {

&#x20;     background: linear-gradient(180deg, transparent, #0b111e);

&#x20;     padding: 120px 8% 80px 8%;

&#x20;     text-align: center;

&#x20;     border-top: 1px solid rgba(255,255,255,0.03);

&#x20;   }



&#x20;   .blab-btn {

&#x20;     display: inline-block;

&#x20;     background: var(--blab-accent-blue);

&#x20;     color: white;

&#x20;     text-decoration: none;

&#x20;     padding: 18px 40px;

&#x20;     font-weight: 700;

&#x20;     border-radius: 30px;

&#x20;     font-size: 1.1rem;

&#x20;     letter-spacing: -0.02em;

&#x20;     box-shadow: 0 10px 30px rgba(0, 102, 255, 0.3);

&#x20;     transition: all 0.3s ease;

&#x20;     margin-top: 30px;

&#x20;   }



&#x20;   .blab-btn:hover {

&#x20;     background: #1a75ff;

&#x20;     transform: translateY(-3px);

&#x20;     box-shadow: 0 15px 35px rgba(0, 102, 255, 0.5);

&#x20;   }



&#x20;   /\* 7. 스크롤 반응형 Reveal 애니메이션 \*/

&#x20;   .blab-reveal {

&#x20;     opacity: 0;

&#x20;     transform: translateY(40px);

&#x20;     transition: all 1s cubic-bezier(0.16, 1, 0.3, 1);

&#x20;   }



&#x20;   .blab-reveal.active {

&#x20;     opacity: 1;

&#x20;     transform: translateY(0);

&#x20;   }



&#x20;   @keyframes revealUp {

&#x20;     to { opacity: 1; transform: translateY(0); }

&#x20;   }



&#x20;   /\* 모바일 반응형 완벽 최적화 \*/

&#x20;   @media (max-width: 1024px) {

&#x20;     .blab-bento-grid { grid-template-columns: 1fr; }

&#x20;     .grid-col-2 { grid-column: span 1; }

&#x20;   }

&#x20; </style>

</head>

<body>



&#x20; <div class="blab-grid-bg"></div>



&#x20; <header class="blab-header">

&#x20;   <div class="blab-logo">MANUFACTURING<span>.OS</span></div>

&#x20;   <div class="blab-nav-badge">CASE STUDY #02</div>

&#x20; </header>



&#x20; <!-- 메인 히어로 섹션 -->

&#x20; <section class="blab-hero">

&#x20;   <div class="blab-hero-content">

&#x20;     <div class="blab-hero-tag">Cloud-Based Factory Automation</div>

&#x20;     <h1 class="blab-hero-title">

&#x20;       <span class="word-1">ENGINEERING.</span><br>

&#x20;       <span class="word-2">AUTOMATED.</span>

&#x20;     </h1>

&#x20;     <p class="blab-hero-desc">

&#x20;       Vention의 기계적 정밀함과 소프트웨어 아키텍처를 결합한 디지털 제조 솔루션 포트폴리오입니다. 복잡한 산업 설비 자동화를 하나의 고도화된 클라우드 인터페이스로 통합 제어합니다.

&#x20;     </p>

&#x20;   </div>

&#x20; </section>



&#x20; <!-- 벤토 아키텍처 및 라이브 데이터 증명 섹션 -->

&#x20; <section class="blab-section">

&#x20;   <div class="blab-section-header blab-reveal">

&#x20;     <div class="blab-hero-tag">Core Architecture</div>

&#x20;     <h2 class="blab-section-title">스마트 팩토리의 기술적 증명</h2>

&#x20;   </div>



&#x20;   <div class="blab-bento-grid">

&#x20;     <!-- 카드 1 (인터랙티브 대형 콘솔) -->

&#x20;     <div class="blab-card grid-col-2 blab-reveal">

&#x20;       <div class="blab-card-num">MODULE 01 / LIVE CONTROLLER</div>

&#x20;       <h3 class="blab-card-title">실시간 엣지 컴퓨팅 및 원격 하드웨어 동기화</h3>

&#x20;       <p class="blab-card-desc">웹 브라우저 내부에서 공장의 기계 장치를 지연 시간 없이 다이렉트로 제어하는 실시간 렌더링 관제 가상 시스템 시뮬레이션 인터페이스입니다.</p>

&#x20;       

&#x20;       <!-- 실시간 JS 작동 콘솔 위젯 (클라이언트가 감탄하는 포인트) -->

&#x20;       <div class="blab-console">

&#x20;         <div class="blab-console-header">

&#x20;           <div><span class="blab-status-dot"></span><span style="font-size:0.8rem; font-weight:700; color:#00ff66;">FACTORY SECTIONS CONNECTED</span></div>

&#x20;           <div style="font-size:0.75rem; color:var(--blab-text-secondary);">SYS\_REFRESH: LIVE</div>

&#x20;         </div>

&#x20;         <div class="blab-metric-flex">

&#x20;           <div class="blab-metric-box">

&#x20;             <div class="blab-metric-label">OPERATIONAL EFFICIENCY</div>

&#x20;             <div class="blab-metric-value" id="eff-value">98.42%</div>

&#x20;           </div>

&#x20;           <div class="blab-metric-box">

&#x20;             <div class="blab-metric-label">REAL-TIME DATA STREAM</div>

&#x20;             <div class="blab-metric-value" id="stream-value">4,120 kb/s</div>

&#x20;           </div>

&#x20;         </div>

&#x20;       </div>

&#x20;     </div>



&#x20;     <!-- 카드 2 -->

&#x20;     <div class="blab-card blab-reveal">

&#x20;       <div class="blab-card-num">MODULE 02 / PLUG \& PLAY</div>

&#x20;       <h3 class="blab-card-title">인텔리전트 컴포넌트 솔루션</h3>

&#x20;       <p class="blab-card-desc">하드웨어 연결 시 클라우드가 감지하여 드라이버를 자동 세팅하는 모듈러 제조 오퍼레이팅 시스템 구조입니다.</p>

&#x20;     </div>



&#x20;     <!-- 카드 3 -->

&#x20;     <div class="blab-card blab-reveal">

&#x20;       <div class="blab-card-num">MODULE 03 / ROI ARCHITECTURE</div>

&#x20;       <h3 class="blab-card-title">공정 리드타임 84% 단축</h3>

&#x20;       <p class="blab-card-desc">설계부터 배포까지 소요되는 인프라 비용과 제조 리드타임을 데이터 수치화 기반으로 설계하여 비즈니스 전환 효과를 극대화합니다.</p>

&#x20;     </div>



&#x20;     <!-- 카드 4 (대형 스팬 카드) -->

&#x20;     <div class="blab-card grid-col-2 blab-reveal">

&#x20;       <div class="blab-card-num">MODULE 04 / SEO \& GROWTH</div>

&#x20;       <h3 class="blab-card-title">제조 경쟁력을 높이는 유저 경험과 검색 최적화(SEO)</h3>

&#x20;       <p class="blab-card-desc">B2B 제조 중소기업 및 글로벌 바이어들이 타겟 검색 시 상위에 노출될 수 있도록 시맨틱 마크업 설계와 데이터 인덱싱 인프라 세팅을 올인원 패키지로 지원합니다.</p>

&#x20;     </div>

&#x20;   </div>

&#x20; </section>



&#x20; <!-- 매출 전환 푸터 섹션 -->

&#x20; <section class="blab-cta-footer blab-reveal">

&#x20;   <div class="blab-hero-tag">NEXT LEVEL BUSINESS</div>

&#x20;   <h2 class="blab-section-title" style="font-size: 3rem;">비즈니스의 디지털 전환,<br>더 이상 복잡할 필요 없습니다.</h2>

&#x20;   <a href="https://kmong.com" target="\_blank" rel="noopener noreferrer" class="blab-btn">BLAB에 외주 프로젝트 문의하기</a>

&#x20; </section>



&#x20; <script>

&#x20;   /\* 1. 실시간 데이터 대시보드 스트리밍 시뮬레이션 스크립트 \*/

&#x20;   setInterval(() => {

&#x20;     // 효율성 수치 미세 변동 (98.2% \~ 99.8%)

&#x20;     const eff = (98.2 + Math.random() \* 1.6).toFixed(2);

&#x20;     // 스트리밍 데이터 변동 (3900 \~ 4400)

&#x20;     const stream = Math.floor(3900 + Math.random() \* 500).toLocaleString();

&#x20;     

&#x20;     document.getElementById('eff-value').innerText = eff + '%';

&#x20;     document.getElementById('stream-value').innerText = stream + ' kb/s';

&#x20;   }, 1200);



&#x20;   /\* 2. 순수 JS 기반 스크롤 Reveal 애니메이션 (Framer Motion 스타일 인터랙션) \*/

&#x20;   const revealElements = document.querySelectorAll('.blab-reveal');

&#x20;   const revealOnScroll = () => {

&#x20;     revealElements.forEach(element => {

&#x20;       const elementTop = element.getBoundingClientRect().top;

&#x20;       const windowHeight = window.innerHeight;

&#x20;       if (elementTop < windowHeight \* 0.88) {

&#x20;         element.classList.add('active');

&#x20;       }

&#x20;     });

&#x20;   };

&#x20;   

&#x20;   window.addEventListener('scroll', revealOnScroll);

&#x20;   window.addEventListener('load', () => {

&#x20;     revealOnScroll(); // 첫 로드 시 실행

&#x20;   });

&#x20; </script>

</body>

</html>

