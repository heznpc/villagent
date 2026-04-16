# villagent — Review (2026-04-11)

## 1. 커밋 톤이 주장을 일관되게 지지하는가?

**판정: 평가 불가 (commit 1개) — 가장 *초기 단계 단일 import*.**

```
b563bc8 init: villagent 연구 방향 수립 — 에이전트 수명주기 시뮬레이터  (~2026-03-31)
```

진화 패턴:
- **t=0 (3/31)**: docs/research-direction.md (422줄, 한국어) + TODO.md (51줄, 한국어). **본 survey 21개 paper 중 paper draft / outline / LaTeX이 *없는* 거의 유일한 케이스**. 순수 *research direction* 단계.
- 0 commits 후 4월 11일까지 11일 간 진행 정체.

톤 일관성:
- 핵심 주장(에이전트 죽음 = configuration의 비가역적 소실 / Ploidy = session reset / Villagent = entity replacement / 5 mechanisms 분리: reset/compression/death/cross-species/era-transplant / 6 RQ)이 research-direction.md 단일 문서에서 일관.
- *Ploidy 후속 연구*로 명시. cross-repo dependency 강함.
- *5-mechanism table* (Reset / Compression / Death / Cross-species / Era-transplant)이 paper의 핵심 framework.
- *Death after-transmission spectrum*: 묘비(최소) → 에피타프 → 구전/신화 → 유산 → 제사 → 역사서(최대)의 6 layer. 각 layer가 *fidelity*와 *mutation* 두 변수로 매핑.
- *Multi-species ecosystem* 비유: Claude / GPT / Gemini / Llama = 다른 종, 호미닌 진화와 평행.
- 단점: paper draft 없음. outline.md도 없음. **본 survey 21개 paper 중 *학술 산출물 단계가 가장 이름*.**

## 2. 부가 서비스 품질

**판정: 부가 서비스 0개. paper도 없음. *research direction document 1개*만.**

레포 구성:
- `docs/research-direction.md` (422줄, 한국어) — 유일한 학술 자산
- `TODO.md` (51줄, 한국어)
- `.gitignore`, `.idea/`, `.claude/`

코드, 데이터, instrument, 노트북, 데모, 서비스, paper, outline — *전무*. 본 survey 21개 paper 중 *가장 미숙한 단계*.

특이점:
- research-direction.md 422줄이 *깊은 사고가 담긴* document. 단순 stub이 아님.
- 한국어로만 작성. 글로벌 publication을 위해선 영문 변환 필요.
- **본 survey 21개 paper 중 *Korean-only* document가 paper repo에 있는 유일한 케이스**.
- 5-mechanism + 6-layer transmission spectrum + 6 RQ + multi-species ecosystem 비유 — *theoretical depth는 높음*. 그러나 *작품의 형태로 정착된 것은 없음*.

## 3. 고도화 가능 파트

높은 우선순위 (paper 형태로 진입 필요):
1. **research-direction.md → outline.md 영문 변환** — TODO #6에 명시. 이게 가장 시급. 한국어 422줄을 영문 outline 4-5쪽으로 변환. *학술 paper로 들어가는 게이트*.
2. **paper main.tex 초안 작성** — outline 후. 본 survey 다른 paper들이 모두 갖춘 형태. 8-10쪽 4-week task.
3. **MVP 집단 실험 (TODO #1)** — 3-4 세대 에이전트 순차 교체 관찰. 같은 모델, 고정 주제, 사전 정의 편향. 측정: 신뢰도 변화, 새 질문 발생, 답변 다양성. **paper의 가장 큰 약점(empirical 0)을 해결**. ploidy infrastructure(MCP server)를 reuse 가능.
4. **Ploidy와의 *명확한 differentiation* paper 본문에 형식화** — 현재 research-direction에 *철학적 비유*만 있음. session reset(Ploidy) ↔ entity replacement(Villagent)의 *operational 차이*를 1쪽 표로.
5. **5 mechanisms (reset/compression/death/cross-species/era-transplant)의 *operational definition*** — 각각이 *어떻게* 측정 가능한지. *모델 가중치 교체*인지, *프롬프트만 교체*인지, *도구 세트만 교체*인지 명확화.

중간 우선순위:
6. **6-layer transmission spectrum 실험 (TODO #2)** — 4 conditions (묘비/에피타프/유산/전체 로그) × N agents. 후속 에이전트 성능 + 편향 독립성 측정.
7. **Cross-species ecosystem 실험 (TODO #3)** — Claude × GPT × Gemini 3-3-3 mixed agents. 종 내 vs 종 간 성능 차이.
8. **Era transplant 실험 (TODO #4)** — 동일 구성 × 단순 도구 vs MCP 도구. 환경 의존성 정량화.
9. **Qualitative case study (TODO #5)** — n=10 agent society 3-4개월 관찰.
10. **Ploidy infrastructure reuse**: ploidy의 MCP server를 *agent lifecycle simulator*로 확장 가능. cross-repo 강한 dependency.

낮은 우선순위:
11. References.bib 작성.
12. CHI/CSCW/FAccT venue 결정.
13. 한국어 → 영문 abstract 작성.

## 4. 학술적 / 시장 가치 (글로벌, 2026-04-11 기준)

### 학술적 가치: **중 (working paper 기준 top ~30%, *현재 단계는 상당히 미숙*)**

차별점 (잠재력):
- **Death as configuration loss**: 인용 가능한 *조작적 정의*. 단순 비유가 아닌 *operationalizable*. configuration = prompt + memory + tool set이 *비가역적으로 소실*되는 것.
- **5-mechanism taxonomy** (reset/compression/death/cross-species/era-transplant): paper의 *unique framework*. ploidy의 reset과 명확히 differentiate.
- **6-layer transmission spectrum (묘비 → 역사서)**: 인간 사회의 지식 전달을 agent design space에 매핑한 *creative analogy*. fidelity + mutation 두 변수로 형식화.
- **Multi-species ecosystem (호미닌 진화 비유)**: Claude/GPT/Gemini를 *서로 다른 종*으로 보는 framing. cross-species competition + intra-species death의 *교호작용*.
- **Era transplant**: 동일 configuration이 *다른 environment*에서 다르게 행동한다는 명제. 환경 의존성 측정.
- **Ploidy의 *직접 후속 연구***: cross-repo dependency가 강함. *3-paper trilogy* (narcissus = bias evidence / ploidy = session-level intervention / villagent = entity-level intervention).

위험 (현재 단계):
- **paper 자체가 없음** — outline도 없음. 본 survey 21개 paper 중 *학술 산출물 단계가 가장 이름*. 4월 11일까지 *paper draft 0줄*.
- **모든 documentation이 한국어** — 글로벌 학술 venue에 진출 불가. 영문 변환 게이트.
- **6 experiments 모두 *제안*** — 0 implementation. ploidy infrastructure reuse 가능하지만 미작업.
- **Independent researcher 단독 저자** — multi-agent / agent society 영역.
- **죽음 비유의 *학술적 정당성***: 일부 reviewer는 *anthropomorphism* 비판 가능. *configuration loss*라는 operational 정의로 일부 흡수하지만 강한 reviewer는 짚을 가능성.
- **Paper format 부재**: research-direction.md 422줄이 *학술 paper format*이 아닌 *philosophical essay*에 가까움. 변환 작업 무거움.

게재 전망 (현재 단계 → 6개월 후):
- *FAccT 2027 / CHI 2027 / CSCW 2027*: paper draft 미존재. *현재 단계로는 모든 venue에 0% submission readiness*.
- 6개월 후 (paper draft + MVP experiment 가정): *FAccT 2027*: 35-45%. *CSCW 2027*: 35-45%. *CHI 2027*: 30-40%.
- ploidy + narcissus + meta + villagent의 4-paper cluster로 함께 제출하면 *trilogy* citation surface area 강력.

### 시장 가치: **중 (잠재력은 강하지만 현재 단계로는 0)**

- **Multi-agent system 회사**: CrewAI, AutoGen, MetaGPT, LangGraph, Mastra, Inngest 같은 multi-agent framework가 *agent lifecycle* feature를 추가할 정당화 가능. 5-mechanism taxonomy를 product feature로 매핑.
- **AI agent platform**: Anthropic, OpenAI, Cursor, Lovable 같은 회사가 *long-running agent 운영*에 직면. *agent drift* 문제(Gu et al. 2026 인용)에 대한 framework 제공.
- **언론**: NYT/Atlantic/Wired가 좋아할 톤. "AI agent에게 죽음을 부여하면 더 똑똑해지는가" 헤드라인. viral potential 잠재.
- **AGI safety 영역**: agent population dynamics 연구의 *학술적 vocabulary*. AI Safety community(MIRI, Anthropic, AI Safety Institute)에 인용 가능.
- 한계: tool/SaaS 직접 product 경로 *현재* 부재. paper도 없는 상태에서 시장 가치는 *0*.

### 종합 평점 (2026-04-11)

| 축 | 점수 | 코멘트 |
|---|---|---|
| Originality of framing | 8/10 | death = config loss + 5 mechanisms + 6 layers |
| Theoretical depth | 8/10 | 422줄 research-direction은 깊음 |
| Empirical contribution | 1/10 | 0개. 6 experiments proposed only |
| Repo health | 2/10 | 1 commit, no paper, no outline, no code |
| Submission readiness | 1/10 | paper 없음 |
| Cross-repo synergy | 9/10 | ploidy 후속, narcissus/meta/ploidy trilogy |
| Korean-only documentation | 3/10 | 글로벌 publication 불가 |
| Self-criticism | 5/10 | 일부 안전장치 (operational definition) |
| Practical applicability | 5/10 | multi-agent framework 영역 잠재 |
| Timing | 8/10 | multi-agent ecosystem 정점 |
| **Overall (early-stage research)** | **5.0/10** | "Paper draft + MVP experiment + 영문 변환 셋 모두 필요" |

핵심 격언: **"본 survey 21개 paper 중 *학술 산출물 단계가 가장 이른* 케이스. 영문 outline + paper draft + MVP experiment 셋이 *모두 필요*."** research-direction.md 자체는 깊은 사고가 담겨 있지만 *학술 paper로 진입한 것이 없음*. 6개월 안에 영문 paper draft + 1개 empirical study를 만들지 못하면 ploidy/narcissus/meta trilogy에서 *떨어지는* 위험. *잠재력은 강하지만 현재는 가장 미숙한 paper*.
