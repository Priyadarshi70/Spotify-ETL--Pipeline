# Spotify ETL Pipeline 🎧

This project is a complete ETL (Extract, Transform, Load) pipeline that extracts data from the Spotify API, performs data cleaning and transformation in a Jupyter Notebook, and then loads the processed data into AWS for storage and analysis. The pipeline is deployed using AWS Lambda, stores data in S3, and uses Athena for querying — all automated using trigger functions.

---

## 📌 Project Overview

- Extracts song, album, and artist data from public Spotify playlists using the Spotify Web API.
- Cleans and transforms the raw JSON data into structured format (using Pandas).
- Saves cleaned data locally during development and then pushes to AWS S3 in production.
- Automates data pipeline using AWS Lambda functions and Athena query triggers.

---

## 🧰 Technologies Used

- **Python** (Jupyter Notebook)
- **Spotipy** – Spotify Web API wrapper
- **Pandas** – for data cleaning
- **AWS S3** – for cloud data storage
- **AWS Lambda** – for running ETL in the cloud
- **AWS Athena** – for querying S3 data
- **AWS CloudWatch / Triggers** – for automation

---




---

## ⚙️ How It Works

1. **Extraction**: 
   - Uses Spotipy to fetch track data from a Spotify playlist.
2. **Transformation**:
   - Extracts relevant fields (song name, artist, album, duration, release date, etc.).
   - Cleans data (removes duplicates, formats durations, handles nulls).
3. **Loading**:
   - Saves cleaned data to AWS S3 in CSV/Parquet format.
4. **Automation**:
   - AWS Lambda is triggered periodically or on event.
   - AWS Athena runs SQL queries on S3 data and can be chained to other workflows.

---

## 📊 Sample Output

The pipeline collects data like:

| Song Name       | Artist        | Album           | Duration | Release Date |
|----------------|---------------|------------------|----------|---------------|
| Blinding Lights | The Weeknd     | After Hours      | 200040   | 2020-03-20     |

---

## 🚀 Future Improvements

- Add real-time streaming support with AWS Kinesis or Kafka.
- Deploy dashboard for visual analytics using AWS QuickSight or Streamlit.
- Parameterize pipeline for different playlists or genres.

---

## 👤 Author

**Priyadarshi Gupta**  
Data Engineering Enthusiast | AWS & Python Developer

---

## 📄 License

This project is for educational and demo purposes only.


## 🗂️ Project Structure

