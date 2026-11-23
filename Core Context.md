---
type: core-context
aliases:
  - User Context
  - 핵심 맥락
description: "Active user context for a robotics graduate student researching optimal control and Whole-Body Control. Guides knowledge collection toward rigorous mathematical formulation, research reuse, and problem-oriented paper analysis."
author:
  - "[[명근]]"
date created: 2026-11-23
date modified: 2026-11-23
tags:
  - system
  - schema
  - core-context
source: []
version: "1.0"
snapshot_date: 2026-11-23
status: active
---

# 🧭 Core Context — 명근의 사용자 맥락

> 이 노트는 LLM 이 ingest / query / lint 전에 반드시 읽는 사용자 맥락 앵커다.

---

## 1. Who — 사용자 정체성

### 기본 정체성

- **이름**: 명근
- **직함 / 역할**: 로보틱스 분야 대학원생
- **전문 분야**: 로보틱스, 최적제어, Whole-Body Control
- **주 활동 영역**: MPC·ROS 기반 제어 연구, 로봇 시스템 구현과 실험, 관련 논문 분석

### 연속성 선언 (Continuity Statement)

> 기계공학을 전공하며 제어에 관심을 갖게 되었고, 모바일 로봇 자율주행을 통해 ROS를 처음 접했다. 그 연장선에서 MPC를 비롯한 제어 기법을 공부한 경험이 대학원 진학과 현재의 최적제어·Whole-Body Control 연구로 이어졌다.

---

## 2. Why — 지식을 수집하는 목적 (재활용 축)

**미래의 나에게 보내는 편지**: "이 소스가 아래 어느 축에 재활용될지" 를 수집 시점에 명시하지 못하면 수집하지 않는다.

1. **대학원 연구·학위논문**: 연구 질문 개발, 이론적 근거 정리, 학위논문 집필
2. **로보틱스 논문 리뷰**: 선행연구의 문제 설정, 방법, 결과, 한계 비교
3. **최적제어·MPC 이론 학습**: 수학적 정의, 최적화 문제, 알고리즘과 가정 정리
4. **Whole-Body Control 연구**: 전신제어 이론, formulation, 구현 방법 축적
5. **ROS·로봇 구현과 실험**: 소프트웨어 구성, 실험 절차, 재현 가능한 구현 지식 보존
6. **세미나·발표 자료**: 연구실 세미나, 학회 발표, 설명 자료로 재구성
7. **개인 지식관리·진로 개발**: 연구 역량의 누적과 장기적인 연구 방향 탐색

---

## 3. What — (옵션) 개인 지식 프레임워크

현재 별도의 개인 지식 프레임워크는 두지 않는다. §2의 재활용 축을 기준으로 자료의 목적과 후속 활용을 추적하며, 연구 과정에서 반복되는 패턴이 확인되면 프레임워크로 승격한다.

---

## 4. How — (옵션) 지식 시스템 철학

- 수식의 formulation과 definition을 명확히 기록한다.
- 각 변수의 의미와 차원을 명시하고, 함수가 scalar-valued인지 vector-valued인지 구분한다.
- 최적화 문제는 결정변수, 목적함수, 제약조건, 가정을 분리하여 표현한다.
- 논문을 정리할 때 결과와 의의를 구분하고, 해당 연구가 어떤 문제를 해결했는지 명시한다.

---

## 5. Operational Directives (LLM 행동 규칙)

### Ingest 시

1. `/ingest` 는 반드시 "왜 수집했는가?" 를 1회 묻는다 (미래의 나에게 보내는 편지, §2 축 참조).
2. Raw Source frontmatter 에 `collectionPurpose`를 기록한다.
3. 수식이 포함된 자료는 §4의 formulation·definition 원칙에 따라 Wiki 페이지에 컴파일한다.

### Query 시

1. 답변이 §2의 7개 재활용 축 중 어느 축에 연결되는지 명시한다.
2. 논문 관련 답변은 해결한 문제, 결과, 의의를 구분한다.

### Lint 시

- Raw Source 에 `collectionPurpose` 없으면 flag.
- Core Context `snapshot_date` 가 30 일 이상 오래되면 `/refresh-context` 추천.

### 이미지 저장

- 모든 이미지·첨부: `80. References/Attachments/` 일원화.

---

## 6. 채우고 나서

- [x] §1 정체성 채움
- [x] §2 재활용 축 7개 정의
- [x] §3 개인 프레임워크 운영 방침 기록
- [x] §4 지식 기록 원칙 정의
- [x] Mode A 단독 운영 설정
- [x] frontmatter `status: active`
- [x] frontmatter `snapshot_date` 갱신

완료 후 첫 `/ingest` 를 실행해보세요. Core Context 가 작동하면 LLM 이 §2 축을 언급하며 목적 질문을 던집니다.

---

## 7. Related

- [[CLAUDE]] — LLM Wiki Schema
- [[index]] — Master Index
- [[log]] — Change Log
- [[LLM-Wiki-Starter-Kit]] — 외부 공유용 간이 킷

---

*템플릿 v1.0 — Karpathy LLM Wiki pattern + 미래의 나에게 보내는 편지 + CMDSPACE harness*
