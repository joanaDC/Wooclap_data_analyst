<h1>📊 Wooclap - Data Analyst</h1>

<h2>📌 Description</h2>

This project aims to analyze student responses in Wooclap events and reconstruct session groupings. The dataset lacks explicit session identifiers, so we will infer them based on time and event data.

<h2>🎯 Objectives</h2>

1. Reconstruct sessions from sample.csv based on event logs.

2. Visualize data:
    - Distribution of the number of answers per session.
    - Monthly session participation of the top 10% most active students.
3. Design a data pipeline to automate this analysis for recurring use.

<h2>📁 Repository Structure</h2>

📂 Wooclap_data_analyst/ <br>
│── 📂 input/ #------------- Raw input data files <br>
│   ├── metadata.csv <br>
│   ├── sample.csv  <br>
│── 📂 output/ #------------ Results and visualizations <br>
│   ├── graph_answers_per_session.png <br>
│   ├── graph_sessions_per_student.png <br>
│── 📂 src/ #--------------- Python scripts/Jupyter notebook for data processing <br>
│── 📜 README.md #---------- Project documentation <br>
│── 📜 .gitignore #--------- Exclude unnecessary files <br>
│── 📜 requirements.txt #--- Dependencies <br>

<h2>📄 Content of the input Folder</h2>

The dataset consists of two primary files: metadata.csv and sample.csv.

1. metadata.csv: This file serves as a data dictionary for understanding the structure of sample.csv. It provides detailed descriptions of each column:

    - type: The type of action performed by the Wooclap user, identified by participant_id. For example, "question-answer" indicates a response to a question.

    - event_id: The unique ID of the Wooclap event associated with the question. This helps to group actions under specific events.

    - participant_id: The unique ID of a participant who interacted with the Wooclap event.

    - created_at: A timestamp indicating when the action was performed. The timezone is UTC, and the format includes the year, month, day, hour, minute, and second.

    - object_id: The unique ID of the question, which is only relevant when type = "question-answer". It identifies which question received the answer.

2. sample.csv: This file contains the raw data for each user action during a Wooclap event. Each row corresponds to a specific action performed by a participant:

This file contains the raw data for each user action during a Wooclap event. Each row represents a specific action performed by a participant, and the columns in sample.csv correspond to those described in metadata.csv (e.g., type, event_id, participant_id, created_at, object_id).

These datasets provide a foundation for analyzing user engagement, event participation, and reconstructing sessions based on the recorded actions.

<h2>📄 Content of the src Folder</h2>

............

<h2>📊 Expected Outputs</h2>

graph_answers_per_session.png: Number of answers per session.
graph_sessions_per_student.png: Monthly participation of top 10% active students.

<h2>🔧 Data Pipeline</h2>

A conceptual data pipeline will be designed to efficiently process raw data into meaningful insights using appropriate technologies.

<h2>🚀 Installation & Usage</h2>

pip install -r requirements.txt
python src/main.py  # Runs the session reconstruction & analysis

