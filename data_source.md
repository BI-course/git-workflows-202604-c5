
---

## ETL Tool Recommendations by Source Type

| Source Type | Recommended Tools |
|-------------|--------------------|
| Transactional DB | Debezium + Kafka, AWS DMS, Fivetran, Airbyte |
| Flat Files | dbt-external-tables, Airflow, AWS Glue, Python (Pandas) |
| API | Airbyte, Fivetran, Singer taps, Custom Python (requests + tenacity) |
| Streaming | Apache Flink, Kafka Streams, Spark Structured Streaming, ksqlDB |

---

## Data Quality Expectations by Source

| Source Type | Expected Quality | Common Issues |
|-------------|------------------|---------------|
| Transactional DB | High (system-enforced) | Schema changes, NULL foreign keys |
| Flat Files | Medium (manual) | Format drift, missing values, duplicates |
| API | Medium (vendor-dependent) | Rate limiting, pagination bugs, field deprecation |
| Streaming | Medium (eventual consistency) | Late arrivals, duplicate events, out-of-order data |

---

## Related Documents

- `warehouse_schema.md` – Target schema for all ingested data (Issue #3)
- `etl_pipeline.md` – Detailed transformation logic per source
- `data_quality_rules.md` – Validation rules and error handling

---

