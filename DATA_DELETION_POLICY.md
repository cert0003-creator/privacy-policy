# 데이터 삭제 정책 (Data Deletion Policy)

## 개요
Past Life View는 사용자의 개인정보 보호 권리를 존중합니다. 사용자는 언제든지 자신의 계정과 데이터를 삭제할 수 있습니다.

## 수집되는 데이터

### 1. 계정 정보
- Google 계정 이메일 주소
- Google 사용자 ID
- OAuth 인증 토큰

### 2. 게임 데이터
- 레벨 진행 상황
- 획득한 별과 코인
- 일일 도전 기록
- 게임 설정 (음향, 진동 등)
- 구매 내역

### 3. 저장 위치
- **로컬 저장소**: 기기의 AsyncStorage에 게임 진행 상황 저장
- **클라우드 저장소**: Firebase Firestore에 동기화된 게임 데이터 저장
- **인증 데이터**: Firebase Authentication에 계정 정보 저장

## 계정 및 데이터 삭제 방법

### 앱 내에서 삭제

1. 앱을 실행합니다
2. 설정 화면으로 이동합니다
3. '계정' 섹션으로 스크롤합니다
4. **'⚠️ 계정 및 데이터 삭제'** 버튼을 누릅니다
5. 2단계 확인 과정을 거칩니다
6. 최종 확인 후 모든 데이터가 삭제됩니다

### 삭제되는 항목

계정 삭제 시 다음 항목이 **영구적으로** 삭제됩니다:

✅ Google 계정 연동 해제  
✅ Firebase Authentication에서 계정 삭제  
✅ Firestore에 저장된 모든 게임 데이터  
✅ 기기에 저장된 로컬 게임 데이터  
✅ 구매 내역 및 획득한 아이템  
✅ 일일 도전 기록  

### 삭제 소요 시간

- **즉시 삭제**: 계정 삭제 요청 시 모든 데이터가 즉시 삭제됩니다
- **백업 삭제**: Firebase의 백업 시스템에서도 30일 이내에 완전히 삭제됩니다

### 복구 불가 안내

⚠️ **중요**: 삭제된 데이터는 복구할 수 없습니다.
- 게임 진행 상황
- 획득한 코인과 아이템
- 구매 내역
- 모든 업적 및 기록

## 데이터 삭제 요청 대체 방법

앱에 접근할 수 없는 경우, 다음 방법으로 데이터 삭제를 요청할 수 있습니다:

### 이메일 요청
**이메일**: [cert0003@gmail.com]  
**제목**: 계정 및 데이터 삭제 요청  
**내용**:
- Google 계정 이메일 주소
- 삭제 요청 사유 (선택사항)
- 본인 확인 정보

### 처리 기간
- 이메일 요청: 영업일 기준 **7일 이내** 처리
- 처리 완료 시 확인 이메일 발송

## Google Play Store 데이터 보안 정책 준수

본 앱은 Google Play Store의 데이터 보안 정책을 준수합니다:

- ✅ 사용자가 쉽게 계정을 삭제할 수 있는 방법 제공
- ✅ 앱 내에서 직접 삭제 가능
- ✅ 삭제 프로세스가 명확하고 투명함
- ✅ 2단계 확인으로 실수 방지
- ✅ 삭제되는 데이터의 범위를 명확히 안내

## 데이터 보관 정책

- **활성 계정**: 데이터는 계정이 활성 상태인 동안 보관됩니다
- **비활성 계정**: 3년간 로그인하지 않은 계정은 자동으로 삭제될 수 있습니다 (사전 통지)
- **삭제 요청**: 사용자 요청 시 즉시 삭제

## 데이터 이동성

삭제 전 데이터 백업을 원하시는 경우:

1. 앱 내 '설정' → '클라우드 동기화' → '데이터 내보내기' (향후 추가 예정)
2. 또는 support@example.com으로 데이터 사본 요청

## 개인정보 보호 담당자

**문의처**: [cert0003@egmail.com]  
**회사명**: [인피니트랩]  
**주소**: [인천시 남동구 인주대로614번길 2]  

## 정책 업데이트

본 정책은 2025년 10월 20일에 마지막으로 업데이트되었습니다.

---

## For Google Play Console - Data Safety Section

### Data Collection Summary
- **Account Info**: Email address, User ID (via Google OAuth)
- **Game Progress**: Levels, coins, achievements
- **Purchase History**: In-app purchases (if applicable)

### Data Usage
- All data is used solely for game functionality and cloud sync
- No data is shared with third parties
- No data is used for advertising

### Data Deletion
- **In-app deletion**: Available in Settings → Account → Delete Account and Data
- **Email request**: [your-support-email@example.com]
- **Processing time**: Immediate (in-app) or within 7 business days (email)
- **Scope**: Complete deletion of all user data from all systems

### Security
- Data encrypted in transit (HTTPS/TLS)
- Firebase Security Rules applied
- OAuth 2.0 authentication
- No sensitive data stored locally without encryption

---

## 개발자 체크리스트

### Google Play Console 설정 시

1. **데이터 보안 섹션**
   - [ ] "데이터를 수집하거나 공유합니까?" → 예
   - [ ] 수집 데이터 유형 선택: 계정 정보, 앱 활동
   - [ ] 데이터 사용 목적: 앱 기능, 계정 관리
   - [ ] 데이터 암호화: 예
   - [ ] 사용자가 데이터 삭제를 요청할 수 있습니까? → 예
   - [ ] 데이터 삭제 방법 URL 또는 이메일 입력

2. **앱 콘텐츠**
   - [ ] 개인정보처리방침 URL 입력
   - [ ] 데이터 삭제 정책 링크 제공

3. **추가 정보**
   - [ ] OAuth 클라이언트 ID 승인
   - [ ] SHA-1 인증서 지문 등록
   - [ ] Firebase 프로젝트 연동 확인

### 주의사항

⚠️ 실제 배포 전에 다음 정보를 업데이트하세요:
- [ ] `[your-support-email@example.com]` → 실제 지원 이메일
- [ ] `[Your Company Name]` → 실제 회사명
- [ ] `[Your Company Address]` → 실제 주소
- [ ] 개인정보처리방침 웹페이지 URL 준비

