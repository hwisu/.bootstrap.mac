# macOS 개발 환경 자동 설정 스크립트

이 프로젝트는 macOS 개발 환경을 자동으로 구성하는 스크립트 모음입니다. 주요 개발 도구, 에디터 설정, 쉘 설정을 자동화하여 빠르고 일관된 개발 환경을 구축할 수 있습니다.

## 🔍 주요 기능

- **Homebrew**: 패키지 관리자 자동 설치 및 구성
- **개발 도구**: 필수 개발 도구 설치 (Git, Node.js 등)
- **Cursor 에디터**: 설치 및 확장 프로그램 자동 구성
- **Neovim**: 현대적인 설정으로 자동 구성 및 플러그인 설치
- **쉘 도구**: Zsh 플러그인, 테마, 유틸리티 설치
- **Docker**: 개발 컨테이너 환경 구축

## ⚠️ 보안 기능

- Neovim 설치 시 [CVE GHSA-6f9m-hj8h-xjgj](https://github.com/neovim/neovim/security/advisories/GHSA-6f9m-hj8h-xjgj) 취약점 검사 및 방어
- 관리자 권한 사용 전 사용자 확인 (safe_sudo)
- 파일 권한 강화 및 무결성 검증
- 버전 체크 기능으로 최소 요구 버전 확인

## 🚀 시작하기

### 요구 사항

- macOS 11.0 이상
- 관리자 권한
- 인터넷 연결

### 설치

```bash
# 저장소 복제
git clone https://github.com/username/bootstrap.mac.git
cd bootstrap.mac

# 메인 스크립트 실행
./bootstrap.sh
```

## 📦 개별 설치

전체 설정 대신 특정 도구만 설치하려면 다음 스크립트를 개별적으로 실행할 수 있습니다:

```bash
# Neovim 설정만 설치
./setup-nvim.sh

# Cursor 확장 프로그램만 설치
./setup-cursor-extensions.sh
```

## 📋 설치되는 Cursor 확장 프로그램

- **Haskell**: Haskell 언어 지원 및 구문 강조
- **Kanagawa**: 다크 테마
- **Python**: Python 언어 지원, Pylance, 디버깅
- **Rainbow CSV**: CSV 파일 보기 및 편집
- **SQLite Viewer**: SQLite 데이터베이스 관리
- **VSCode Neovim**: Vim 키바인딩 지원

## 🔧 Neovim 설정

기본 설정으로 다음 플러그인이 자동 설치됩니다:

- **lazy.nvim**: 플러그인 관리자
- **lspconfig + mason**: LSP 지원
- **treesitter**: 향상된 구문 강조
- **telescope**: 파일 및 코드 검색
- **kanagawa**: 다크 테마
- **nvim-cmp**: 자동 완성

## 🛡️ 문제 해결

문제가 발생하면 다음 단계를 시도해보세요:

1. 스크립트에서 발생하는 오류 메시지 확인
2. `~/.bootstrap_state` 파일 확인 (설치 상태 추적)
3. 필요한 경우 `rm ~/.bootstrap_state` 명령으로 상태 초기화 후 재시도

### 알려진 문제

- Python 확장 설치 실패 시 Cursor를 직접 실행하여 확장 프로그램 설치

## 📄 라이선스

MIT License - 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 🤝 기여하기

이슈 및 풀 리퀘스트는 환영합니다! 기여하기 전에 코드 스타일 가이드를 확인해주세요.

## 🙏 감사의 말

- 이 프로젝트는 다양한 오픈 소스 도구와 커뮤니티의 도움으로 만들어졌습니다.
