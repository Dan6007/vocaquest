[index.html](https://github.com/user-attachments/files/29368399/index.html)
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>보카퀘스트 - VocaQuest 영단어 퀴즈</title>
  <!-- Google Fonts: Outfit for titles, Inter for body -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Outfit:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="index.css">
</head>
<body class="dark-theme">
  <!-- Glowing decorative blobs for premium glassmorphism background -->
  <div class="bg-glow blob-1"></div>
  <div class="bg-glow blob-2"></div>
  <div class="bg-glow blob-3"></div>

  <div class="app-container">
    <!-- Header -->
    <header class="app-header">
      <div class="logo-area" id="btn-logo">
        <svg class="logo-icon" viewBox="0 0 24 24" width="32" height="32">
          <path fill="currentColor" d="M12 2L2 22h20L12 2zm0 4.5L18.5 19H5.5L12 6.5zM11 10v4h2v-4h-2zm0 5v2h2v-2h-2z"/>
        </svg>
        <span class="logo-text">VocaQuest</span>
      </div>
      <div class="header-controls">
        <button class="icon-btn" id="btn-backup" title="진도 백업/복원" aria-label="진도 백업/복원">
          <svg viewBox="0 0 24 24" width="20" height="20">
            <path fill="currentColor" d="M19.35 10.04C18.67 6.59 15.64 4 12 4 9.11 4 6.6 5.64 5.35 8.04 2.34 8.36 0 10.91 0 14c0 3.31 2.69 6 6 6h13c2.76 0 5-2.24 5-5 0-2.64-2.05-4.78-4.65-4.96zM19 18H6c-2.21 0-4-1.79-4-4 0-2.05 1.53-3.76 3.56-3.97l1.07-.11.5-.95C8.08 7.14 9.94 6 12 6c2.62 0 4.88 1.86 5.39 4.43l.3 1.5 1.53.11c1.56.1 2.78 1.41 2.78 2.96 0 1.65-1.35 3-3 3zm-5.55-8h-2.9v3H7.5l4.5 4.5 4.5-4.5h-3.05V10z"/>
          </svg>
        </button>
        <button class="icon-btn" id="btn-theme-toggle" title="테마 변경" aria-label="테마 변경">
          <!-- Sun Icon (shows in dark mode) -->
          <svg class="sun-icon" viewBox="0 0 24 24" width="20" height="20">
            <path fill="currentColor" d="M12 7c-2.76 0-5 2.24-5 5s2.24 5 5 5 5-2.24 5-5-2.24-5-5-5zM2 13h2c.55 0 1-.45 1-1s-.45-1-1-1H2c-.55 0-1 .45-1 1s.45 1 1 1zm18 0h2c.55 0 1-.45 1-1s-.45-1-1-1h-2c-.55 0-1 .45-1 1s.45 1 1 1zM11 2v2c0 .55.45 1 1 1s1-.45 1-1V2c0-.55-.45-1-1-1s-1 .45-1 1zm0 18v2c0 .55.45 1 1 1s1-.45 1-1v-2c0-.55-.45-1-1-1s-1 .45-1 1zM5.99 4.58c-.39-.39-1.03-.39-1.41 0s-.39 1.03 0 1.41l1.06 1.06c.39.39 1.03.39 1.41 0s.39-1.03 0-1.41L5.99 4.58zm12.37 12.37c-.39-.39-1.03-.39-1.41 0s-.39 1.03 0 1.41l1.06 1.06c.39.39 1.03.39 1.41 0s.39-1.03 0-1.41l-1.06-1.06zm1.06-10.96c.39-.39.39-1.03 0-1.41s-1.03-.39-1.41 0l-1.06 1.06c-.39.39-.39 1.03 0 1.41s1.03.39 1.41 0l1.06-1.06zM7.05 18.01c.39-.39.39-1.03 0-1.41s-1.03-.39-1.41 0l-1.06 1.06c-.39.39-.39 1.03 0 1.41s1.03.39 1.41 0l1.06-1.06z"/>
          </svg>
          <!-- Moon Icon (shows in light mode) -->
          <svg class="moon-icon" viewBox="0 0 24 24" width="20" height="20">
            <path fill="currentColor" d="M12.3 22h-.1c-5.5 0-10-4.5-10-10 0-4.8 3.5-8.9 8.2-9.8.6-.1 1.2.3 1.3.9.1.6-.2 1.2-.8 1.4-3.4 1-5.7 4.1-5.7 7.6 0 4.4 3.6 8 8 8 3.5 0 6.6-2.3 7.6-5.7.2-.6.8-.9 1.4-.8.6.1 1 .7.9 1.3-.9 4.7-5 8.1-9.8 8.1z"/>
          </svg>
        </button>
      </div>
    </header>

    <!-- Main Screens Container -->
    <main class="main-content">
      
      <!-- 1. DASHBOARD SCREEN -->
      <section id="screen-dashboard" class="screen active">
        <div class="hero-section">
          <h1>영단어 마스터를 위한<br><span class="gradient-text">보카퀘스트 챌린지</span></h1>
          <p class="subtitle">다양한 퀴즈를 풀고 단어를 암기하여 랭크를 올려보세요!</p>
        </div>

        <!-- Progress Widget Grid -->
        <div class="stats-grid">
          <div class="stat-card glass-panel">
            <div class="stat-icon icon-blue">
              <svg viewBox="0 0 24 24" width="24" height="24"><path fill="currentColor" d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm1 17h-2v-2h2v2zm2.07-7.75l-.9.92C13.45 12.9 13 13.5 13 15h-2v-.5c0-1.1.45-2.1 1.17-2.83l1.24-1.26c.37-.36.59-.86.59-1.41 0-1.1-.9-2-2-2s-2 .9-2 2H7c0-2.76 2.24-5 5-5s5 2.24 5 5c0 1.04-.42 1.99-1.07 2.75z"/></svg>
            </div>
            <div class="stat-info">
              <span class="stat-label">누적 학습 점수</span>
              <span class="stat-value" id="stats-xp">0 XP</span>
            </div>
          </div>
          <div class="stat-card glass-panel">
            <div class="stat-icon icon-orange">
              <svg viewBox="0 0 24 24" width="24" height="24"><path fill="currentColor" d="M12 11.55C9.64 9.35 6.48 8 3 8v11c3.48 0 6.64 1.35 9 3.55 2.36-2.2 5.52-3.55 9-3.55V8c-3.48 0-6.64 1.35-9 3.55zM12 2c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3z"/></svg>
            </div>
            <div class="stat-info">
              <span class="stat-label">마스터한 단어</span>
              <span class="stat-value" id="stats-mastered">0 / 45</span>
            </div>
          </div>
          <div class="stat-card glass-panel">
            <div class="stat-icon icon-red">
              <svg viewBox="0 0 24 24" width="24" height="24"><path fill="currentColor" d="M12 23c-5.52 0-10-4.48-10-10S6.48 3 12 3s10 4.48 10 10-4.48 10-10 10zm-1-15v6h2V8h-2zm0 8v2h2v-2h-2z"/></svg>
            </div>
            <div class="stat-info">
              <span class="stat-label">최고 불타는 콤보</span>
              <span class="stat-value" id="stats-streak">0 Combo</span>
            </div>
          </div>
        </div>

        <!-- Configuration Settings -->
        <div class="config-section glass-panel">
          <h3>난이도 설정</h3>
          <div class="difficulty-selector">
            <button class="diff-btn active" data-difficulty="easy">
              <span class="diff-title">쉬움 (Easy)</span>
              <span class="diff-desc">초급 영단어 및 기본 숙어</span>
            </button>
            <button class="diff-btn" data-difficulty="medium">
              <span class="diff-title">보통 (Medium)</span>
              <span class="diff-desc">중급/수능 필수 영단어</span>
            </button>
            <button class="diff-btn" data-difficulty="hard">
              <span class="diff-title">어려움 (Hard)</span>
              <span class="diff-desc">학술 및 토플/SAT 고급 어휘</span>
            </button>
          </div>
        </div>

        <!-- Mode Select Grid -->
        <div class="modes-container">
          <h3>게임 모드 선택</h3>
          <div class="modes-grid">
            <div class="mode-card glass-panel" id="mode-quiz">
              <div class="mode-icon quiz-theme">
                <svg viewBox="0 0 24 24" width="36" height="36"><path fill="currentColor" d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-2 10h-4v4h-2v-4H7v-2h4V7h2v4h4v2z"/></svg>
              </div>
              <h4>4지선다 객관식 퀴즈</h4>
              <p>제한 시간 안에 단어의 뜻을 맞혀 콤보 점수를 획득하세요.</p>
              <button class="btn btn-primary">도전하기</button>
            </div>

            <div class="mode-card glass-panel" id="mode-spelling">
              <div class="mode-icon spelling-theme">
                <svg viewBox="0 0 24 24" width="36" height="36"><path fill="currentColor" d="M3 17.25V21h3.75L17.81 9.94l-3.75-3.75L3 17.25zM20.71 7.04c.39-.39.39-1.02 0-1.41l-2.34-2.34c-.39-.39-1.02-.39-1.41 0l-1.83 1.83 3.75 3.75 1.83-1.83z"/></svg>
              </div>
              <h4>주관식 스펠링 적기</h4>
              <p>뜻과 힌트를 보고 영어 단어의 스펠링을 완벽하게 맞혀보세요.</p>
              <button class="btn btn-primary">도전하기</button>
            </div>

            <div class="mode-card glass-panel" id="mode-flashcards">
              <div class="mode-icon flashcard-theme">
                <svg viewBox="0 0 24 24" width="36" height="36"><path fill="currentColor" d="M4 6H2v14c0 1.1.9 2 2 2h14v-2H4V6zm16-4H8c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h12c1.1 0-2-.9-2-2V4c0-1.1-.9-2-2-2zm0 14H8V4h12v12z"/></svg>
              </div>
              <h4>단어장 플래시 카드</h4>
              <p>3D 카드를 뒤집어가며 단어를 편하게 읽고 암기해 보세요.</p>
              <button class="btn btn-primary">공부하기</button>
            </div>
          </div>
        </div>
      </section>

      <!-- 2. QUIZ MODE SCREEN -->
      <section id="screen-quiz" class="screen">
        <div class="game-header">
          <button class="btn-back" id="quiz-back">
            <svg viewBox="0 0 24 24" width="20" height="20"><path fill="currentColor" d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z"/></svg>
            <span>대시보드로</span>
          </button>
          <div class="score-display">
            <span>Score: <b id="quiz-score">0</b></span>
            <span class="combo-badge" id="quiz-combo-badge">Combo x1</span>
          </div>
          <div class="lives-display" id="quiz-lives">
            <!-- Filled via JS with Heart SVGs -->
          </div>
        </div>

        <div class="timer-container">
          <div class="timer-bar" id="quiz-timer-bar"></div>
        </div>

        <div class="word-card-container">
          <div class="word-card glass-panel">
            <span class="pos-badge" id="quiz-word-pos">noun</span>
            <h2 class="quiz-target-word" id="quiz-word">Apple</h2>
            <div class="audio-pronounce-container">
              <button class="audio-btn" id="quiz-speak-btn" title="발음 듣기">
                <svg viewBox="0 0 24 24" width="24" height="24">
                  <path fill="currentColor" d="M3 9v6h4l5 5V4L7 9H3zm13.5 3c0-1.77-1.02-3.29-2.5-4.03v8.05c1.48-.73 2.5-2.25 2.5-4.02zM14 3.23v2.06c2.89.86 5 3.54 5 6.71s-2.11 5.85-5 6.71v2.06c4.01-.91 7-4.49 7-8.77s-2.99-7.86-7-8.77z"/>
                </svg>
                <span>발음 듣기</span>
              </button>
            </div>
          </div>
        </div>

        <div class="options-container">
          <div class="options-grid" id="quiz-options">
            <!-- Created dynamically in JS -->
            <button class="option-btn glass-panel">선택지 1</button>
            <button class="option-btn glass-panel">선택지 2</button>
            <button class="option-btn glass-panel">선택지 3</button>
            <button class="option-btn glass-panel">선택지 4</button>
          </div>
        </div>
      </section>

      <!-- 3. SPELLING MODE SCREEN -->
      <section id="screen-spelling" class="screen">
        <div class="game-header">
          <button class="btn-back" id="spelling-back">
            <svg viewBox="0 0 24 24" width="20" height="20"><path fill="currentColor" d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z"/></svg>
            <span>대시보드로</span>
          </button>
          <div class="score-display">
            <span>Score: <b id="spelling-score">0</b></span>
          </div>
          <div class="lives-display" id="spelling-lives">
            <!-- Hearts -->
          </div>
        </div>

        <div class="spelling-card-container">
          <div class="spelling-card glass-panel">
            <div class="spelling-meaning-container">
              <span class="pos-badge" id="spelling-word-pos">verb</span>
              <h3 class="spelling-korean" id="spelling-meaning">탐험하다</h3>
              <p class="spelling-definition" id="spelling-definition">To travel through an unfamiliar area to learn about it.</p>
            </div>

            <div class="spelling-input-wrapper">
              <!-- Grid of letter slots or single beautiful input -->
              <input type="text" id="spelling-input" class="spelling-input-field" autocomplete="off" placeholder="알맞은 영단어를 타이핑하세요" autofocus>
            </div>

            <div class="spelling-hint-area">
              <button class="btn btn-secondary" id="btn-spelling-hint">
                <svg viewBox="0 0 24 24" width="16" height="16"><path fill="currentColor" d="M9 21c0 .55.45 1 1 1h4c.55 0 1-.45 1-1v-1H9v1zm3-19C8.14 2 5 5.14 5 9c0 2.38 1.19 4.47 3 5.74V17c0 .55.45 1 1 1h6c.55 0 1-.45 1-1v-2.26c1.81-1.27 3-3.36 3-5.74 0-3.86-3.14-7-7-7zm2.85 11.1l-.85.6V16h-4v-2.3l-.85-.6C8.62 12.02 8 10.58 8 9c0-2.21 1.79-4 4-4s4 1.79 4 4c0 1.58-.62 3.02-1.15 4.1z"/></svg>
                힌트 보기 (<span id="spelling-hint-count">3</span>)
              </button>
              <div class="hint-text-display hidden" id="spelling-hint-text">힌트: E _ _ _ _ _ E</div>
            </div>
          </div>
        </div>

        <div class="spelling-submit-area">
          <button class="btn btn-primary btn-block" id="btn-spelling-submit">제출하기</button>
        </div>
      </section>

      <!-- 4. FLASHCARDS SCREEN -->
      <section id="screen-flashcards" class="screen">
        <div class="game-header">
          <button class="btn-back" id="flash-back">
            <svg viewBox="0 0 24 24" width="20" height="20"><path fill="currentColor" d="M20 11H7.83l5.59-5.59L12 4l-8 8 8 8 1.41-1.41L7.83 13H20v-2z"/></svg>
            <span>대시보드로</span>
          </button>
          <div class="flashcard-progress">
            Card <span id="flash-current-index">1</span> of <span id="flash-total-count">15</span>
          </div>
        </div>

        <div class="flashcard-deck">
          <!-- 3D Flip Card Container -->
          <div class="flip-card-wrapper" id="flash-card-trigger">
            <div class="flip-card" id="flash-card">
              <!-- FRONT -->
              <div class="flip-card-front glass-panel">
                <span class="pos-badge" id="flash-front-pos">adjective</span>
                <h2 class="card-word" id="flash-front-word">Beautiful</h2>
                <p class="click-hint">카드를 클릭하여 뜻을 확인하세요</p>
                
                <button class="audio-btn flash-speak-btn" id="flash-speak-front" title="발음 듣기">
                  <svg viewBox="0 0 24 24" width="20" height="20">
                    <path fill="currentColor" d="M3 9v6h4l5 5V4L7 9H3zm13.5 3c0-1.77-1.02-3.29-2.5-4.03v8.05c1.48-.73 2.5-2.25 2.5-4.02z"/>
                  </svg>
                </button>
              </div>
              <!-- BACK -->
              <div class="flip-card-back glass-panel">
                <span class="pos-badge" id="flash-back-pos">adjective</span>
                <h3 class="card-meaning" id="flash-back-meaning">아름다운</h3>
                <div class="card-details">
                  <p class="card-def"><strong>정의:</strong> <span id="flash-back-def">Very pleasing to the senses or to the mind.</span></p>
                  <p class="card-ex"><strong>예문:</strong> <em id="flash-back-ex">The garden is full of beautiful flowers.</em></p>
                </div>
                
                <button class="audio-btn flash-speak-btn" id="flash-speak-back" title="발음 듣기">
                  <svg viewBox="0 0 24 24" width="20" height="20">
                    <path fill="currentColor" d="M3 9v6h4l5 5V4L7 9H3zm13.5 3c0-1.77-1.02-3.29-2.5-4.03v8.05c1.48-.73 2.5-2.25 2.5-4.02z"/>
                  </svg>
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="flashcard-controls">
          <button class="btn btn-secondary" id="btn-flash-prev">
            <svg viewBox="0 0 24 24" width="18" height="18"><path fill="currentColor" d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z"/></svg>
            이전 단어
          </button>
          <button class="btn btn-accent" id="btn-flash-master">
            <svg viewBox="0 0 24 24" width="18" height="18"><path fill="currentColor" d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/></svg>
            암기 완료!
          </button>
          <button class="btn btn-secondary" id="btn-flash-next">
            다음 단어
            <svg viewBox="0 0 24 24" width="18" height="18"><path fill="currentColor" d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/></svg>
          </button>
        </div>
      </section>

    </main>

    <!-- Footer -->
    <footer class="app-footer">
      <p>&copy; 2026 VocaQuest. Built for study and fun.</p>
    </footer>
  </div>

  <!-- MODAL: BACKUP & RESTORE -->
  <div class="modal-overlay" id="modal-backup">
    <div class="modal-content glass-panel">
      <button class="modal-close" id="modal-backup-close">
        <svg viewBox="0 0 24 24" width="24" height="24"><path fill="currentColor" d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z"/></svg>
      </button>
      <h2>학습 데이터 백업 및 복원</h2>
      <p class="modal-desc">컴퓨터실에서 학습 내용이 초기화되는 것을 막기 위해 진도를 백업하거나 다시 불러오세요.</p>
      
      <div class="backup-actions">
        <div class="backup-box">
          <h4>현재 학습 진도 내보내기</h4>
          <p>지금까지 획득한 XP, 최고 콤보, 암기한 단어 통계를 파일로 다운로드합니다.</p>
          <button class="btn btn-primary btn-block" id="btn-export-data">
            <svg viewBox="0 0 24 24" width="18" height="18" style="margin-right:8px;"><path fill="currentColor" d="M19.35 10.04C18.67 6.59 15.64 4 12 4 9.11 4 6.6 5.64 5.35 8.04 2.34 8.36 0 10.91 0 14c0 3.31 2.69 6 6 6h13c2.76 0 5-2.24 5-5 0-2.64-2.05-4.78-4.65-4.96zM17 13l-5 5-5-5h3V9h4v4h3z"/></svg>
            백업 파일 다운로드
          </button>
        </div>

        <div class="backup-divider"></div>

        <div class="backup-box">
          <h4>이전 백업 파일 가져오기</h4>
          <p>저장해 두었던 백업 파일을 업로드하여 이전 상태 그대로 진도를 이어갑니다.</p>
          <div class="file-upload-wrapper">
            <button class="btn btn-secondary btn-block" id="btn-file-trigger">
              파일 선택 및 가져오기
            </button>
            <input type="file" id="backup-file-input" accept=".json,.txt" class="hidden">
          </div>
          <span class="file-status-text" id="import-status">선택된 파일 없음</span>
        </div>
      </div>
    </div>
  </div>

  <!-- MODAL: RESULT SUMMARY -->
  <div class="modal-overlay" id="modal-result">
    <div class="modal-content glass-panel text-center">
      <div class="confetti-container" id="confetti-canvas"></div>
      <h2 id="result-title">도전 완료!</h2>
      <p class="result-subtitle" id="result-subtitle">훌륭한 실력입니다!</p>
      
      <div class="result-stats-container">
        <div class="result-stat-box">
          <span class="res-val" id="res-score">150</span>
          <span class="res-lbl">최종 점수</span>
        </div>
        <div class="result-stat-box">
          <span class="res-val text-orange" id="res-combo">12</span>
          <span class="res-lbl">최대 콤보</span>
        </div>
        <div class="result-stat-box">
          <span class="res-val text-blue" id="res-xp">+45 XP</span>
          <span class="res-lbl">획득한 경험치</span>
        </div>
      </div>

      <div class="result-message" id="result-message">
        새로운 최고 점수를 달성했습니다! 난이도를 높여 도전해보세요.
      </div>

      <div class="modal-buttons">
        <button class="btn btn-primary" id="btn-result-close">대시보드로 돌아가기</button>
      </div>
    </div>
  </div>

  <!-- Background sound activation banner if browser blocks speech/audio -->
  <div class="audio-banner hidden" id="audio-banner">
    <span>더 나은 경험을 위해 오디오와 소리를 허용해 주세요!</span>
    <button class="btn btn-xs" id="btn-audio-allow">확인</button>
  </div>

  <!-- Load script files -->
  <script src="words.js"></script>
  <script src="app.js"></script>
</body>
</html>
