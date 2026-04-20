---
marp: true
theme: default
paginate: true
style: |
  /* ── 기본 레이아웃 ── */
  section {
    background: #FFFFFF;
    color: #1C1C1C;
    font-family: 'Noto Sans KR', 'Apple SD Gothic Neo', 'Malgun Gothic', sans-serif;
    font-size: 22px;
    padding: 48px 64px 64px;
    line-height: 1.6;
  }

  /* SKT 레드 상단 라인 */
  section::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 5px;
    background: #E51537;
  }

  /* 페이지 번호 */
  section::after {
    font-size: 14px;
    color: #AAAAAA;
  }

  /* 헤더 */
  h1 { font-size: 36px; color: #1C1C1C; margin-bottom: 16px; border-bottom: 2px solid #E51537; padding-bottom: 8px; }
  h2 { font-size: 28px; color: #1C1C1C; margin-bottom: 12px; }
  h3 { font-size: 22px; color: #E51537; margin-bottom: 8px; }

  /* 불릿 */
  ul { margin: 0; padding-left: 24px; }
  ul li { margin-bottom: 10px; }
  ul li::marker { color: #E51537; }
  ul ul li::marker { color: #888888; }

  /* 강조 */
  strong { color: #E51537; }
  em { color: #555555; font-style: normal; font-weight: 500; }

  /* 인용 (중요 강조) */
  blockquote {
    border-left: 4px solid #E51537;
    background: #FFF5F5;
    padding: 10px 16px;
    margin: 8px 0;
    color: #555555;
    font-size: 0.95em;
    border-radius: 0 4px 4px 0;
  }

  /* 코드 */
  code {
    background: #F5F5F5;
    padding: 2px 7px;
    border-radius: 4px;
    font-size: 0.85em;
    color: #C7254E;
    font-family: 'D2Coding', 'Fira Code', 'Courier New', monospace;
  }
  pre {
    background: #1C1C1C;
    border-left: 5px solid #E51537;
    padding: 16px 20px;
    border-radius: 0 6px 6px 0;
    overflow: hidden;
  }
  pre code { background: transparent; color: #F0F0F0; padding: 0; }

  /* 표 */
  table { width: 100%; border-collapse: collapse; margin-top: 12px; font-size: 0.9em; }
  th { background: #E51537; color: #FFFFFF; padding: 10px 14px; text-align: left; }
  td { border: 1px solid #E0E0E0; padding: 9px 14px; }
  tr:nth-child(even) td { background: #F9F9F9; }

  /* ── 타이틀 슬라이드 ── */
  section.title {
    background: linear-gradient(135deg, #1C1C1C 0%, #2D2D2D 100%);
    color: #FFFFFF;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 64px;
  }
  section.title::before { background: #E51537; height: 6px; }
  section.title h1 { font-size: 44px; color: #FFFFFF; border-bottom: none; margin-bottom: 12px; }
  section.title h2 { font-size: 24px; color: #E51537; border: none; }
  section.title p { color: #BBBBBB; font-size: 18px; margin-top: 32px; }

  /* ── 섹션 구분 슬라이드 ── */
  section.part {
    background: #E51537;
    color: #FFFFFF;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
  }
  section.part::before { background: rgba(255,255,255,0.3); }
  section.part h1 { font-size: 52px; color: #FFFFFF; border-bottom: 2px solid rgba(255,255,255,0.4); padding-bottom: 12px; }
  section.part h2 { font-size: 24px; color: rgba(255,255,255,0.85); margin-top: 8px; }

  /* ── 정리/요약 슬라이드 ── */
  section.summary { background: #F9F9F9; }
  section.summary h1 { color: #E51537; }

  /* ── 경고/주의 슬라이드 ── */
  section.warning { background: #FFF8E1; }
  section.warning h1 { color: #FF6F00; }

  /* ── 두 컬럼 레이아웃 ── */
  .cols { display: grid; grid-template-columns: 1fr 1fr; gap: 32px; margin-top: 12px; }
  .cols-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 24px; margin-top: 12px; }
  .box { background: #F5F5F5; padding: 16px; border-radius: 6px; border-top: 3px solid #E51537; }
  .box-green { background: #F1F8E9; border-top-color: #43A047; padding: 16px; border-radius: 6px; }
  .box-orange { background: #FFF3E0; border-top-color: #FB8C00; padding: 16px; border-radius: 6px; }
  .box-red { background: #FFEBEE; border-top-color: #E51537; padding: 16px; border-radius: 6px; }

  /* 배지 */
  .badge-ok { background: #E8F5E9; color: #2E7D32; border: 1px solid #43A047; padding: 2px 10px; border-radius: 12px; font-size: 0.85em; }
  .badge-warn { background: #FFF8E1; color: #F57F17; border: 1px solid #FFC107; padding: 2px 10px; border-radius: 12px; font-size: 0.85em; }
  .badge-no { background: #FFEBEE; color: #C62828; border: 1px solid #E53935; padding: 2px 10px; border-radius: 12px; font-size: 0.85em; }
  /* URL 링크 (슬라이드 우측 하단) */
  .url-link {
    position: absolute;
    bottom: 22px;
    right: 64px;
    font-size: 12px;
  }
  .url-link a {
    color: #AAAAAA;
    text-decoration: none;
    letter-spacing: 0.01em;
  }
  .url-link a:hover { color: #E51537; }
---

<!-- _class: title -->
<!-- _paginate: false -->

# 오픈소스 가이드
## 사용 · 기여 · 공개 · 공급망 보안

기업 개발자를 위한 실무 오픈소스 교육

<!--
이 교육 자료는 기업 내 개발자가 오픈소스를 올바르고 안전하게 활용하기 위한 실무 지식을 다룹니다.
라이선스 컴플라이언스, 오픈소스 기여, 공개, SBOM을 포함한 공급망 보안을 다룹니다.
각 PART는 독립적으로 학습할 수 있으며, 전체를 순서대로 따라가면 오픈소스 활동의 전체 흐름을 이해할 수 있습니다.
-->

---


# 왜 오픈소스인가?

- *"If software is eating the world, open source is eating the software world."*
- 현대 애플리케이션 코드의 **70~90%는 오픈소스 컴포넌트**로 구성
- 오픈소스 없이 제품·서비스 개발은 사실상 불가능한 시대
- 기업이 직면한 핵심 과제 3가지:
  - ① 라이선스 컴플라이언스
  - ② 보안 취약점(CVE) 관리
  - ③ 소프트웨어 공급망 보안

<div class="url-link"><a href="https://sktelecom.github.io/guide/">sktelecom.github.io/guide</a></div>

<!--
오픈소스는 이미 기업 소프트웨어 개발의 핵심 인프라입니다. 단순히 사용하는 것에 그치지 않고 기여하고 공개하는 기업이 늘어나고 있습니다.
이 교육은 오픈소스를 올바르고 안전하게 활용하기 위한 실무 지식을 다룹니다.
-->

---


# 이 가이드의 구성

1. **PART 1 — 사용하기 (Consume)**
   외부 오픈소스를 제품·서비스에 올바르게 쓰는 법

2. **PART 2 — 기여하기 (Contribute)**
   외부 오픈소스 프로젝트에 코드·문서를 기여하는 법

3. **PART 3 — 공개하기 (Release)**
   사내 소프트웨어를 오픈소스로 공개하는 법

4. **PART 4 — 공급망 보안 (Supply Chain Security)**
   SBOM 관리와 취약점 대응

<div class="url-link"><a href="https://sktelecom.github.io/guide/">sktelecom.github.io/guide</a></div>

<!--
네 가지 주제는 서로 독립적으로 학습할 수도 있고, 순서대로 따라가면 오픈소스 활동의 전체 흐름을 이해할 수 있습니다.
각 파트는 기업의 법적 리스크 최소화와 생태계 기여 극대화를 목표로 합니다.
-->

---


# OSPO란 무엇인가?

- **OSPO** (Open Source Program Office)
  기업 내 오픈소스 정책·절차를 수립하고 지원하는 전담 조직
- 역할:
  - 구성원의 오픈소스 사용·기여·공개 안내
  - 저작권·라이선스·보안 문제 사전 예방
  - 법적 리스크 검토 및 승인 프로세스 운영
- 주요 참고 표준: **OpenChain** (ISO/IEC 5230), **SPDX** (ISO/IEC 5962), **CycloneDX**

<div class="url-link"><a href="https://sktelecom.github.io/about/ospo/">sktelecom.github.io/about/ospo</a></div>

<!--
OSPO는 오픈소스 활동에서 발생하는 저작권·라이선스·보안 문제를 사전에 방지하는 역할을 합니다.
규모에 따라 전담 조직이 없더라도 법무팀 또는 보안팀과 협력하는 유사 체계를 갖추는 것이 중요합니다.
모호한 판단이 필요한 경우에는 언제나 OSPO 또는 법무팀에 먼저 문의하는 습관이 중요합니다.
-->

---

<!-- _class: part -->
<!-- _paginate: false -->

# PART 1
## 오픈소스 사용하기 (Consume)

<!--
이 파트에서는 외부 오픈소스 소프트웨어를 제품·서비스에 활용할 때 알아야 할 라이선스 지식과 컴플라이언스 프로세스를 다룹니다.
-->

---


# 오픈소스란? — 정의와 법적 책임

- **오픈소스**: 라이선스를 통해 복사·수정·사용·재배포를 자유롭게 허용한 소프트웨어
- OSI(Open Source Initiative)가 인증한 라이선스 80여 개
- **GitHub Public ≠ 오픈소스**: 라이선스 없으면 저작권자 독점 상태 → 사용 금지
  - Fork/열람만 허용, 사용·배포 권리는 별도 라이선스 필요
- 라이선스 위반 시: 사용 권리 박탈 → 제품 판매 중단 → 법적 소송

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/">sktelecom.github.io/guide/use</a></div>

<!--
가장 흔한 오해는 "GitHub에 공개된 코드는 자유롭게 써도 된다"는 것입니다. 이는 사실이 아닙니다.
라이선스가 없는 코드는 저작권자의 독점 상태이므로, 반드시 명시된 라이선스를 확인해야 합니다.
라이선스 위반은 단순한 규정 위반을 넘어 제품 출시 중단, 법적 소송으로 이어질 수 있습니다.
-->

---


# 오픈소스 선택 시 5가지 체크포인트

| 항목 | 확인 내용 |
|------|-----------|
| **① 품질** | GitHub Star/Fork 수, 기능·성능·호환성 검증 |
| **② 커뮤니티** | 활성도, Issue 관리 현황, 업데이트 주기 |
| **③ 문서화** | 도입 용이성과 기여 가능성 판단 기준 |
| **④ 보안취약점** | CVE 데이터베이스에서 알려진 취약점 확인 |
| **⑤ 라이선스** | 의무사항 파악 및 준수 가능 여부 사전 검토 |

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/choose/">sktelecom.github.io/guide/use/choose</a></div>

<!--
수년 전에 커뮤니티 활동이 멈춘 오픈소스는 보안 패치를 기대할 수 없어 위험합니다.
특히 라이선스는 도입 후에 발견하면 이미 제품 설계 변경이 어려워지므로 반드시 선택 단계에서 확인해야 합니다.
이 5가지 항목 중 하나라도 문제가 있다면 도입을 재고하거나 대안을 탐색하는 것이 좋습니다.
-->

---


# 소프트웨어 지식재산권 — 저작권 vs 특허권

<div class="cols">
<div class="box">

**저작권 (Copyright)**
- 창작과 동시에 **자동 발생**
- 코드 표현(실질적 유사성) 보호
- 고용 중 창작물 → **회사 소유**
- 별도 등록 불필요

</div>
<div class="box">

**특허권 (Patent)**
- 출원·심사·**등록 필요**
- 알고리즘·기능의 아이디어 보호
- 직무발명 규정 적용
- 명시적 허여 없으면 사용 불가

</div>
</div>

> ※ 고용 기간에 만든 코드의 저작권은 **회사 소유** → 임의로 외부에 기여하면 저작권 침해

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/license/">sktelecom.github.io/guide/use/license</a></div>

<!--
저작권과 특허권의 차이를 이해하면 오픈소스 라이선스의 법적 의미를 훨씬 명확히 파악할 수 있습니다.
특히 Apache-2.0처럼 명시적 특허 허여 조항이 있는 라이선스가 왜 기업 친화적인지 이해하는 데 중요한 배경 지식입니다.
구성원이 회사 저작물을 무단으로 오픈소스에 기여하면 저작권 침해 이슈가 발생하므로 반드시 승인 절차를 따라야 합니다.
-->

---


# 오픈소스 라이선스란?

- **라이선스** = 저작자가 타인에게 부여하는 사용 허가증
- 오픈소스 라이선스 3가지 목적:
  - ① 자유로운 사용·수정·배포 권리 부여
  - ② 저작자 법적 보호
  - ③ 커뮤니티 공동 발전
- "로열티 없음" 대신 → **지켜야 할 의무사항** 있음
- **라이선스 없는 코드 = 오픈소스 아님** → 사용 금지

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/license/">sktelecom.github.io/guide/use/license</a></div>

<!--
오픈소스 라이선스는 '공짜 소프트웨어'가 아닙니다. 금전적 대가 대신 고지, 소스코드 공개 등의 의무를 이행해야 합니다.
라이선스 종류마다 요구하는 의무가 다르므로 각각의 특성을 파악하는 것이 중요합니다.
라이선스가 명시되지 않은 코드는 저작권자가 모든 권리를 보유하는 독점 상태이므로 사용 자체가 불가능합니다.
-->

---


# 라이선스 주요 의무사항 3가지

1. **저작권 표시 및 라이선스 고지**
   거의 모든 라이선스 요구 (MIT, Apache-2.0, BSD 등)

2. **소스코드 공개**
   GPL 계열 Copyleft — 바이너리 배포 시 소스코드 함께 제공

3. **재배포 시 동일 라이선스 적용 (Copyleft)**
   결합된 코드에도 같은 라이선스 적용 요구

```
낮음 ◀── Permissive ── Weak Copyleft ── Copyleft ── Network Copyleft ──▶ 높음
         (고지만) (모듈 공개) (전체 공개) (네트워크 포함)
```

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
의무사항의 핵심은 '얼마나 많은 코드를 공개해야 하는가'입니다.
Permissive 라이선스는 고지문 하나로 해결되지만, GPL은 결합된 자사 코드까지 공개해야 하므로 설계 단계부터 주의가 필요합니다.
의무 강도 스펙트럼을 기억하면 라이선스 선택과 사용 판단에 도움이 됩니다.
-->

---


# 의무 발생 시점 — "재배포"란?

> 대부분의 의무사항은 **외부 재배포(redistribute) 시에만** 발생한다.

| 재배포 해당 (의무 발생) | 재배포 비해당 (의무 없음) |
|--------------------------|---------------------------|
| 앱스토어 배포 | 사내 개발 도구 |
| 고객사 납품 소프트웨어 | 내부 테스트·빌드 환경 |
| 외부 SaaS 서비스 제공 | 사내 전용 운영 서비스 |
| 3rd Party 제공 | 개인 학습·실험 |

**판단 기준**: "소프트웨어를 외부에 전달하는가?" → YES이면 의무 준수 필요

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
많은 팀이 사내에서 사용하는 오픈소스에 대해 불필요하게 걱정합니다. 의무는 외부 배포 시에 발생하므로 사내 도구·테스트 환경은 자유롭게 활용할 수 있습니다.
단, SaaS 형태로 외부 사용자에게 서비스하는 경우는 반드시 확인이 필요하며, 특히 AGPL은 네트워크 서비스도 '배포'로 간주합니다.
경계가 모호한 경우에는 항상 법무팀 또는 OSPO에 문의하는 것이 안전합니다.
-->

---


# 오픈소스 라이선스 확인 방법

**수동 확인 우선순위:**

```
① 소스 파일 상단 주석 →  ② LICENSE/COPYING 파일 →  ③ README/웹사이트
```

충돌 시: **파일 상단 주석이 최우선** 기준

**자동화 도구:**

| 도구 | 용도 |
|------|------|
| **Syft** | SBOM 생성 + 라이선스 추출 |
| **Trivy** | 취약점 + 라이선스 스캔 |
| **FOSSology** | 파일 단위 상세 스캔 |

> ※ Trivy: 2025년 공급망 공격 피해 → GitHub Actions에서 `@latest` 금지, 버전 고정 필수

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/check/">sktelecom.github.io/guide/use/check</a></div>

<!--
대규모 프로젝트에서 수백 개 의존성을 수동으로 확인하는 것은 현실적으로 불가능합니다.
Syft나 Trivy 같은 자동화 도구를 CI/CD 파이프라인에 통합하여 라이선스 확인을 자동화하는 것을 권장합니다.
2025년 Trivy 공급망 공격 사례처럼 도구 자체의 보안도 주의해야 합니다.
-->

---


# 라이선스 분류 ① — Public Domain & Permissive

<div class="cols">
<div class="box-green">

**Public Domain**
- CC0, Unlicense
- 아무 조건 없이 자유 사용
- 저작권 자체를 포기

</div>
<div class="box-green">

**Permissive**
- MIT, Apache-2.0, BSD-2/3
- **고지 의무만** 준수하면 자유 사용
- 소스코드 공개 불필요
- 상용 소프트웨어와 결합 가능

</div>
</div>

**Apache-2.0 특징**: 명시적 **특허 허여 조항** 포함 → 기업 사용 시 가장 권장

의무 준수 방법: 오픈소스 고지문 작성 후 배포 시 동봉 (About 페이지, NOTICE 파일 등)

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
Permissive 라이선스는 기업 입장에서 가장 다루기 쉬운 유형입니다.
제품의 About 페이지나 별도 고지 파일에 저작권과 라이선스 내용을 포함하면 의무를 충족할 수 있습니다.
Apache-2.0은 특허 관련 분쟁을 예방하는 조항이 포함되어 있어 특히 기업 환경에서 권장됩니다.
-->

---


# 라이선스 분류 ② — Weak Copyleft

- 대표 라이선스: **LGPL-2.1/3.0, MPL-2.0, EPL-2.0, CDDL-1.0**
- 소스코드 공개는 요구하지만, 공개 범위가 제한적 (해당 모듈·파일만)
- **LGPL 핵심 전략**: Dynamic Link(동적 링크) 방식 사용 시 자사 코드 공개 의무 없음
  - Static Link(정적 링크) → 오브젝트 코드 제공 의무 발생
  - Java JAR import는 파생저작물로 간주하지 않음

> ※ **GPL-3.0 / LGPL-3.0 + 임베디드 기기**: 사용자가 소프트웨어를 재설치할 수 있도록 **설치 정보**까지 제공 의무 → 실무적으로 불가능한 경우 많음 → 임베디드 제품에 사용 제한

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
LGPL 라이브러리를 Static Link로 포함하면 자사 코드도 공개해야 하지만, Dynamic Link 방식으로 분리하면 LGPL 라이브러리 부분만 공개하면 됩니다.
임베디드 제품 개발 시에는 GPL-3.0/LGPL-3.0 사용에 특히 주의가 필요합니다.
MPL-2.0은 파일 단위 Copyleft라서 수정한 파일만 공개하면 되어 상용 소프트웨어 친화적입니다.
-->

---


# 라이선스 분류 ③ — Copyleft & Network Copyleft

**Copyleft (GPL-2.0 / GPL-3.0)**
- 결합한 자사 코드 **전체**를 동일 라이선스로 공개 요구
- 파생저작물: 수정 코드, 동일 프로세스 모듈, 링크된 라이브러리, 상속 클래스
- 설계 원칙: 빌드 시 통합 금지, 런타임에서도 독립 프로세스로 동작

<div class="box-red">

**[금지] Network Copyleft — AGPL-3.0 사용 절대 금지**

네트워크를 통한 서비스 제공도 '배포'로 간주 → **SaaS/API 서버에 사용 시 서버 코드 전체 공개 의무** 발생
클라우드·서버 서비스 개발 시 AGPL 라이브러리 사용 금지

</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
GPL은 설계 단계부터 오픈소스와 자사 코드의 경계를 명확히 해야 합니다.
AGPL은 클라우드 시대에 더욱 위험한 라이선스입니다. 바이너리를 배포하지 않더라도 네트워크 서비스 제공만으로 소스코드 공개 의무가 발생하기 때문입니다.
AGPL 소프트웨어는 사전에 법무팀 또는 OSPO와 반드시 협의해야 합니다.
-->

---


# 라이선스 분류 ④ — Source Available · 제한 · AI 모델

| 유형 | 대표 라이선스 | 주요 제한 | 기업 적용 |
|------|-------------|----------|----------|
| Source Available | SSPL, BSL, Elastic-2.0 | 상업적 SaaS 제한, OSI 미승인 | 사전 법적 검토 필수 |
| 비상업 | CC-BY-NC | 기업 활동 전체가 상업적 | 기업 사용 불가 |
| 광고 의무 | BSD-4-Clause | 모든 광고에 특정 문구 삽입 | 사용 제한 |
| AI 모델 | Llama 2, RAIL, CreativeML | 용도 제한·책임 조항 | 반드시 별도 검토 |

> SSPL: 서비스 운영에 사용하는 **전체 인프라** 소스코드 공개 → 사실상 불가능

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
MongoDB의 SSPL이나 Elastic의 Elastic-2.0은 소스코드가 공개되어 있어 오픈소스처럼 보이지만, 상업적 SaaS 서비스 제공에 강력한 제한을 가합니다.
AI 모델 라이선스는 군사·감시 등 특정 용도를 명시적으로 금지하는 새로운 유형이므로 AI 서비스 개발 시 반드시 확인해야 합니다.
Llama 2는 MAU 7억 명 초과 시 Meta와 별도 협의가 필요하며, 경쟁 LLM 학습에 사용이 금지됩니다.
-->

---

<!-- _class: summary -->

# 라이선스 정책 요약

<div class="cols-3">
<div class="box-green">

**자유 사용**

Public Domain (CC0)
MIT
Apache-2.0
BSD-2-Clause / BSD-3-Clause

고지문 준수 시 제약 없음

</div>
<div class="box-orange">

**※ 조건부 사용**

LGPL (Dynamic Link 권장)
MPL-2.0
EPL-2.0
GPL-2.0/3.0 (코드 분리 설계)

담당자 검토 후 사용

</div>
<div class="box-red">

**사용 금지 / 검토 필수**

AGPL (SaaS/네트워크 서비스)
SSPL · BSL · Elastic-2.0
CC-BY-NC (비상업)
AI 모델 라이선스

반드시 법무/OSPO 문의

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
이 표는 현장에서 빠르게 참조할 수 있는 기준입니다.
경계가 모호한 경우에는 절대 독단적으로 판단하지 말고 반드시 사전 검토를 거쳐야 합니다.
특히 AGPL과 Source Available 라이선스는 사전 지식 없이 사용했다가 큰 피해를 입는 사례가 많습니다.
-->

---


# 오픈소스 컴플라이언스 프로세스

```
① 오픈소스 목록 확정
   (개발·설계 단계에서 사용할 컴포넌트 결정)
        ↓
② 라이선스 확인 및 의무사항 검토
   (수동 또는 자동화 도구 활용)
        ↓
③ 법무/OSPO 점검 요청
   (불확실한 경우 반드시 사전 검토)
        ↓
④ 오픈소스 고지문 발급
        ↓
⑤ 배포 시 고지문 동봉
   (Copyleft: 소스코드 또는 서면 약정서 제공)
```

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/">sktelecom.github.io/guide/use</a></div>

<!--
컴플라이언스는 배포 직전이 아닌 개발 초기 단계부터 관리해야 합니다.
뒤늦게 라이선스 문제를 발견하면 설계 변경까지 이어질 수 있습니다.
모바일 앱은 About 페이지를 활용하는 것이 일반적인 고지 방법입니다.
-->

---


# 오픈소스 보안 취약점 점검

- **CVE** (Common Vulnerabilities and Exposures): 알려진 취약점 표준 데이터베이스
- **CVSS 심각도 등급**: Critical / High / Medium / Low

**자동화 도구:**

| 도구 | 특징 |
|------|------|
| GitHub Dependabot | 저장소 의존성 자동 모니터링 |
| Trivy | 컨테이너·파일시스템 취약점 스캔 |
| Syft | SBOM 생성으로 취약점 분석 기반 확보 |

**대응 원칙**: Critical/High → 즉시 패치 버전 업그레이드 또는 **완화 조치 문서화**

핵심: 도입 시 1회 점검이 아닌 **지속적 모니터링** 체계 구축

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/">sktelecom.github.io/guide/use</a></div>

<!--
취약점 점검은 도입 시 1회로 끝나지 않습니다. 오픈소스 사용 중에도 새로운 CVE가 발표되므로 지속적인 모니터링 체계를 갖추는 것이 중요합니다.
패치가 불가능한 경우에는 실제 서비스에 영향이 없는 이유를 소명서로 문서화해야 합니다.
Dependabot을 활성화하면 GitHub 저장소에서 자동으로 취약한 의존성을 감지하고 업데이트 PR을 생성해 줍니다.
-->

---

<!-- _class: summary -->

# PART 1 핵심 정리 — 오픈소스 사용 10계명

<div class="cols">
<div>

① GitHub Public ≠ 오픈소스
② 라이선스 없는 코드 = 사용 금지
③ 재배포 시에만 의무 발생
④ Permissive: 고지문으로 해결
⑤ LGPL: Dynamic Link 전략

</div>
<div>

⑥ GPL: 설계부터 코드 분리
⑦ AGPL: SaaS 절대 사용 금지
⑧ AI 모델 라이선스: 별도 검토
⑨ CVE 지속 모니터링 체계 구축
⑩ 모르면 법무/OSPO에 먼저 문의

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/">sktelecom.github.io/guide/use</a></div>

<!--
PART 1에서 배운 내용을 10개 원칙으로 요약했습니다. 모든 내용을 외울 필요는 없지만, 경계가 모호할 때 혼자 판단하지 말고 반드시 전문가에게 문의하는 습관이 가장 중요합니다.
라이선스 정책은 프로젝트마다 다를 수 있으므로 조직의 정책 문서를 항상 최신 상태로 유지하는 것도 중요합니다.
-->

---

<!-- _class: part -->
<!-- _paginate: false -->

# PART 2
## 오픈소스 기여하기 (Contribute)

<!--
이 파트에서는 외부 오픈소스 프로젝트에 기여하는 방법과 기업 내 승인 절차, 좋은 기여자가 되기 위한 원칙을 다룹니다.
-->

---


# 기업이 오픈소스에 기여해야 하는 이유

- **유지 관리 비용 절감**
  기여 안 하면 신규 버전마다 자체 패치 재적용 반복 → 비용 기하급수 증가
- **프로젝트 방향에 영향력 행사**
  필요한 기능 직접 제안·개발 → 원하는 방향으로 프로젝트 성장 유도
- **우수 인재 채용**
  오픈소스 커뮤니티에서 좋은 평판 → 뛰어난 개발자 자연스럽게 유입
- **협력 게임 이론**
  협력하면 모든 참가자가 투자 이상의 가치 창출 (존 내쉬)

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/benefit/">sktelecom.github.io/guide/contribute/benefit</a></div>

<!--
많은 기업이 기여는 '좋은 일'이라고 생각하지만 실제로는 비즈니스 관점에서 매우 합리적인 투자입니다.
패치를 기여하지 않으면 새 버전이 나올 때마다 같은 작업을 반복해야 하고, 이 비용은 시간이 지날수록 기하급수적으로 늘어납니다.
기여는 의무가 아닌 기업의 지속가능한 오픈소스 활용을 위한 전략입니다.
-->

---


# 개발자가 기여해야 하는 이유

- **실력 향상**: 버전 관리, Unit Test, CI/CD 등 현업 최고의 실습 환경
- **기술 심화 이해**: 이슈 분석·해결로 오픈소스 내부 동작 깊이 파악
- **글로벌 포트폴리오**: 모든 기여 이력이 GitHub에 공개 → 이력서보다 강력
- **인맥 형성**: 전 세계 개발자와 협업, 다양한 문화권과 소통 경험
- **리더십 경험**: 팀 구성, 갈등 해결, 우선순위 조정 등 실전 리더십

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/benefit/">sktelecom.github.io/guide/contribute/benefit</a></div>

<!--
오픈소스 커뮤니티는 초보자의 실수에 비교적 관대하여 안전하게 실력을 키울 수 있는 공간입니다.
기여 이력은 GitHub에 영구적으로 남아 이력서보다 강력한 포트폴리오가 됩니다.
첫 기여를 망설이고 있다면, 오타 수정이나 문서 번역처럼 작은 것부터 시작하는 것을 권장합니다.
-->

---


# 오픈소스 기여 유형 — 코드 외에도 다양하다

<div class="cols">
<div class="box">

**문서·번역**
튜토리얼, 뉴스레터
자국어 번역, API 문서

**테스트·이슈**
기능 테스트, 버그 리포트
빌드/설치 테스트, API 검증

**디자인**
웹사이트 레이아웃
스타일 가이드, 로고

</div>
<div class="box">

**코드·리뷰**
버그 수정, 신기능 추가
PR 리뷰, 자동화 개선
멘토링

**마케팅·이벤트**
SNS 홍보, 컨퍼런스 발표
밋업·워크숍 기획

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/background/type/">sktelecom.github.io/guide/contribute/background/type</a></div>

<!--
개발자가 아니어도 기여할 수 있습니다. 번역, 문서 개선, 버그 리포트만으로도 프로젝트에 큰 도움이 됩니다.
특히 첫 기여라면 간단한 오류 수정이나 문서 번역으로 시작하는 것이 좋습니다.
코드 기여보다 문서와 테스트 기여가 더 환영받는 프로젝트도 많습니다.
-->

---


# 오픈소스 프로젝트 멤버십 구조

```
         ┌─────────────────┐
         │ 리더 │  프로젝트 방향·최종 결정
         └────────┬────────┘ (개인 또는 운영위원회)
                  │
         ┌────────▼────────┐
         │ 메인테이너 │  특정 영역 위임 관리
         └────────┬────────┘
                  │
         ┌────────▼────────┐
         │ 커미터 │  특정 모듈 Merge 권한
         └────────┬────────┘
                  │
         ┌────────▼────────┐
         │ 기여자 │  버그 수정·문서화 기여
         └────────┬────────┘
                  │
         ┌────────▼────────┐
         │ 사용자 │  버그 리포트·기능 제안
         └─────────────────┘ ← 가장 중요한 역할
```

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/background/membership/">sktelecom.github.io/guide/contribute/background/membership</a></div>

<!--
역할 구조를 이해하면 기여 시 누구에게 어떤 방식으로 접근해야 할지 알 수 있습니다.
처음에는 기여자로 시작해 커밋 이력이 쌓이면 커미터, 메인테이너로 성장하는 경로를 밟습니다.
사용자 역할도 프로젝트 성공에 필수적이며, 좋은 버그 리포트 하나가 많은 사람에게 도움이 됩니다.
-->

---


# 프로젝트 주요 문서 — 기여 전 필독

| 문서 | 내용 | 기여 전 중요도 |
|------|------|--------------|
| **README** | 소개·설치·사용 방법 | 필독 |
| **LICENSE** | 오픈소스 라이선스 명시 | 없으면 기여 불필요 |
| **CONTRIBUTING** | 기여 절차·코딩 스타일·PR 방법 | **기여자 필독** |
| **CODE OF CONDUCT** | 커뮤니티 행동 강령 | 없으면 기여 재고 |

> CONTRIBUTING 없이 PR을 보내면 기여가 거절될 확률이 높습니다.
> 항상 프로젝트가 원하는 방식대로 기여해야 수락 가능성이 높아집니다.

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/background/document/">sktelecom.github.io/guide/contribute/background/document</a></div>

<!--
CONTRIBUTING 파일은 프로젝트마다 요구사항이 다르므로 반드시 먼저 읽어야 합니다.
코딩 스타일, 커밋 메시지 형식, 테스트 요구사항 등을 미리 파악해야 리뷰 사이클을 줄일 수 있습니다.
CODE OF CONDUCT가 없는 프로젝트는 커뮤니티 문화가 불건전할 가능성이 있으므로 기여 전 주의가 필요합니다.
-->

---


# 기여할 프로젝트 선택 체크리스트

- **LICENSE 파일**이 있는가? (없으면 오픈소스 아님 → 기여 불필요)
- **최근 Commit**이 있고 기여자가 활발한가?
- **Issue**가 신속히 처리되고 Close되고 있는가?
- **PR**에 활발한 토론과 정기적 Merge가 이루어지는가?
- 메인테이너가 **기여에 감사 표시**를 하고 커뮤니티가 친절한가?

> 체크리스트를 통과하지 못하는 프로젝트에 공들인 기여를 보내도
> 아무 응답을 받지 못할 수 있습니다.

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/background/good-project/">sktelecom.github.io/guide/contribute/background/good-project</a></div>

<!--
기여할 프로젝트 선택은 기여 결과에 큰 영향을 미칩니다.
관리되지 않는 프로젝트에 공들인 기여를 보내도 아무 응답을 못 받을 수 있습니다.
체크리스트를 통해 사전에 프로젝트의 건강도를 확인하면 시간과 노력을 효율적으로 투자할 수 있습니다.
-->

---


# 좋은 기여자가 되기 위한 원칙

- **커뮤니티 채널 가입 먼저**: Slack, 포럼, 메일링 리스트에 가입하고 문화 파악
- **거버넌스 문서 읽기**: 누가 어떻게 의사결정하는지 이해
- **작은 것부터 시작**: 오타·버그 수정 → 문서 개선 → 기능 추가 순으로 확대
- **초기부터 자주 기여**: 대량 코드를 한 번에 보내면 수락 어려움
- **이벤트 참가**: 컨퍼런스·밋업으로 관계 형성
- **아이디어 단계에서 논의**: 대형 기여 전 커뮤니티와 방향 사전 합의

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/background/good-contributor/">sktelecom.github.io/guide/contribute/background/good-contributor</a></div>

<!--
새 프로젝트에 참여할 때는 항상 관찰 기간을 갖는 것이 좋습니다. 커뮤니티 문화를 이해한 후 기여하면 수락 가능성이 훨씬 높아집니다.
아이디어 단계에서 커뮤니티와 먼저 논의하면 방향이 맞지 않는 기여를 사전에 방지할 수 있습니다.
작고 빠른 기여 여러 개가 크고 완벽한 기여 하나보다 커뮤니티에서 더 환영받는 경우가 많습니다.
-->

---


# 기업 오픈소스 기여 Rule

<div class="cols">
<div class="box">

**승인 받기**
조직 내부 승인 + OSPO 리뷰 필수
(고용 중 저작물은 회사 소유)

**권리 있는 코드만**
직접 작성한 코드만 기여
3rd Party 코드 임의 기여 금지

**지식재산 보호**
민감 정보·특허 코드 기여 금지
모호하면 OSPO에 먼저 문의

</div>
<div class="box">

**CLA 서명 주의**
저작권 양도 조항 포함 CLA는
법무/OSPO 검토 후 서명

**저작권 표시**
`Copyright [연도] [회사명]`
SPDX 태그 사용

**회사 이메일 사용**
개인 이메일이 아닌
회사 이메일로 기여

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/rule/">sktelecom.github.io/guide/contribute/rule</a></div>

<!--
기여 Rule은 기업의 지식재산을 보호하기 위한 최소한의 안전장치입니다.
특히 CLA 서명 시 저작권 양도 조항이 있는지 꼭 확인해야 합니다.
한 번 OSPO 승인을 받은 프로젝트는 이후 동일 프로젝트에 대한 기여는 개인 재량으로 진행할 수 있습니다.
-->

---


# CLA vs DCO — 기여자 동의 방식 비교

| | **CLA** | **DCO** |
|--|---------|---------|
| 방식 | 별도 약정서 서명 | 커밋 메시지 한 줄 추가 |
| 저작권 | 양도 가능성 있음 | 양도 없음 |
| 복잡도 | 높음 | 낮음 |
| 특징 | 라이선스 변경 유연성 확보 | 기여 장벽 최소화 |
| 적합 | 기업 주도 대형 프로젝트 | 빠른 기여, 커뮤니티 프로젝트 |

**DCO 사용 예시:**
```bash
git commit -s -m "fix: resolve null pointer in auth module"
# Signed-off-by: 홍길동 <gildong@company.com>
```

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/rule/">sktelecom.github.io/guide/contribute/rule</a></div>

<!--
Linux Kernel, Git 등 많은 프로젝트가 DCO를 채택하고 있습니다.
CLA는 프로젝트의 라이선스 변경 유연성을 높이지만, 기업 구성원이 서명하기 전에 반드시 저작권 양도 조항 여부를 확인해야 합니다.
CLA Assistant 같은 도구를 활용하면 GitHub PR 단계에서 자동으로 CLA 서명을 관리할 수 있습니다.
-->

---


# 기업 내 오픈소스 기여 절차

```
STEP 1 소속 조직 내부 승인
        (담당 임원·리더 승인)
           ↓
STEP 2 OSPO Review 요청
        (프로젝트명·라이선스·기여 목적 포함)
           ↓
STEP 3 프로젝트 문서 검토
        (CONTRIBUTING, CLA/DCO, 코딩 스타일)
           ↓
STEP 4 기여 Rule 준수 확인
        (저작권 표시, 회사 이메일, 지식재산 점검)
           ↓
STEP 5 Issue / PR 생성으로 기여 제출
```

> **예외**: 10라인 이하 수정, Stack Overflow 답변, GitHub 이슈 관리 → 별도 승인 불필요

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/process/">sktelecom.github.io/guide/contribute/process</a></div>

<!--
절차가 복잡해 보이지만, 한 번 OSPO 승인을 받은 프로젝트는 이후 같은 프로젝트에 대한 기여는 간소화됩니다.
10라인 이하의 간단한 코드 수정이나 Stack Overflow 답변은 별도 승인 없이 기여 가능합니다.
기여 전 프로젝트의 CONTRIBUTING 파일을 반드시 읽어 프로젝트별 요구사항을 확인해야 합니다.
-->

---


# 기여 제출 — Issue와 Pull Request

**GitHub 기여 워크플로우:**

```
이전 이슈 확인 → Issue 생성 → Fork → Clone
→ Branch 생성 → 코드 작업 → Commit → Push
→ Pull Request 오픈 → Feedback 대응
```

**Feedback 유형별 대응:**

| 응답 유형 | 대응 방법 |
|----------|----------|
| 응답 없음 (1주일+) | 정중하게 Follow-up 댓글 |
| 수정 요청 | 즉시 대응, 질문 있으면 명확히 확인 |
| 거절 | 이유 확인 후 다음 기여에 반영 |
| 수락 | 커뮤니티에 기여 성공! |

> **팁**: WIP(Work In Progress) PR을 일찍 오픈해 방향 사전 확인

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/process/submit/">sktelecom.github.io/guide/contribute/process/submit</a></div>

<!--
Pull Request는 작업이 완전히 끝나지 않아도 WIP로 일찍 오픈하여 방향이 맞는지 사전에 확인하는 것이 좋습니다.
거절을 두려워하지 말고, 거절 이유를 분석해 다음 기여의 품질을 높이는 기회로 활용하세요.
이전에 같은 이슈가 이미 논의된 경우가 많으므로 이슈 검색을 먼저 하는 것이 중요합니다.
-->

---


# 커뮤니케이션 에티켓

| 나쁜 예 | 좋은 예 |
|-----------|-----------|
| "X가 안 돼요" | "Y 작업 중 X가 동작하지 않습니다. OS: macOS 14, 버전: 2.1.0, 재현 방법: ..." |
| 모르면 바로 질문 | README·이슈 확인 후 질문 (노력했음을 보여주기) |
| 개인 이메일로 연락 | Issue·Comment로 공개 소통 (모두에게 도움) |
| 길고 복잡한 요청 | 핵심만 담아 간결하게 |
| 결정에 불복 | 커뮤니티 결정 존중, 이견 시 Fork 고려 |

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/background/communication/">sktelecom.github.io/guide/contribute/background/communication</a></div>

<!--
오픈소스 커뮤니티는 전 세계 다양한 문화권 사람들이 모입니다. 상대방의 글은 항상 좋은 의도라고 가정하고 품위 있게 소통하는 것이 장기적인 관계 형성에 중요합니다.
공개 채널에서의 소통은 같은 문제를 겪는 다른 사람들에게도 도움이 됩니다.
메인테이너들은 매우 바쁘므로 간결하고 명확한 요청이 빠른 응답을 받는 데 도움이 됩니다.
-->

---

<!-- _class: summary -->

# PART 2 핵심 정리 — 기여 성공의 3원칙

1. **규칙 먼저**
   조직 승인 → OSPO 리뷰 → CLA/DCO 확인 → 기여 제출

2. **작게 시작**
   오타·문서 수정 → 버그 수정 → 기능 추가 → 아키텍처 제안

3. **커뮤니티 존중**
   문화 파악 → 공개 소통 → 결정 수용 → 장기적 관계 형성

> 기여는 단발 이벤트가 아닌 **장기적 관계 구축**입니다.
> 꾸준히 기여하면 커미터 → 메인테이너로 성장할 수 있습니다.

<div class="url-link"><a href="https://sktelecom.github.io/guide/contribute/">sktelecom.github.io/guide/contribute</a></div>

<!--
PART 2에서 배운 핵심은 기여가 기술적 행위인 동시에 사회적 행위라는 점입니다.
좋은 코드를 작성하는 것만큼이나 커뮤니티와 잘 소통하는 것이 기여 성공의 핵심입니다.
한 번의 기여로 끝내지 말고, 꾸준히 기여하면서 신뢰를 쌓아가는 것이 중요합니다.
-->

---

<!-- _class: part -->
<!-- _paginate: false -->

# PART 3
## 오픈소스 공개하기 (Release)

<!--
이 파트에서는 기업 내부 소프트웨어를 오픈소스로 공개하는 방법과 절차, 공개 후 커뮤니티 운영 방법을 다룹니다.
-->

---


# 공개의 혜택 — 자선이 아닌 투자

<div class="cols">
<div class="box-green">

**경제적 이득**
오픈소스는 자선이 아닌 투자
생태계 확산으로 더 높은 ROI
(Angular → 70만 개 일자리 창출)

**표준 선점**
해당 분야 사실상 표준 확보
(예: Linux → 서버·임베디드 표준)

</div>
<div class="box-green">

**생태계 성장**
외부 개발자의 확장 개발 활성화
(예: V8 엔진 → Node.js 생태계)

**우수 인재 채용**
도구에 이미 익숙한 개발자 채용
교육 비용 절감 + 기업 명성 향상

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/benefit/">sktelecom.github.io/guide/release/benefit</a></div>

<!--
존 내쉬의 협력 게임 이론처럼, 오픈소스는 모든 참가자가 협력함으로써 투자 이상의 수익을 창출하는 구조입니다.
Google이 Angular를 오픈소스로 공개한 것처럼, 내부 도구를 공개하면 외부 생태계가 만들어 주는 가치가 훨씬 더 클 수 있습니다.
기업 명성 향상으로 우수한 개발자가 '이 도구를 만든 회사에서 일하고 싶다'는 동기로 지원하게 됩니다.
-->

---


# 공개 전 체크 — 공개할 가치가 있는가?

- **차별화 가치**: 커뮤니티에 기존 프로젝트와 다른 가치를 제공하는가?
- **실제 사용 코드**: 제품·서비스에 실제로 사용 중인 코드인가?
  *(미사용 코드 공개는 커뮤니티 신뢰 저하)*
- **유사 프로젝트 확인**: 이미 존재한다면 → 새 공개보다 기존 프로젝트 기여가 더 효율적
- **지속 관리 가능성**: 인력·예산·장기적 의지가 있는가?

<div class="box-red">

※ **경고**: 리소스 없이 공개하면 프로젝트는 빠르게 죽는다
방치된 오픈소스 프로젝트는 기업 이미지에 부정적 영향

</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/rule/">sktelecom.github.io/guide/release/rule</a></div>

<!--
매력없는 코드를 반복해서 공개하면 나중에 좋은 코드를 공개해도 개발자들이 관심을 갖지 않습니다.
공개는 시작이 아닌 장기적인 커밋이므로, 충분한 준비 없이 공개하는 것은 오히려 역효과입니다.
"공개하지 않는 것이 낫다"는 결론도 충분히 유효한 의사결정입니다.
-->

---


# 기업 오픈소스 공개 Rule

- **승인 받기**: 내부 승인 + OSPO 리뷰 필수 — 임의 공개는 저작권 침해
- **권리 있는 코드만**: 모든 코드 출처 확인, 문제 소지 코드 삭제
- **지식재산 보호**: 민감 정보·특허 코드 제외 (git history까지 확인)
- **품질·유용성**:
  - 수준 이하 코드 공개 금지
  - 커뮤니티에 실제로 유용한 코드만 공개
  - 미사용 코드 공개 지양
- **리소스 확보**: 개발자·법무·마케팅·인프라 예산 없으면 공개 보류
- **회사 이메일**: 기업 활동임을 명확히 하고 책임감 강화

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/rule/">sktelecom.github.io/guide/release/rule</a></div>

<!--
공개 Rule은 기업의 지식재산을 보호하는 동시에 오픈소스 커뮤니티의 신뢰를 유지하기 위한 기준입니다.
완벽한 코드가 아니어도 공개할 수 있지만, 최소한 제품에 실제로 사용하는 수준의 품질은 갖춰야 합니다.
git history에 민감한 정보가 포함되어 있는지도 반드시 확인해야 합니다.
-->

---


# 오픈소스 공개 절차 전체 흐름

```
① 승인·의사결정
  조직 승인 → OSPO 지원 요청
  → 이름 / 라이선스(기본: Apache-2.0) / CLA·DCO 결정
        ↓
② 코드 준비·점검
  3rd Party 정리 → 저작권 SPDX 표시
  → 불필요 주석·정보 제거 → 보안·라이선스 점검
        ↓
③ 인프라·거버넌스·문서화
  GitHub 저장소 설정 → 역할 정의
  → README / CONTRIBUTING / CODE OF CONDUCT 작성
        ↓
④ 공개·마케팅·커뮤니티 활성화
  OSPO 리뷰 → 공개 → 블로그·컨퍼런스 홍보
  → Good First Issue 라벨 → 기여자 유입
```

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/">sktelecom.github.io/guide/release/process</a></div>

<!--
11단계의 절차처럼 보이지만 핵심은 '코드 정리·라이선스 결정·문서화·커뮤니티 운영' 4가지입니다.
특히 공개 후 커뮤니티 관리가 지속되지 않으면 프로젝트는 금방 사라지게 됩니다.
OSPO의 지원을 적극 활용하면 절차를 훨씬 효율적으로 진행할 수 있습니다.
-->

---


# 라이선스 선택 — 기본은 Apache-2.0

- **기업 공개 오픈소스 기본 라이선스**: **Apache-2.0**
- **이유**:
  - 명시적 **특허 허여 조항** 포함 → 기여자·사용자 특허 분쟁 방지
  - 광범위한 사용 자유 + 기업 친화적
  - GPL-3.0과 호환 (GPL-2.0과는 비호환)

| 상황 | 권장 라이선스 |
|------|------------|
| 기본 | Apache-2.0 |
| 커뮤니티 표준이 다른 경우 | 해당 표준 (예: Node.js → MIT) |
| GPL 의존성이 있는 경우 | GPL-2.0 또는 GPL-3.0 |

> 참고 도구: [choosealicense.com](https://choosealicense.com)

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/">sktelecom.github.io/guide/release/process</a></div>

<!--
Apache-2.0은 특허 허여 조항 덕분에 기여자와 사용자 모두를 특허 분쟁에서 보호합니다.
MIT는 더 간단하지만 특허 관련 조항이 없어 기업 소프트웨어에는 Apache-2.0이 더 안전한 선택입니다.
커뮤니티 표준이 있는 경우에는 그 표준을 따르는 것이 외부 기여자 유입에 유리합니다.
-->

---


# 코드 준비 체크리스트

- [ ] 3rd Party 코드 출처 확인 및 문제 소지 코드 삭제
- [ ] **SPDX 태그**로 모든 소스 파일 상단에 저작권·라이선스 표시
- [ ] 사내 정보·개인정보·내부 시스템 정보 주석 및 **git history 제거**
- [ ] 저장소 루트에 **LICENSE 파일** 배치
- [ ] 포함된 오픈소스 의존성 라이선스 의무사항 확인
- [ ] **CVE 취약점 점검** 및 Critical/High 조치 완료

> 가장 흔한 실수: 내부 주석에 서버 주소, API 키, 동료 이름이 남아 있는 경우
> git log / git blame으로 history 전체 검토 필수

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/">sktelecom.github.io/guide/release/process</a></div>

<!--
공개 전 코드 정리에서 가장 많이 실수하는 부분은 내부 주석에 사내 정보가 남아 있는 경우입니다.
git history까지 포함해 민감 정보가 없는지 꼼꼼히 확인해야 하며, git-secrets나 truffleHog 같은 도구를 활용할 수 있습니다.
취약점이 있는 의존성을 포함한 채로 공개하면 커뮤니티 신뢰를 잃게 됩니다.
-->

---


# 파일 내 저작권·라이선스 표시 (SPDX)

**표준 방법**: SPDX Tag 사용 — Linux Foundation 권장 방식

```python
# SPDX-FileCopyrightText: Copyright 2025 회사명
# SPDX-License-Identifier: Apache-2.0
```

```java
// SPDX-FileCopyrightText: Copyright 2025 회사명
// SPDX-License-Identifier: Apache-2.0
```

- 모든 소스 파일 상단에 적용
- 자동화 도구: **`addlicense`**, **`autogen`** — 배치 적용 가능
- SPDX ID 목록: [spdx.org/licenses](https://spdx.org/licenses/)
- 장점: 기계 파싱 가능, Syft·FOSSology 등 라이선스 분석 도구와 호환

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/copyright/">sktelecom.github.io/guide/release/process/copyright</a></div>

<!--
SPDX Tag 방식은 기계가 자동으로 파싱할 수 있어 라이선스 분석 도구와의 호환성이 높습니다.
새 파일을 생성할 때마다 자동으로 헤더를 추가하는 훅(hook)을 개발 환경에 설정해두면 편리합니다.
저작권 연도는 파일 최초 작성 연도를 사용하며, 수정 연도를 추가하는 것도 권장됩니다.
-->

---


# 프로젝트 이름 결정 원칙

- **기억하기 쉽고** 프로젝트 목적을 나타낼 것
  *(예: Sentry=감시·추적, Thin=가볍고 간단)*
- **중복 확인**: 같은 생태계 내 동일·유사 이름 프로젝트 사전 검색
- **피해야 할 것**:
  - 기업 브랜드명 포함 (독립 오픈소스로 오해)
  - 타사 브랜드·상표 포함 ("Java Test Library" → "Test Library for Java" )
  - 상표권 침해
- **사전 확보**: 도메인·GitHub 조직·SNS 계정 미리 확보
- **상표권 검색**: Kipris (국내), WIPO (글로벌)

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/name/">sktelecom.github.io/guide/release/process/name</a></div>

<!--
이름 선택은 단순해 보이지만 나중에 바꾸기 매우 어렵습니다.
특히 상표권 침해는 나중에 법적 분쟁으로 이어질 수 있으므로, 공개 전에 반드시 상표권 검색을 해야 합니다.
도메인과 SNS 계정도 미리 확보하지 않으면 나중에 다른 사람이 선점할 수 있습니다.
-->

---


# 개발 환경·거버넌스·문서화

<div class="cols-3">
<div class="box">

**인프라**
GitHub 저장소
CI/CD 파이프라인
웹사이트 (선택)
커뮤니케이션 채널
(Slack, Discord 등)

</div>
<div class="box">

**거버넌스**
역할 공개
(리더/메인테이너/커미터)
CODE OF CONDUCT
의사결정 프로세스
문서화

</div>
<div class="box">

**문서화**
README
(소개·Quick Start)
CONTRIBUTING
(절차·스타일·CLA/DCO)
CHANGELOG
API 문서

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/">sktelecom.github.io/guide/release/process</a></div>

<!--
문서화는 커뮤니티 진입 장벽을 낮추는 가장 중요한 요소입니다.
README가 빈약하면 외부 개발자는 프로젝트를 이해하지 못하고 떠나버립니다.
Good First Issue 라벨을 활용하면 초보 기여자의 진입을 도울 수 있습니다.
-->

---


# 공개 후 커뮤니티 운영

- **마케팅**: 기술 블로그 포스팅, 컨퍼런스 발표, 개발자 커뮤니티 등록
- **기여자 관리**:
  - PR·Issue 신속 대응 (최대 1~2주 이내)
  - 기여자에게 감사 표현
  - `good first issue` 라벨로 초보자 진입 유도
- **지속 성장**:
  - 정기 릴리즈 일정 유지
  - 로드맵 공개 (커뮤니티 방향 공유)
  - 커미터 승진 제도 운영

<div class="box-red">

※ **핵심 원칙**: PR이 몇 달째 리뷰 없이 방치되면 기여자들이 떠나고 프로젝트는 죽는다
최소한 PR 리뷰에 응답할 수 있는 **전담 담당자**를 반드시 지정할 것

</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/process/">sktelecom.github.io/guide/release/process</a></div>

<!--
오픈소스 공개 후 가장 많이 실패하는 이유는 커뮤니티 관리 리소스 부족입니다.
PR이 몇 달째 리뷰 없이 방치되면 기여자들이 떠나고 프로젝트는 죽어버립니다.
공개 직후 6개월이 커뮤니티 형성의 황금 기간이므로 이 시기에 집중적으로 투자하는 것이 중요합니다.
-->

---

<!-- _class: summary -->

# PART 3 핵심 정리 — 공개 성공의 4가지 요소

1. **가치**
   커뮤니티에 차별화된 가치를 제공하는가? 실제로 사용하는 코드인가?

2. **품질·법적 준비**
   보안·라이선스 점검 완료? Apache-2.0, SPDX 표시, 상표권 확인?

3. **문서·거버넌스**
   README / CONTRIBUTING / CODE OF CONDUCT 완비?
   역할 분담과 의사결정 프로세스 명확히 정의?

4. **지속성**
   커뮤니티 관리 전담 인력 확보? 장기적 의지와 예산?

> 오픈소스 공개는 단기 이벤트가 아닌 **장기 프로젝트**입니다.

<div class="url-link"><a href="https://sktelecom.github.io/guide/release/">sktelecom.github.io/guide/release</a></div>

<!--
오픈소스 공개는 준비 없이 서두르지 말고, 리소스와 의지가 충분할 때 공개하는 것이 커뮤니티와 기업 모두에 좋은 결과를 가져옵니다.
4가지 요소 중 하나라도 부족하면 공개를 미루거나, 부족한 부분을 먼저 해결하는 것이 낫습니다.
-->

---

<!-- _class: part -->
<!-- _paginate: false -->

# PART 4
## 소프트웨어 공급망 보안
## Supply Chain Security

<!--
이 파트에서는 소프트웨어 공급망 공격의 개념과 사례, SBOM의 정의와 활용, 공급망 보안 규제 동향을 다룹니다.
-->

---


# 소프트웨어 공급망 공격이란?

<div class="cols">
<div class="box">

**전통적 공격**

```
공격자
  ↓
최종 기업 직접 공격
  ↓
피해 (1개 기업)
```

탐지·방어 가능

</div>
<div class="box-red">

**공급망 공격**

```
공격자
  ↓
신뢰받는 소프트웨어
업데이트·개발 도구 오염
  ↓
하류 기업 동시 감염
```

탐지 어려움, 피해 광범위

</div>
</div>

- 정식 서명된 소프트웨어조차 안전하지 않음
- 방화벽·백신으로 탐지 어려움
- 공통 컴포넌트 하나 오염 = **수만~수억 시스템 동시 피해**

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/overview/">sktelecom.github.io/guide/supply-chain/overview</a></div>

<!--
공급망 공격은 직접 공격이 아닌 우회 공격입니다. 개발자가 매일 사용하는 라이브러리나 빌드 도구를 오염시키는 방식으로, 보안이 철저한 기업도 방어하기 어렵습니다.
이 때문에 사용하는 모든 소프트웨어 구성요소를 파악하고 관리하는 것이 필수입니다.
-->

---

<!-- _class: warning -->

# 주요 공급망 공격 사례

| 사례 | 연도 | 공격 방법 | 피해 규모 |
|------|------|----------|----------|
| **SolarWinds** | 2020 | 정상 업데이트에 백도어 삽입 | 미국 정부·기업 18,000개 |
| **Log4Shell** | 2021 | Log4j 취약점 (CVE-2021-44228) | 수억 대 디바이스 노출 |
| **3CX** | 2023 | 직원 PC 해킹 → 개발환경 침투 → 바이너리 변조 | VoIP 앱 사용자 전체 |
| **Trivy** | 2025 | 릴리즈 태그 재지정 → 악성 Docker 이미지 | CI/CD 파이프라인 |

> **Log4Shell의 교훈**: SBOM이 있었다면 영향받는 시스템을 즉시 파악할 수 있었다.
> SBOM 없이 수개월간 혼란 지속.

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/overview/">sktelecom.github.io/guide/supply-chain/overview</a></div>

<!--
Log4Shell 사태는 SBOM의 중요성을 전 세계에 알린 결정적 사건입니다.
SBOM이 있었다면 영향받는 시스템을 즉시 파악할 수 있었지만, 대부분의 기업이 어디에 Log4j가 쓰이는지조차 몰라 수개월간 혼란이 지속됐습니다.
2025년 Trivy 공격은 CI/CD에서 사용하는 도구 자체도 공급망 공격의 대상이 됨을 보여주었습니다.
-->

---


# 왜 공급망 보안이 중요한가?

- 현대 애플리케이션 코드의 **70~90%는 오픈소스 컴포넌트** → 의존성 폭발적 증가
- 하나의 공통 컴포넌트 오염 = 전 세계적 피해 파급
- 빌드·개발 단계 오염 코드는 **방화벽·백신으로 탐지 불가**

**공급망 보안 3대 관리:**

<div class="cols-3">
<div class="box">

**① 투명성**
SBOM으로 모든 구성요소 파악

</div>
<div class="box">

**② 취약점**
CVE 관리로 알려진 위협 제거

</div>
<div class="box">

**③ 무결성**
빌드 환경·도구 자체의 보안 확보

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/">sktelecom.github.io/guide/supply-chain</a></div>

<!--
소프트웨어 의존성 그래프는 점점 복잡해지고 있습니다. 내가 직접 쓰는 라이브러리만이 아니라, 그 라이브러리가 의존하는 라이브러리까지 파악해야 합니다.
SBOM은 이 복잡한 의존성을 투명하게 문서화하는 도구입니다.
3대 관리 중 하나라도 소홀히 하면 공급망 보안의 약한 고리가 됩니다.
-->

---


# 글로벌 규제 동향

| 규제 | 주체 | 핵심 요구사항 |
|------|------|--------------|
| **EO 14028** (2021) | 미국 연방 정부 | 연방 납품 기업 SBOM 제출 의무화, NIST SSDF 준수 |
| **Cyber Resilience Act** (CRA) | EU | CE 마크 인증, 5년 보안 업데이트, 24h 취약점 신고 |
| **SW 공급망 보안 가이드라인** | 한국 | SBOM 도입 권고, 역할별 보안 활동 정의 |

**추세**: 법적 의무화 방향으로 **빠르게 전개** → 선제적 대응 필수

> SolarWinds 사태 이후 미국은 국가 안보 차원에서 공급망 보안을 강제화.
> 글로벌 비즈니스를 하는 기업은 이러한 규제를 반드시 준수해야 합니다.

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/overview/regulations/">sktelecom.github.io/guide/supply-chain/overview/regulations</a></div>

<!--
SolarWinds 사태 이후 미국은 국가 안보 차원에서 공급망 보안을 강제화하기 시작했습니다.
EU도 CRA를 통해 디지털 제품의 전체 생명주기 보안을 법제화했습니다.
현재 권고 수준인 한국도 법제화 방향으로 움직이고 있으므로 선제적 대응이 필요합니다.
-->

---


# 기업 공급망 보안 정책 3대 원칙

<div class="cols-3">
<div class="box">

**원칙 1**
**SBOM 제출 의무화**

모든 납품 소프트웨어에
CycloneDX v1.3+ 또는
SPDX v2.2+ 형식
SBOM 제출

</div>
<div class="box-orange">

**원칙 2**
**취약점 점검 및 조치**

납품 전 CVE 자체 점검
Critical: **7일** 이내 대응
High: **30일** 이내 대응
불가 시 소명서 제출

</div>
<div class="box-red">

**원칙 3**
**투명한 변경 관리**

구성요소 변경 시
갱신된 SBOM 즉시 제출
라이선스 의무 준수 보증

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/overview/policy/">sktelecom.github.io/guide/supply-chain/overview/policy</a></div>

<!--
이 세 가지 원칙은 공급망의 투명성을 확보하고 알려진 취약점으로부터 고객을 보호하기 위한 최소한의 기준입니다.
패치가 불가능한 취약점은 왜 실제 서비스에 영향이 없는지 소명서를 통해 증명해야 합니다.
공급사 입장에서는 계약 전부터 SBOM 생성 체계를 갖추는 것이 중요합니다.
-->

---


# SBOM이란? — Software Bill of Materials

> **SBOM**: 소프트웨어를 구성하는 모든 컴포넌트·라이브러리·모듈과
> 의존성 관계를 기술한 **정형화된 명세서**

**비유**: 제조업의 부품 목록(BOM)을 소프트웨어에 적용

```
음식 재료 목록 →    알레르기 확인, 성분 표시
소프트웨어 SBOM →    취약점 확인, 라이선스 표시
```

**SBOM이 답하는 질문:**
*"우리 제품에 어떤 오픈소스가 어떤 버전으로 들어있나?"*

**핵심 구성 요소:**
- 컴포넌트 정보 (이름·버전·공급자·라이선스)
- 고유 식별자 (PURL, CPE)
- 의존성 관계 (직접·전이적)
- 메타데이터 (생성 시점·도구 정보)

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/sbom/what-is-sbom/">sktelecom.github.io/guide/supply-chain/sbom/what-is-sbom</a></div>

<!--
SBOM을 식재료 목록에 비유하면 이해하기 쉽습니다. 음식에 어떤 재료가 들어갔는지 모르면 알레르기 대응도 안전 점검도 할 수 없습니다.
소프트웨어도 마찬가지로 구성요소를 모르면 취약점 발생 시 즉각 대응이 불가능합니다.
Log4Shell 사태가 SBOM의 필요성을 전 세계에 각인시킨 사건이었습니다.
-->

---


# SBOM 주요 구성요소 — PURL과 전이적 의존성

**PURL (Package URL)** — 컴포넌트 고유 식별 표준:

```
pkg:maven/org.springframework/spring-core@5.3.20
pkg:npm/express@4.18.2
pkg:pypi/django@4.1.0
pkg:golang/github.com/gin-gonic/gin@1.9.0
```

**의존성 유형:**

| 유형 | 설명 | SBOM 포함 여부 |
|------|------|--------------|
| 직접 의존성 | 프로젝트가 직접 선언 | 필수 |
| **전이적 의존성** | 의존성의 의존성 | ** 반드시 포함** |

> **핵심**: 빌드(패키지 설치) **완료 후** SBOM 생성해야 전이적 의존성 포함

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/for-suppliers/requirements/">sktelecom.github.io/guide/supply-chain/for-suppliers/requirements</a></div>

<!--
전이적 의존성이 중요한 이유는 Log4Shell처럼 개발자가 직접 사용하지 않은 라이브러리에서 취약점이 발생하는 경우가 많기 때문입니다.
직접 의존성만 포함된 SBOM은 절반의 정보만 담고 있어 실질적인 보안 분석이 어렵습니다.
npm install, mvn package 등 빌드 명령어 실행 후에 SBOM을 생성해야 전이적 의존성이 정확히 포함됩니다.
-->

---


# SBOM의 4가지 활용 가치

<div class="cols">
<div>

**보안 취약점 신속 식별**
새 CVE 발표 시 영향받는
서비스 즉시 파악 가능
*(Log4Shell: SBOM 없었으면 수개월 혼란)*

**라이선스 리스크 관리**
비호환 라이선스 조합 사전 차단
GPL/AGPL 혼입 즉시 감지

</div>
<div>

**소프트웨어 노후화 관리**
EOL(End-of-Life) 컴포넌트 식별
기술 부채 현황 파악

**규제 준수**
미국 EO 14028
EU Cyber Resilience Act
FDA 의료기기 보안 가이드라인

</div>
</div>

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/sbom/what-is-sbom/">sktelecom.github.io/guide/supply-chain/sbom/what-is-sbom</a></div>

<!--
SBOM이 없었다면 Log4Shell 사태 때 각 팀이 모든 서버를 수동으로 전수 조사해야 했을 것입니다.
SBOM이 있으면 취약한 버전의 Log4j가 포함된 서비스 목록을 즉시 뽑아내어 우선순위를 정해 대응할 수 있습니다.
SBOM은 보안뿐만 아니라 라이선스 관리, 기술 부채 파악, 규제 준수 등 다양한 목적으로 활용됩니다.
-->

---


# SBOM 표준 비교 — SPDX vs CycloneDX

| | **SPDX** | **CycloneDX** |
|--|----------|---------------|
| 주관 | Linux Foundation | OWASP |
| 표준 인증 | ISO/IEC 5962 | — |
| 주요 목적 | **라이선스 컴플라이언스** | **보안 취약점 관리** |
| 파일 레벨 추적 | 지원 | 미지원 |
| 취약점 정보 | 별도 설정 필요 | **기본 포함** |
| 구조 복잡도 | 상대적으로 복잡 | 간결 |
| 권장 상황 | 라이선스 감사 목적 | **보안 목적 (일반 권장)** |

> 두 표준 간 **상호 변환 도구** 제공 → 필요 시 변환 가능

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/sbom/standards/">sktelecom.github.io/guide/supply-chain/sbom/standards</a></div>

<!--
두 표준은 상호 변환 도구가 제공되므로 하나를 선택해도 필요 시 다른 형식으로 변환할 수 있습니다.
내부 DevSecOps 파이프라인에는 CycloneDX가 보안 도구와의 통합이 더 용이합니다.
라이선스 감사가 주목적이라면 SPDX가 더 상세한 파일 레벨 정보를 제공합니다.
-->

---


# SBOM 생성 도구

| 도구 | 특징 | 적합 용도 |
|------|------|----------|
| **cdxgen** | 소스코드 분석, 다중 언어 지원 | Java, Python, Node.js, Go, Ruby, PHP, Rust, .NET, C++ |
| **Syft** | 이미지·파일시스템·바이너리 분석 | Docker 이미지, 컨테이너, 바이너리/펌웨어 |
| **Trivy** | 취약점 스캔 + SBOM 생성 | **반드시 버전 고정 사용** |

**핵심 원칙**: **빌드 완료 후** SBOM 생성

```bash
# 올바른 순서
npm install # 먼저 의존성 설치
mvn package # Java: 빌드 완료
pip install -r requirements.txt
→ 그 후 SBOM 생성 도구 실행
```

> ※ **Trivy 경고**: 2025년 공급망 공격 피해 → GitHub Actions에서 `@latest` **절대 금지**

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/for-suppliers/creation-guide/">sktelecom.github.io/guide/supply-chain/for-suppliers/creation-guide</a></div>

<!--
도구마다 전이적 의존성 지원 방식이 다릅니다. Syft로 Docker 이미지를 스캔하면 OS 패키지와 앱 라이브러리를 모두 포함한 가장 완전한 SBOM을 생성할 수 있습니다.
소스코드 분석은 빌드 전 상태에서는 전이적 의존성이 누락되므로 패키지 설치 후 실행해야 합니다.
SKT SBOM Scanner는 Docker 기반으로 별도 언어 설치 없이 사용 가능한 편의 도구입니다.
-->

---

<!-- _class: summary -->

# SBOM 제출 절차 및 검증 체크리스트

**제출 프로세스:**

```
SBOM 생성 → 사전 검증 → 이메일/시스템 제출
→ 형식 검토 (3일) → 취약점 분석 → 승인/보완 요청
```

**제출 전 검증 체크리스트:**

- [ ] JSON/XML 문법 오류 없음 (CycloneDX Validator 활용)
- [ ] **전이적 의존성 포함** (일반 웹 앱 컴포넌트 10개 미만이면 의심)
- [ ] 모든 컴포넌트에 **유효한 PURL** 존재
- [ ] Critical/High CVE **조치 완료** 또는 소명서 준비

> 가장 흔한 반려 사유: **전이적 의존성 누락** + **PURL 미기재**

<div class="url-link"><a href="https://sktelecom.github.io/guide/supply-chain/for-suppliers/submission/">sktelecom.github.io/guide/supply-chain/for-suppliers/submission</a></div>

<!--
가장 흔한 반려 사유는 전이적 의존성 누락과 PURL 미기재입니다.
제출 전 온라인 CycloneDX Validator로 형식 검증을 먼저 수행하면 반려를 방지할 수 있습니다.
처음 제출하는 경우 담당자에게 사전 문의하면 시행착오를 줄일 수 있습니다.
-->

---

<!-- _class: title -->
<!-- _paginate: false -->

# 오픈소스는 의무가 아닌 전략이다

## 올바른 사용 → 기여 → 공개 → 공급망 보안

### 기업과 개발자 모두가 성장하는 오픈소스 생태계

오픈소스 관련 문의: 소속 조직의 법무팀 또는 OSPO

<!--
오픈소스는 현대 소프트웨어 개발의 핵심 인프라입니다. 올바르게 사용하고, 기여하고, 공개하며, 공급망을 안전하게 관리하는 것이 기업과 개발자 모두의 지속가능한 성장을 이끕니다.
모르는 것이 있다면 혼자 판단하지 말고, 항상 법무팀 또는 OSPO에 먼저 문의하는 습관을 갖추세요.
-->

---


# 참고 표준 및 자료

| 자료 | 설명 | 주소 |
|------|------|------|
| **OpenChain** (ISO/IEC 5230) | 오픈소스 컴플라이언스 국제 표준 | openchainproject.org |
| **SPDX Specification** | 라이선스·패키지 정보 교환 표준 | spdx.dev |
| **CycloneDX** | 보안 중심 SBOM 표준 | cyclonedx.org |
| **NTIA SBOM Minimum Elements** | SBOM 최소 요소 정의 (미국 상무부) | ntia.gov |
| **Open Source Guide** | 기여·공개 실무 가이드 | opensource.guide |
| **choosealicense.com** | 라이선스 선택 도움 도구 | choosealicense.com |
| **SPDX License List** | SPDX 라이선스 ID 목록 | spdx.org/licenses |

<div class="url-link"><a href="https://sktelecom.github.io/guide/">sktelecom.github.io/guide</a></div>

<!--
이 자료들은 교육 내용을 심화 학습하거나 실무에서 기준 문서로 활용할 수 있습니다.
OpenChain은 기업 오픈소스 컴플라이언스 체계를 인증받는 국제 표준으로, ISO 인증을 준비하는 기업에게 특히 중요합니다.
-->

---


# 라이선스 분류 요약표

| 분류 | 대표 라이선스 | 주요 의무 | 기업 적용 기준 |
|------|-------------|----------|--------------|
| **Public Domain** | CC0, Unlicense | 없음 | 자유 사용 |
| **Permissive** | MIT, Apache-2.0, BSD-2/3 | 고지문 동봉 | 자유 사용 |
| **Weak Copyleft** | LGPL, MPL-2.0, EPL-2.0 | 수정 모듈 공개 | ※ Dynamic Link 권장 |
| **Copyleft** | GPL-2.0, GPL-3.0 | 전체 소스 공개 | ※ 코드 분리 설계 필수 |
| **Network Copyleft** | AGPL-3.0 | 네트워크 서비스도 공개 | SaaS 사용 금지 |
| **Source Available** | SSPL, BSL, Elastic-2.0 | 인프라 전체 공개 등 | 사전 법적 검토 |
| **비상업·제한** | CC-BY-NC, BSD-4 | 상업적 사용 금지 등 | 기업 사용 불가 |
| **AI 모델** | Llama 2, RAIL, CreativeML | 용도 제한 | 별도 검토 필수 |

<div class="url-link"><a href="https://sktelecom.github.io/guide/use/obligation/">sktelecom.github.io/guide/use/obligation</a></div>

<!--
이 표는 현장에서 빠르게 참조할 수 있는 요약본입니다. 실제 업무에서는 경계가 모호한 사례가 많으므로, 이 표는 최초 판단 기준으로만 활용하고 모호한 경우에는 반드시 전문가에게 문의하세요.
-->

---


# 오픈소스 활동 의사결정 흐름도

**[사용]** 오픈소스를 제품에 사용하고 싶다
→ 라이선스 확인 → 의무사항 검토 → 또는 법무/OSPO 문의

**[기여]** 오픈소스를 수정했고 기여하고 싶다
→ 조직 승인 → OSPO 리뷰 → CLA/DCO 확인 → PR 제출

**[공개]** 사내 소프트웨어를 공개하고 싶다
→ 가치·리소스 확인 → 조직 승인 → OSPO 지원 → 코드 정리 → 공개

**[SBOM]** 소프트웨어를 납품해야 한다
→ 빌드 완료 후 SBOM 생성 → 검증 → 제출 → 취약점 조치

> **공통 원칙**: 모호한 경우 → **법무팀 또는 OSPO에 먼저 문의**

<div class="url-link"><a href="https://sktelecom.github.io/guide/">sktelecom.github.io/guide</a></div>

<!--
세 가지 활동(기여·공개·SBOM)의 핵심 공통점은 '혼자 결정하지 않는다'는 것입니다.
기업의 지식재산과 법적 리스크가 걸린 문제이므로, 내부 승인 체계와 OSPO 지원을 적극 활용하세요.
오픈소스 활동은 올바른 프로세스를 따를 때 기업과 개발자 모두에게 최대의 가치를 만들어냅니다.
-->
