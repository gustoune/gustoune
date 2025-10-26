
<themed-picture data-catalyst-inline="true" data-catalyst="" style="visibility: visible;">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg">
    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" style="visibility: visible; max-width: 100%;">
  </picture>
</themed-picture>

<h1 align="center">Augustin de Préville</h1>
<p align="center">Engineering · Digital (Brand, Design, Tech, Growth–Thinking) · Data · AI</p>

<p align="center">
  <a href="https://www.linkedin.com/in/augustindepreville/"><img src="https://img.shields.io/badge/LinkedIn-augustindepreville-0A66C2?logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://www.twitter.com/gustoune"><img src="https://img.shields.io/badge/Twitter-@gustoune-111?logo=x&logoColor=white" alt="Twitter"></a>
  <img src="https://komarev.com/ghpvc/?username=gustoune&style=flat&label=Views" alt="Views">
  <img src="https://img.shields.io/badge/Focus-LLM%20Ops%20%7C%20RAG%20%7C%20Search-000" alt="Focus">
</p>

---

## À propos
- Entrepreneur technique, fondateur-dirigeant d’une agence digitale & ESN pendant 19 ans — x (brand, design, tech, growth thinking).
- Croissance soutenue et reconnue : classements fast-growth et tops sectoriels.
- Pilotage produit/ingénierie à l’échelle : plateformes web et APIs, search, data/IA, performance, sécurité, CI/CD.
- Management & structuration : équipes pluridisciplinaires, design ops, offres de conseil, implantation internationale.
- R&D certifiée CIR (10 ans) : IA/ML séquentiel (RNN/LSTM), MLOps (évaluation, dérive, CI/CD).
- Architecture de plateformes web à fort trafic, moteurs de recherche, pipelines temps réel. Priorités : qualité, performance, sécurité, fiabilité, mesure de valeur.

---

## Compétences LLM
- **RAG** : ingestion web → doc-store, normalisation, chunking, recherche hybride (BM25 + embeddings), réécriture de requêtes, citations/grounding.  
- **Agents** : planification/outillage, mémoire, garde-fous, exécution out-of-process (tools, navigateur, code).  
- **Routing** : multi-fournisseurs/modèles, politiques coût/latence/qualité, fallback local.  
- **Observabilité** : traçage des runs/outils, métrologie coûts, benchmarks offline, tests de régression.  
- **MCP** : exposition sécurisée d’outils/données (SQL, identité), auditabilité.  
- **Inférence** : quantisation/1-bit, batching, cache sémantique, maîtrise du cold-start.  
- **ML séquentiel** : RNN/LSTM/GRU pour séries temporelles et détection d’événements.

---

## Stack d’ingénierie
- **Langages** : PHP, JavaScript, Python  
- **Back** : Symfony, Node.js utilitaire, ORM Doctrine  
- **Front** : Angular, React, design systems, accessibilité  
- **CMS/E-commerce** : Drupal, WordPress, Magento, headless CMS  
- **Search** : Elasticsearch, Solr  
- **Data/BI** : Python (pandas, NumPy), Scrapy, Looker Studio, Tableau  
- **Bases** : MySQL, PostgreSQL, Oracle, SQL Server  
- **Perf** : Varnish, profils JS/PHP, budgets de perf  
- **Cloud/DevOps** : Docker, Kubernetes, AWS (ECS, RDS, S3), GitLab CI/CD, Helm  
- **Sécurité/Qualité** : IBM Rational AppScan, Qualys, tests unitaires/fonctionnels, Selenium, JMeter, DST  
- **Méthodos** : Scrum, Lean, Cycle en V

---

## Extraits de code

```ts
// profile.ts — playful CV-as-code 

type Cloud = "aws" | "gcp" | "azure" | "on-prem";
type SearchStack = "elasticsearch" | "solr";
type Db = "mysql" | "postgresql" | "oracle" | "sqlserver";
type Lang = "fr" | "en";

type LatencyBudget = { p50: number; p95: number; p99: number };
type SLO = { availability: string; latency: LatencyBudget; errorRate: string };

type LLMProvider = "openai" | "groq" | "anthropic" | "ollama";
type LLMTask =
  | "chat"
  | "rag"
  | "routing"
  | "tool_use"
  | "voice"
  | "sql_generation";

type Drift = "data" | "concept" | "prompt" | "model";

interface RAGPolicy {
  chunking: "semantic" | "fixed";
  retrieval: "bm25" | "hybrid";
  citeSources: boolean;
  maxTokens: number;
}

interface Budget {
  capUSDPerMonth: number;
  capTokensPerDay: number;
}

interface BenchResult {
  task: LLMTask;
  latencyMs: number;
  quality: number; // 0..100
  costUSD: number;
}

// Nouveauté : Ajout d'un type générique pour les benchmarks, pour plus de flexibilité warrior-style
type BenchResultGeneric<T extends LLMTask> = {
  task: T;
  latencyMs: number;
  quality: number;
  costUSD: number;
  extraMetrics?: Record<string, number>; // Extensible pour d'autres métriques
};

class ChiefDataAIOfficer {
  private years = 19;
  private centersOfExcellence = ["platform", "search", "data", "mlops", "llm"] as const;
  private slo: SLO = {
    availability: "99.9%",
    latency: { p50: 120, p95: 250, p99: 600 },
    errorRate: "<0.5%",
  };

  public readonly name = "Augustin de Préville";
  public readonly role = "Chief Data & AI Officer";
  public readonly location = "Paris, France";
  public readonly languages: Lang[] = ["fr", "en"];

  // Core stacks
  public readonly clouds: Cloud[] = ["aws"];
  public readonly dbs: Db[] = ["mysql", "postgresql", "oracle", "sqlserver"];
  public readonly search: SearchStack[] = ["elasticsearch", "solr"];
  public readonly backends = ["symfony", "nodejs-utility"] as const;
  public readonly frontend = ["angular", "react", "pwa"] as const;
  public readonly devops = ["docker", "kubernetes", "gitlab-ci", "helm", "prometheus", "sentry"] as const;

  // LLM stack
  public readonly providers: LLMProvider[] = ["openai", "groq", "anthropic", "ollama"];
  public readonly ragPolicy: RAGPolicy = {
    chunking: "semantic",
    retrieval: "hybrid",
    citeSources: true,
    maxTokens: 2048,
  };

  // Governance
  private budget: Budget = { capUSDPerMonth: 3000, capTokensPerDay: 5_000_000 };
  private cirCertifiedYears = 10; // R&D program leadership

  getSnapshot() {
    return {
      role: this.role,
      years: this.years,
      centers: [...this.centersOfExcellence],
      slo: this.slo,
      stacks: {
        clouds: this.clouds,
        dbs: this.dbs,
        search: this.search,
        backends: this.backends,
        frontend: this.frontend,
        devops: this.devops,
      },
      llm: { providers: this.providers, ragPolicy: this.ragPolicy },
      governance: { budget: this.budget, cirCertifiedYears: this.cirCertifiedYears },
    };
  }

  // Routing policy: pick the right model/provider based on task + constraints
  routePrompt(task: LLMTask, tokens: number, needDeterminism = false): { provider: LLMProvider; model: string } {
    // toy policy for demo
    if (task === "rag") return { provider: "openai", model: "gpt-4o-mini" };
    if (task === "voice") return { provider: "openai", model: "gpt-4o-realtime" };
    if (task === "sql_generation") return { provider: "anthropic", model: "claude-3.5-sonnet" };
    if (needDeterminism || tokens > 200_000) return { provider: "ollama", model: "llama3.1:70b-instruct-q5" };
    return { provider: "groq", model: "llama3.1-70b" };
  }

  // Bench a provider/model pair (toy deterministic function)
  bench<T extends LLMTask>(task: T): BenchResultGeneric<T> {
    const baseLatency = { chat: 160, rag: 190, routing: 80, tool_use: 220, voice: 140, sql_generation: 260 }[task];
    const quality = { chat: 92, rag: 90, routing: 85, tool_use: 88, voice: 91, sql_generation: 89 }[task];
    const cost = { chat: 0.003, rag: 0.005, routing: 0.001, tool_use: 0.004, voice: 0.006, sql_generation: 0.004 }[task];
    return { task, latencyMs: baseLatency, quality, costUSD: cost };
  }

  // MLOps lifecycle — simplified orchestra
  async deployModel(name: string, sha: string) {
    const checks = ["unit", "integration", "bias", "security"] as const;
    const passed = checks.every(() => true);
    if (!passed) throw new Error("quality gates failed");
    await new Promise((r) => setTimeout(r, 42));
    return { name, sha, strategy: "canary", traffic: "10% → 50% → 100%", rollback: "auto on regression" };
  }

  // Drift detection (toy)
  detectDrift(kind: Drift, metric: number) {
    const threshold = { data: 0.15, concept: 0.1, prompt: 0.2, model: 0.08 }[kind];
    return { kind, metric, threshold, drift: metric > threshold };
  }

  // RAG configuration check
  checkRAG(policy: Partial<RAGPolicy> = {}) {
    const cfg = { ...this.ragPolicy, ...policy };
    const ok = cfg.retrieval === "hybrid" && cfg.citeSources;
    return { cfg, status: ok ? "ready" : "needs_review" };
  }

  // Executive summary (because boards love bullets)
  boardSlide() {
    return [
      `AI/LLM: routing multi-fournisseurs, RAG avec citations, agents out-of-process`,
      `MLOps: évaluation, dérive, CI/CD modèles & prompts, canary/rollback`,
      `Plateformes: APIs first, recherche, perf & SLOs, sécurité by design`,
      `R&D: ${this.cirCertifiedYears} ans de centre certifié CIR (industrialisation IA)`,
    ];
  }

  // Easter egg: generator that streams “value creation” like log lines
  *valueStream() {
    yield "[ok] data contracts enforced";
    yield "[ok] search relevance +27% after synonym tuning";
    yield "[ok] latency p95 down to 230ms (budget 250ms)";
    yield "[ok] hallucination rate -8% with grounding+reranking";
    yield "[ok] cost per answer -32% via routing & caching";
  }

  // Nouveauté : Méthode pour comparer deux benchmarks, avec typing strict
  compareBenches<T extends LLMTask>(bench1: BenchResultGeneric<T>, bench2: BenchResultGeneric<T>): { deltaLatency: number; deltaQuality: number; deltaCost: number } {
    return {
      deltaLatency: bench1.latencyMs - bench2.latencyMs,
      deltaQuality: bench1.quality - bench2.quality,
      deltaCost: bench1.costUSD - bench2.costUSD,
    };
  }
}

// --- demo usage ---
const cdao = new ChiefDataAIOfficer();

console.log("== SNAPSHOT ==");
console.log(cdao.getSnapshot());

console.log("\n== ROUTING SAMPLE ==");
console.log("rag →", cdao.routePrompt("rag", 800));
console.log("sql_generation →", cdao.routePrompt("sql_generation", 1200, true));

console.log("\n== BENCHES ==");
(["rag", "chat", "tool_use"] as LLMTask[]).forEach(t => console.log(t, cdao.bench(t)));

// Nouveauté dans demo : Comparaison de benches
const benchRag = cdao.bench("rag");
const benchChat = cdao.bench("chat");
console.log("\n== COMPARE BENCHES ==");
console.log("rag vs chat →", cdao.compareBenches(benchRag, benchChat));

console.log("\n== DEPLOY ==");
cdao.deployModel("search-relevancy-rlhf", "a1b2c3d").then(r => console.log(r));

console.log("\n== DRIFT ==");
console.log(cdao.detectDrift("data", 0.11));
console.log(cdao.detectDrift("concept", 0.12));

console.log("\n== RAG CHECK ==");
console.log(cdao.checkRAG({ retrieval: "hybrid", citeSources: true }));

console.log("\n== BOARD SLIDE ==");
console.log(cdao.boardSlide().map(b => "• " + b).join("\n"));

console.log("\n== VALUE STREAM ==");
for (const line of cdao.valueStream()) console.log(line);

```

## Réalisations techniques (exemple)

* **Comparateur dynamique** : pipelines Python, index Elasticsearch, tableaux de bord temps réel. Rôle : architecture, pertinence, gouvernance données.
* **Moteur de recherche vertical** : Symfony + Elasticsearch, facettes, synonymes, re-ranking, SLA < 200 ms.
* **Application web transactionnelle** : architecture API-first, CI/CD GitLab, déploiements canary, observabilité instrumentée (Sentry, Prometheus).
* **Génération d’IHM/API depuis schémas relationnels** : ORM/logique relationnelle, CRUD + API JSON/REST.
* **Prédiction opérationnelle** : jobs ML planifiés, features saisonnières, explications locales, alerting.

---

## Toolbox rapide

<p>
  <img src="https://img.shields.io/badge/PHP-777?logo=php&logoColor=fff" alt="PHP">
  <img src="https://img.shields.io/badge/JavaScript-777?logo=javascript&logoColor=fff" alt="JavaScript">
  <img src="https://img.shields.io/badge/Python-777?logo=python&logoColor=fff" alt="Python">
  <img src="https://img.shields.io/badge/Symfony-777?logo=symfony&logoColor=fff" alt="Symfony">
  <img src="https://img.shields.io/badge/Node.js-777?logo=node.js&logoColor=fff" alt="Node.js">
  <img src="https://img.shields.io/badge/Angular-777?logo=angular&logoColor=fff" alt="Angular">
  <img src="https://img.shields.io/badge/React-777?logo=react&logoColor=fff" alt="React">

  <img src="https://img.shields.io/badge/Drupal-777?logo=drupal&logoColor=fff" alt="Drupal">
  <img src="https://img.shields.io/badge/WordPress-777?logo=wordpress&logoColor=fff" alt="WordPress">
  <img src="https://img.shields.io/badge/Magento-777?logo=magento&logoColor=fff" alt="Magento">
  <img src="https://img.shields.io/badge/Headless_CMS-777" alt="Headless CMS">

  <img src="https://img.shields.io/badge/Elasticsearch-777?logo=elasticsearch&logoColor=fff" alt="Elasticsearch">
  <img src="https://img.shields.io/badge/Apache_Solr-777?logo=apachesolr&logoColor=fff" alt="Solr">

  <img src="https://img.shields.io/badge/MySQL-777?logo=mysql&logoColor=fff" alt="MySQL">
  <img src="https://img.shields.io/badge/PostgreSQL-777?logo=postgresql&logoColor=fff" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Oracle_DB-777?logo=oracle&logoColor=fff" alt="Oracle">
  <img src="https://img.shields.io/badge/SQL_Server-777?logo=microsoft%20sql%20server&logoColor=fff" alt="SQL Server">

  <img src="https://img.shields.io/badge/Varnish-777" alt="Varnish">
  <img src="https://img.shields.io/badge/Profiling_JS%2FPHP-777" alt="Profiling">
  <img src="https://img.shields.io/badge/Budgets_de_perf-777" alt="Performance Budgets">

  <img src="https://img.shields.io/badge/Docker-777?logo=docker&logoColor=fff" alt="Docker">
  <img src="https://img.shields.io/badge/Kubernetes-777?logo=kubernetes&logoColor=fff" alt="Kubernetes">
  <img src="https://img.shields.io/badge/AWS-777?logo=amazon-aws&logoColor=fff" alt="AWS">
  <img src="https://img.shields.io/badge/GitLab_CI-777?logo=gitlab&logoColor=fff" alt="GitLab CI">
  <img src="https://img.shields.io/badge/Helm-777?logo=helm&logoColor=fff" alt="Helm">

  <img src="https://img.shields.io/badge/Selenium-777?logo=selenium&logoColor=fff" alt="Selenium">
  <img src="https://img.shields.io/badge/JMeter-777" alt="JMeter">
  <img src="https://img.shields.io/badge/Tests_unitaires%2Ffonctionnels-777" alt="Tests">

  <img src="https://img.shields.io/badge/Scrapy-777" alt="Scrapy">
  <img src="https://img.shields.io/badge/pandas-777?logo=pandas&logoColor=fff" alt="pandas">
  <img src="https://img.shields.io/badge/NumPy-777?logo=numpy&logoColor=fff" alt="NumPy">
  <img src="https://img.shields.io/badge/Looker_Studio-777?logo=google&logoColor=fff" alt="Looker Studio">
  <img src="https://img.shields.io/badge/Tableau-777?logo=tableau&logoColor=fff" alt="Tableau">

  <img src="https://img.shields.io/badge/Sentry-777?logo=sentry&logoColor=fff" alt="Sentry">
  <img src="https://img.shields.io/badge/Prometheus-777?logo=prometheus&logoColor=fff" alt="Prometheus">

  <img src="https://img.shields.io/badge/IA%2FLLM-777" alt="IA/LLM">
  <img src="https://img.shields.io/badge/RNN%2FLSTM%2FGRU-777" alt="RNN/LSTM/GRU">
  <img src="https://img.shields.io/badge/RAG-777" alt="RAG">
  <img src="https://img.shields.io/badge/Agents-777" alt="Agents">
  <img src="https://img.shields.io/badge/MCP-777" alt="MCP">
  <img src="https://img.shields.io/badge/Observabilit%C3%A9-777" alt="Observabilité">
  <img src="https://img.shields.io/badge/CI%2FCD-777" alt="CI/CD">
</p>

---

## Langues

Français (natif) · Anglais (professionnel) · Espagnol (notions)

## Formation

Diplôme d’ingénieur — Arts et Métiers ParisTech
Math Sup/Spé — CPGE

## Connection

* LinkedIn : [https://www.linkedin.com/in/augustindepreville/](https://www.linkedin.com/in/augustindepreville/)
* Twitter : [https://www.twitter.com/gustoune](https://www.twitter.com/gustoune)

```
::contentReference[oaicite:0]{index=0}
```
