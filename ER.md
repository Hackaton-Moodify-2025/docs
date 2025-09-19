# Ingest Service (парсер) загружает в reviews
# ML Service (обучение) на reviews

## Парсер - БД - ML (train)

## ML (inference) - Backend - Фронт

reviews 
- id (serial)
- source (varchar)
- url (varchar)
- text (text)
- published_at (timestamp)
- scraped_at (timestamp)

predictions
- id (serial)
- review_id (fk - reviews.id)
- topic (varchar)
- sentiment (varchar)   -- positive/neutral/negative
- predicted_at (timestamp)

topics
- id (varchar)          -- "credit_cards"
- name (varchar)        -- "Кредитные карты"

aggregates
- id (serial)
- topic_id (fk - topics.id)
- month (date)          -- YYYY-MM-DD
- positive_count (int)
- neutral_count (int)
- negative_count (int)
