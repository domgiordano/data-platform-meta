# Repository File Structures

## 1. azure-data-platform-infra
```
azure-data-platform-infra/
├── README.md
├── .github/
│   └── CODEOWNERS
├── environments/
│   ├── dev.tfvars
│   ├── stg.tfvars
│   └── prod.tfvars
├── modules/
│   ├── networking/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── storage/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── compute/
│   │   ├── synapse/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   └── data-factory/
│   │       ├── main.tf
│   │       ├── variables.tf
│   │       └── outputs.tf
│   ├── ai-services/
│   │   ├── openai/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   └── search/
│   │       ├── main.tf
│   │       ├── variables.tf
│   │       └── outputs.tf
│   ├── security/
│   │   ├── key-vault/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   └── identity/
│   │       ├── main.tf
│   │       ├── variables.tf
│   │       └── outputs.tf
│   └── monitoring/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
├── main.tf
├── variables.tf
├── outputs.tf
├── versions.tf
└── terraform.tf
```

## 2. azure-data-platform-backend
```
azure-data-platform-backend/
├── README.md
├── .github/
│   ├── workflows/
│   │   ├── deploy.yml
│   │   ├── test.yml
│   │   └── release.yml
│   └── CODEOWNERS
├── notebooks/
│   ├── bronze/
│   │   ├── raw_to_bronze.py
│   │   └── validation.py
│   ├── silver/
│   │   ├── bronze_to_silver.py
│   │   ├── data_quality.py
│   │   └── deduplication.py
│   ├── gold/
│   │   ├── silver_to_gold.py
│   │   └── aggregations.py
│   └── ai/
│       ├── text_extraction.py
│       ├── embedding_generation.py
│       ├── metadata_enrichment.py
│       └── index_management.py
├── pipelines/
│   ├── definitions/
│   │   ├── document_processing.json
│   │   ├── daily_batch.json
│   │   └── streaming_pipeline.json
│   ├── datasets/
│   │   ├── source_datasets.json
│   │   └── sink_datasets.json
│   └── triggers/
│       ├── scheduled_triggers.json
│       └── event_triggers.json
├── functions/
│   ├── document-processor/
│   │   ├── __init__.py
│   │   ├── function.json
│   │   └── handler.py
│   ├── event-handler/
│   │   ├── __init__.py
│   │   ├── function.json
│   │   └── handler.py
│   └── shared/
│       ├── utils.py
│       └── constants.py
├── schemas/
│   ├── bronze/
│   │   └── document.json
│   ├── silver/
│   │   └── enriched_document.json
│   └── gold/
│       └── document_mart.json
├── search/
│   ├── indices/
│   │   ├── regulatory_docs.json
│   │   └── policies.json
│   └── skillsets/
│       └── document_skillset.json
├── scripts/
│   ├── deploy_notebooks.py
│   ├── deploy_pipelines.py
│   ├── deploy_functions.py
│   └── deploy_search.py
├── tests/
│   ├── unit/
│   ├── integration/
│   └── fixtures/
├── requirements.txt
├── requirements-dev.txt
├── pyproject.toml
└── .env.example
```

## 3. azure-data-platform-frontend
```
azure-data-platform-frontend/
├── README.md
├── .github/
│   ├── workflows/
│   │   ├── deploy.yml
│   │   ├── test.yml
│   │   └── build.yml
│   └── CODEOWNERS
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── search/
│   │   │   ├── SearchBar.tsx
│   │   │   ├── SearchResults.tsx
│   │   │   └── Filters.tsx
│   │   ├── documents/
│   │   │   ├── DocumentViewer.tsx
│   │   │   ├── DocumentList.tsx
│   │   │   └── DocumentCard.tsx
│   │   ├── dashboard/
│   │   │   ├── MetricsPanel.tsx
│   │   │   ├── ProcessingStatus.tsx
│   │   │   └── Charts.tsx
│   │   └── common/
│   │       ├── Header.tsx
│   │       ├── Footer.tsx
│   │       └── Layout.tsx
│   ├── lib/
│   │   ├── api/
│   │   │   ├── search.ts
│   │   │   ├── documents.ts
│   │   │   └── metrics.ts
│   │   ├── hooks/
│   │   │   ├── useSearch.ts
│   │   │   └── useDocuments.ts
│   │   └── utils/
│   │       ├── constants.ts
│   │       └── helpers.ts
│   ├── types/
│   │   ├── document.ts
│   │   ├── search.ts
│   │   └── api.ts
│   └── config/
│       └── environment.ts
├── public/
│   ├── favicon.ico
│   └── assets/
├── tests/
│   ├── unit/
│   ├── e2e/
│   └── fixtures/
├── package.json
├── tsconfig.json
├── next.config.js
├── .env.example
├── .eslintrc.json
└── tailwind.config.ts
```
