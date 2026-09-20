# music-analysis-etl

This ETL will create a comprehensive music analytics database that can analyze relationships between top chart success and critical acclaim in the music industry from the past decade (2015-2025). The ETL integrates datasets from Billboard Hot 100, Spotify Audio Features, and Grammy Awards.

The ETL extracts approximately 350,000 Billboard chart entries, 4,800 Grammy nominations, and 28,680 Spotify artist profiles. The ETL transforms this data by standardizing artist names across sources, generating unique artist IDs, and aggregating records into artist-level metrics.

The data is loaded into an AWS PostgreSQL database with three tables, which are artist_master (table with aggregated metrics), chart_performance (table with weekly chart detail), and grammy_nominations (table with individual nomination records).

This ETL can answer queries such as:

    Do Grammy winners have better chart performance?
    What audio features correlate with commercial success?
    Do more energetic songs correlate with better peak positions?
