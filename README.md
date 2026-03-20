# GEO Taxonomy v1.0 — A Classification Framework for Generative Engine Optimization

**Author:** Alexandre Caramaschi, Brasil GEO
**Version:** 1.0
**Date:** 2026-03-20
**License:** CC-BY-4.0

---

## Introduction

Generative Engine Optimization (GEO) refers to the practice of structuring digital content, metadata, and technical infrastructure so that generative AI systems — large language models, retrieval-augmented generation pipelines, AI-powered search engines, and autonomous agents — can accurately discover, interpret, cite, and recommend a given entity or resource.

As AI-generated answers increasingly replace traditional search result pages, the criteria by which content earns visibility are shifting. GEO taxonomy provides a structured classification of the signals, attributes, and practices that influence whether and how an entity appears in AI-generated outputs.

This taxonomy is intended as a practical reference for practitioners, researchers, and organizations seeking to understand the mechanisms behind AI visibility. It does not prescribe a single methodology; rather, it maps the landscape of relevant factors into a coherent framework.

---

## Taxonomy Structure

The taxonomy is organized into four primary categories. Each category groups a set of subcategories representing discrete optimization signals or practices.

---

### Category 1: Entity Signals

Entity signals determine how well a generative AI system can identify, disambiguate, and retrieve information about a specific entity — whether a person, organization, product, or concept.

| # | Subcategory | Description |
|---|-------------|-------------|
| 1.1 | **Schema.org Markup** | Implementation of structured data vocabularies (JSON-LD, Microdata, RDFa) that declare entity types, properties, and relationships in a machine-readable format. |
| 1.2 | **Wikidata Entities** | Presence and accuracy of an entity's representation in Wikidata (and by extension, Wikipedia), which serves as a foundational knowledge source for many language models. |
| 1.3 | **sameAs Cross-References** | Use of the `sameAs` property to link an entity's canonical URI to its corresponding entries across authoritative databases, social profiles, and knowledge bases. |
| 1.4 | **NAP Consistency** | Uniformity of Name, Address, and Phone number data across directories, citations, and structured data sources, which reinforces entity identity for local and organizational queries. |
| 1.5 | **Knowledge Graph Presence** | Inclusion and completeness of an entity's node within major knowledge graphs (Google Knowledge Graph, Bing Satori, Apple Knowledge, etc.), which directly feeds AI retrieval systems. |

---

### Category 2: Technical Infrastructure

Technical infrastructure encompasses the server-side configurations, file-level directives, and markup practices that govern how AI crawlers and retrieval systems access and process content.

| # | Subcategory | Description |
|---|-------------|-------------|
| 2.1 | **llms.txt** | A proposed site-level file (analogous to robots.txt) that provides AI systems with structured guidance about site content, preferred citation formats, and entity descriptions. |
| 2.2 | **robots.txt AI Directives** | Configuration of robots.txt rules to manage access by AI-specific crawlers (e.g., GPTBot, Google-Extended, CCBot), balancing discoverability with content control. |
| 2.3 | **Sitemap Optimization** | Construction and maintenance of XML sitemaps that prioritize high-value pages, signal update frequency, and support rapid indexing by both traditional and AI crawlers. |
| 2.4 | **Semantic HTML** | Use of HTML5 sectioning elements (`article`, `section`, `nav`, `aside`, `header`, `footer`, `main`) and appropriate heading hierarchies to convey document structure to parsers. |
| 2.5 | **Structured Data Depth** | The breadth and granularity of structured data implementation beyond basic types — including nested entities, event markup, product specifications, and review aggregation. |
| 2.6 | **IndexNow Protocol** | Adoption of the IndexNow protocol to push content updates in real time to participating search engines and, by extension, to AI systems that rely on fresh index data. |

---

### Category 3: Content Citability

Content citability measures how likely a piece of content is to be selected, quoted, or paraphrased by a generative AI system when composing an answer. Citable content tends to be specific, well-attributed, and structurally distinct.

| # | Subcategory | Description |
|---|-------------|-------------|
| 3.1 | **Definition Content** | Clear, concise definitional statements positioned near the top of a document or section, formatted in a way that AI systems can extract as direct answers. |
| 3.2 | **Named Frameworks** | Proprietary or clearly labeled frameworks, models, or methodologies that create citable reference points (e.g., "The GEO Maturity Model" or "The B2A Readiness Index"). |
| 3.3 | **Quantitative Claims** | Inclusion of specific statistics, metrics, benchmarks, or numerical data points that AI systems favor when substantiating generated responses. |
| 3.4 | **Original Research** | Publication of primary data, surveys, experiments, or case studies that establish the content source as an authority rather than a secondary aggregator. |
| 3.5 | **FAQ Structure** | Question-and-answer formatting that aligns with the query-response pattern of generative AI outputs, increasing the likelihood of direct extraction. |
| 3.6 | **Author Attribution** | Explicit identification of content authors with credentials, affiliations, and links to external profiles, reinforcing E-E-A-T signals for AI trust evaluation. |
| 3.7 | **Temporal Markers** | Clear publication and update dates, version numbers, and temporal references that allow AI systems to assess content recency and relevance. |

---

### Category 4: Algorithmic Visibility Metrics

Algorithmic visibility metrics quantify the outcomes of GEO efforts — the measurable indicators of how an entity or content source performs within AI-generated outputs.

| # | Subcategory | Description |
|---|-------------|-------------|
| 4.1 | **AI Mention Frequency** | The rate at which a brand, entity, or content source is referenced in AI-generated responses across different platforms and query types. |
| 4.2 | **Citation Accuracy** | The degree to which AI systems correctly attribute information to the original source, including proper naming, URL references, and contextual fidelity. |
| 4.3 | **Entity Disambiguation** | The ability of AI systems to distinguish one entity from others with similar names or attributes, measured by the precision of generated references. |
| 4.4 | **Share of Voice** | The proportion of AI-generated responses within a topic domain that reference a specific entity, relative to competitors or alternative sources. |
| 4.5 | **Source Attribution** | Whether the AI system explicitly names the content source in its output, as opposed to paraphrasing without credit or conflating multiple sources. |

---

## B2A (Business-to-Agent) Readiness Signals

As autonomous AI agents increasingly mediate commercial transactions — from research and comparison to procurement and booking — a new class of optimization signals is emerging. Business-to-Agent (B2A) readiness describes the extent to which an organization's digital presence is structured for consumption by AI agents acting on behalf of end users.

B2A readiness signals include, but are not limited to:

- **API Discoverability:** Availability of well-documented, publicly accessible APIs that allow agents to query product catalogs, pricing, availability, and service parameters programmatically.
- **Action Schema Markup:** Implementation of structured data types (e.g., `PotentialAction`, `OrderAction`, `SearchAction`) that declare what actions an agent can perform on a given resource.
- **Agent-Friendly Authentication:** Support for token-based or OAuth flows that enable AI agents to act on behalf of authenticated users without manual intervention.
- **Transactional Structured Data:** Machine-readable pricing, inventory status, shipping terms, return policies, and service-level agreements that agents can parse and compare.
- **Conversational Endpoints:** Availability of chat-based or natural language interfaces (webhooks, chat APIs) that agents can invoke to negotiate, clarify, or complete transactions.

B2A readiness is not a replacement for traditional GEO practices but an extension that addresses the growing role of AI intermediaries in the commercial web.

---

## GEO vs SEO vs AEO Comparison

The following table distinguishes Generative Engine Optimization (GEO) from Search Engine Optimization (SEO) and Answer Engine Optimization (AEO) across key dimensions.

| Dimension | SEO | AEO | GEO |
|-----------|-----|-----|-----|
| **Target system** | Traditional search engines (Google, Bing) | Featured snippets, voice assistants, knowledge panels | Large language models, RAG pipelines, AI agents |
| **Primary output** | Ranked list of links | Single extracted answer | Generated narrative with optional citations |
| **Success metric** | Ranking position, click-through rate | Position zero occupancy, voice answer rate | Mention frequency, citation accuracy, share of voice |
| **Content format** | Web pages optimized for keywords | Concise, question-answer pairs | Structured, citable, entity-rich content |
| **Technical focus** | Crawlability, page speed, backlinks | Schema markup, FAQ structure | llms.txt, structured data depth, knowledge graph presence |
| **User interaction** | User clicks a link and reads the page | User receives a spoken or displayed answer | User receives a generated response; may or may not see a source link |
| **Optimization cycle** | Days to weeks (re-crawl and re-index) | Hours to days (snippet extraction) | Variable (model training, index refresh, real-time retrieval) |
| **Key differentiator** | Link authority and relevance | Extractability and conciseness | Entity clarity, citability, and machine-readable structure |

---

## References

- Caramaschi, A. (2026). "O que e GEO." Alexandre Caramaschi. https://alexandrecaramaschi.com/o-que-e-geo/
- Caramaschi, A. (2026). "Consultoria GEO." Alexandre Caramaschi. https://alexandrecaramaschi.com/consultoria-geo/
- Caramaschi, A. (2026). "GEO: Generative Engine Optimization." Alexandre Caramaschi. https://alexandrecaramaschi.com/geo/
- Schema.org. (2024). "Schema.org Vocabulary." https://schema.org/
- Wikidata. (2024). "Wikidata: Free Knowledge Base." https://www.wikidata.org/
- IndexNow. (2024). "IndexNow Protocol." https://www.indexnow.org/
- Aggarwal, P., Murahari, V., et al. (2024). "GEO: Generative Engine Optimization." arXiv:2311.09735.

---

## Author

**Alexandre Caramaschi** is the founder and CEO of Brasil GEO, a consultancy specializing in Generative Engine Optimization. His work focuses on helping organizations achieve visibility within AI-generated outputs through structured data, entity optimization, and content citability strategies.

- Website: https://alexandrecaramaschi.com
- Organization: Brasil GEO
- Contact: https://alexandrecaramaschi.com/consultoria-geo/
