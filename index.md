# LuckyMeter - 걸음수 기반 리워드 앱

## 스토어 앱 설명

**LuckyMeter는 걸을수록 포인트를 획득하고 재미있는 미니게임을 즐길 수 있는 건강 리워드 앱입니다.**
**LuckyMeter와 함께 건강한 걸음 하나하나가 행운으로 바뀌는 경험을 해보세요!**

### 주요 기능
- 🚶‍♂️ **걸음수 추적**: 스마트폰의 건강 센서와 GPS를 활용한 정확한 걸음수 및 거리 측정
- 💰 **포인트 시스템**: 걸음수와 활동량에 따른 포인트 적립
- 🎮 **미니게임**: 사다리타기, 룰렛, 랜덤 숫자 뽑기, 오늘의 운세 등 다양한 게임
- 🛒 **상품 구매**: 적립된 포인트로 실제 상품 구매 가능
- 👥 **초대 시스템**: 친구 초대를 통한 추가 포인트 획득
- 🌍 **다국어 지원**: 한국어, 영어, 힌디어 지원

### 앱의 목적
- **건강한 라이프스타일**: 걷기 활동을 통한 자연스러운 건강 관리
- **실질적인 리워드**: 가상 포인트가 아닌 실제 구매 가능한 상품으로 교환
- **재미있는 게임**: 지루하지 않은 다양한 미니게임으로 즐거움 제공
- **간편한 사용**: 직관적인 UI/UX로 누구나 쉽게 사용 가능

### 앱 미리보기

<table border="0">
 <tr>
    <td><img src="https://i.postimg.cc/SKnx1bd5/iOS-1.jpg" alt="screenshot1" width="100%"></td>
    <td><img src="https://i.postimg.cc/qMrgJYBh/iOS-2.jpg" alt="screenshot2" width="100%"></td>
    <td><img src="https://i.postimg.cc/G3GH1rRn/iOS-3.jpg" alt="screenshot3" width="100%"></td>
 </tr>
 <tr>
    <td><img src="https://i.postimg.cc/T3YwmDDT/iOS-4.jpg" alt="screenshot4" width="100%"></td>
    <td><img src="https://i.postimg.cc/jdh2LXC8/iOS-5.jpg" alt="screenshot5" width="100%"></td>
    <td><img src="https://i.postimg.cc/WzG3mm81/iOS-6.jpg" alt="screenshot6" width="100%"></td>
 </tr>
</table>

---

## 프로젝트 전체 소개

### 🏗️ **LuckyMeter - Flutter 건강 리워드 앱**

LuckyMeter는 사용자의 걸음수와 신체 활동을 추적하여 포인트를 제공하고, 다양한 미니게임과 실제 상품 구매 기능을 통해 건강한 라이프스타일을 장려하는 종합 헬스케어 리워드 플랫폼입니다.

### 🔧 **기술 스택**
- **프레임워크**: Flutter (Dart)
- **상태관리**: Riverpod (Provider에서 마이그레이션)
- **백엔드**: Firebase (Firestore, Storage, Core)
- **아키텍처**: Clean Architecture (Domain-driven design)
- **주요 기능**:
  - Health API를 통한 걸음수 추적
  - Geolocator를 통한 GPS 위치 기반 거리 측정
  - Google Mobile Ads 광고 통합
  - JSON 직렬화를 통한 데이터 관리
  - 다국어 지원 (한국어/영어/힌디어)

### 📱 **핵심 기능**

1. **건강 추적 시스템**
   - 실시간 걸음수 모니터링
   - GPS 기반 거리 및 경로 추적
   - 일별/주별/월별 활동 통계

2. **포인트 리워드 시스템**
   - 걸음수 기반 포인트 적립
   - 활동량에 따른 차등 보상
   - 포인트 히스토리 관리

3. **미니게임 플랫폼**
   - 사다리타기 게임
   - 룰렛 게임  
   - 랜덤 숫자 뽑기
   - 오늘의 운세

4. **쇼핑 시스템**
   - 포인트를 활용한 실제 상품 구매
   - 구매 내역 관리
   - 상품 상세 정보 제공

5. **소셜 기능**
   - 친구 초대 시스템
   - 초대 기록 추적

### 🏛️ **아키텍처 구조**

```
lib/
├── core/                    # 핵심 비즈니스 로직 및 공통 기능
│   ├── data/repositories/   # 데이터 저장소 구현체
│   ├── domain/repositories/ # 저장소 인터페이스
│   └── providers.dart       # 핵심 Riverpod 프로바이더
├── features/                # 기능별 모듈화
│   ├── auth/               # 인증 (로그인, 회원가입)
│   ├── member/             # 회원 관리 및 프로필
│   ├── activity/           # 활동 추적 및 상태
│   ├── games/              # 미니게임 모음
│   ├── item/               # 상품 관리 및 구매
│   └── point_history/      # 포인트 거래 내역
└── shared/                 # 공통 위젯 및 유틸리티
    ├── constants/          # 앱 상수 (색상, 값, 정규식)
    ├── utils/              # 유틸리티 함수들
    └── widgets/            # 재사용 가능한 UI 컴포넌트
```

### 🔄 **데이터 플로우**
1. **Presentation Layer**: 화면 및 위젯 (Riverpod 상태 관리)
2. **Domain Layer**: 비즈니스 로직 및 저장소 인터페이스
3. **Data Layer**: Firebase/로컬 저장소 구현체

### 🚀 **개발 환경 설정**
- Flutter SDK 3.8.0+
- Firebase 프로젝트 설정 (rupeewalk)
- 필수 권한: 건강 데이터, 위치 정보, 네트워크
- 빌드 명령어: `dart run build_runner build` (모델 변경 시)

### 🌐 **글로벌 지원**
- 다국어 지원 (ARB 파일 기반)
- 지역별 맞춤형 콘텐츠
- 현지화된 사용자 경험

### 📋 **개발 명령어**

#### Core Development
- `flutter run` - Run the app in development mode
- `flutter test` - Run all tests
- `flutter analyze` - Run static analysis and linting
- `dart run build_runner build` - Generate JSON serialization code (required after model changes)
- `flutter gen-l10n` - Generate localization files from ARB files

#### Building for Release
- `flutter build apk --release` - Build Android APK
- `flutter build appbundle --release` - Build Android App Bundle
- `flutter build ios --release` - Build iOS release
