# Overview

# Table of Contents
1. [What is the Article Pipeline?](#what-is-the-article-pipeline)
2. [The Software Architecture](#architecture)
3. [Terminology](#terminology)


# What is the Article Pipeline?
The Article Pipeline is a data pipeline that can be used to ingest journal articles and their accompanying NMR data into the NP-MRD as soon as the articles are published. 

This pipeline was developed as a way to get large amounts of raw nmr data into the NP-MRD database as well as encourage data deposition by the wider chemistry community.


# The Software Architecture
The Article Pipeline is constructed of many different microservices which work to funnel data on articles from the publishing journal, to entries in the [Article Pipeline Database](#article-pipeline-database). The database is then accessed by the [Frontend Webpage](#frontend-webpage) to send and recieve data (the specifics will be discussed later).

<img src="assets/Article_Pipeline_Architecture.png" alt="drawing" width="800"/>


# Terminology
#### **Article Pipeline Database**: 
This is the holding bay for data that is being sent to NPMRD. It is a PostgreSQL database in the backend of the Article Pipeline. This database holds metadata on every deposition as well as filepaths to the raw data files. 

#### **Frontend Webpage**:
This is the frontend webpage for the Data Deposition Platform. This site is built using the Next.js framework on top of React. It consists of mainly three different pages, the DOI search page, data deposition page, and the data validation page.
