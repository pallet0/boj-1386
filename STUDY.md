# BOJ 1386 학습 자료

각 Phase별로 **개념 → 구현** 순으로 정리. 한국어 자료는 🇰🇷, 일본어는 🇯🇵, 영상은 🎥, 책/PDF는 📖로 표시.

> **추천 시작 루트:** Phase 1 들어가기 전에 3Blue1Brown 푸리에 영상 한 편 → Reducible FFT 영상 → JusticeHui 한글 글 순서. 이 1시간 반이 이후 모든 Phase의 체감 난이도를 낮춰줌.

---

## Phase 0 — 모듈러 산술 기초체력

**개념**
- [CP-Algorithms — Modular Inverse](https://cp-algorithms.com/algebra/module-inverse.html)
- [CP-Algorithms — Binomial Coefficients](https://cp-algorithms.com/combinatorics/binomial-coefficients.html)
- 📖 [Competitive Programmer's Handbook](https://cses.fi/book/book.pdf) — Ch. 21 "Number theory" (Antti Laaksonen, 무료 PDF)

**한국어**
- 🇰🇷 koosaga 블로그: "페르마 소정리 모듈러 역원" 검색

---

## Phase 1 — FFT 입문

**직관 (먼저 보기)**
- 🎥 [3Blue1Brown — But what is the Fourier Transform?](https://www.youtube.com/watch?v=spUNpyF58BY) · 푸리에 변환의 시각적 직관
- 🎥 [Reducible — The Fast Fourier Transform: Most Ingenious Algorithm Ever?](https://www.youtube.com/watch?v=h7apO7q16V0) · FFT 분할정복 구조 애니메이션

**개념**
- 📖 *CLRS — Introduction to Algorithms* Ch. 30 "Polynomials and the FFT" · 교과서 표준 설명

**구현**
- [CP-Algorithms — Fast Fourier Transform](https://cp-algorithms.com/algebra/fft.html) · 코드 포함, 첫 구현 표준 참고
- 🇰🇷 [JusticeHui — FFT in PS](https://justicehui.github.io/hard-algorithm/2019/09/04/FFT/) · 한국어 PS 관점 정리
- 🇰🇷 namnamseo — "FFT in competitive programming" (검색)

---

## Phase 2 — NTT & 임의 모듈러 NTT

**개념**
- [CP-Algorithms — Number Theoretic Transform](https://cp-algorithms.com/algebra/fft.html#number-theoretic-transform) · FFT 글 후반부
- 🇰🇷 [JusticeHui — 정확도 높은 FFT와 NTT](https://justicehui.github.io/hard-algorithm/2020/05/20/fftntt/) · 998244353, 임의 모듈러 처리까지 한국어로 가장 친절

**임의 모듈러 NTT (1386 핵심)**
- Codeforces 블로그에서 "arbitrary modulus NTT" 검색 — rng_58, Nyaan 등의 표준 글
- **첫 구현은 3-prime CRT 방식 추천** (split-radix보다 디버깅 쉬움)

---

## Phase 3 — 다항식 라이브러리 (역원·log·exp·분할정복)

**개념**
- [CP-Algorithms — Operations on polynomials and series](https://cp-algorithms.com/algebra/polynomial.html) · **이 페이지를 통째로 정독**. Phase 3·4·5가 사실상 한 페이지에 다 있음
- 📖 *Competitive Programming 4* (Halim) Volume 2 — 다항식 챕터
- 🇯🇵 maspy 블로그: [maspypy.com](https://maspypy.com)에서 "形式的冪級数" 검색 · 일본 PS 표준 자료, Google 번역으로도 충분히 읽힘

**한국어**
- 🇰🇷 [hyperbolic — 다항식 나눗셈/역원/log/exp 시리즈](https://hyperbolic.tistory.com/4) · 한국어로 이 깊이까지 다룬 거의 유일한 글
- 🇰🇷 cubelover, ho94949의 [infossm.github.io](https://infossm.github.io) 글들

---

## Phase 4 — 라그랑주 보간 & Faulhaber

**개념**
- [CP-Algorithms — Lagrange Interpolation](https://cp-algorithms.com/numerical_methods/lagrange_interpolation.html)
- 📖 *Concrete Mathematics* (Graham, Knuth, Patashnik) Ch. 6 "Special Numbers" · 베르누이 수와 Faulhaber 공식의 근원. 평생 두고 볼 책

**한국어**
- 🇰🇷 koosaga, jhnah917 블로그에서 "라그랑주 보간" 검색

---

## Phase 5 — 근의 거듭제곱 합 / Multipoint Evaluation

**개념**
- [CP-Algorithms — Multipoint Evaluation](https://cp-algorithms.com/algebra/polynomial.html#multi-point-evaluation)
- 🇰🇷 [ho94949 — Multipoint Evaluation](https://github.com/infossm/infossm.github.io/blob/master/_posts/2019-06-17-Multipoint-evaluation.md) · 분할정복 + 다항식 나눗셈
- [Wikipedia — Newton's identities](https://en.wikipedia.org/wiki/Newton%27s_identities) · 기본 대칭 다항식 ↔ 거듭제곱 합 양방향 공식

> **팁:** Phase 3에서 정독한 cp-algorithms polynomial 페이지를 한 번 더 읽기. 이번엔 multipoint evaluation 부분이 다르게 보임.

---

## Phase 6 — 생성함수 / EGF

**원서 (이 단계는 책이 진짜 도움됨)**
- 📖 [Wilf — *generatingfunctionology* (무료 PDF)](https://www2.math.upenn.edu/~wilf/DownldGF.html) · **1~3장만 읽어도 1386 EGF 사고가 손에 잡힘**. 얇고 무료. 안 읽을 이유 없음
- 📖 *Concrete Mathematics* Ch. 7 "Generating Functions" · Wilf보다 친절하고 길게
- 📖 [Flajolet & Sedgewick — *Analytic Combinatorics* (무료 PDF)](https://algo.inria.fr/flajolet/Publications/book.pdf) · 끝판왕. Part A만 훑어도 충분

**한국어**
- 🇰🇷 [evenharder — Generating Function](https://github.com/infossm/infossm.github.io/blob/master/_posts/2019-10-19-generating-function.md) · PS 관점 압축 정리
- 🇰🇷 yclock의 generating function 시리즈 (infossm)

---

## Phase 7 — 종합 리허설

새 자료보단 **복습**이 효과적. cp-algorithms polynomial 챕터 + yosupo editorial이 핵심.

**라이브러리 비교용**
- 🇯🇵 [Nyaan's Library](https://github.com/NyaanNyaan/library) · 일본 강자의 다항식 라이브러리. 본인 라이브러리 부족한 부분 즉시 발견
- [AtCoder Library (ACL)](https://github.com/atcoder/ac-library) · 공식, 미니멀 비교용

---

## 한 줄 학습 순서

1. 🎥 3Blue1Brown 푸리에 → Reducible FFT (1시간) — **Phase 1 시작 전**
2. 🇰🇷 JusticeHui FFT 글 — Phase 1 구현
3. [cp-algorithms algebra 섹션](https://cp-algorithms.com/) 북마크 — Phase 1~5 내내 곁에 두기
4. 📖 Wilf *generatingfunctionology* 1~3장 — **Phase 4 끝날 무렵** 시작 (이때가 가장 와닿음)
5. 🇰🇷🇯🇵 maspy / hyperbolic / ho94949 블로그 — 막힐 때마다 검색