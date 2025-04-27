# Project Manager Guide: Fake News Detection with NLP

## 📌 Project Overview
**Goal**: Build an NLP tool to classify news as "real" or "fake" using an LSTM model with Streamlit UI.  
**Key Changes from Original Plan**:
- **UI**: Streamlit replaces Flask for faster deployment in Google Colab.
- **Model**: Prioritize LSTM over BERT for resource efficiency.
- **Deployment**: Use Google Colab + ngrok for demo (no Docker needed).

---

## 👥 Team Roles & Responsibilities (Updated)

| Role                | Key Tasks                                                                 | Tools/Skills               |
|---------------------|--------------------------------------------------------------------------|----------------------------|
| **Data Engineer**   | Clean datasets, handle text preprocessing, manage Google Drive pipelines | Python, Pandas, NLTK       |
| **ML Engineer**     | Train/evaluate LSTM model, optimize thresholds, track metrics            | TensorFlow, Scikit-learn    |
| **Full-Stack Dev**  | Build Streamlit UI, integrate ngrok for Colab deployment                 | Streamlit, ngrok           |
| **Project Manager** | Track deadlines, document progress, resolve blockers                    | Trello, Git, Google Docs   |

---


---

## 🗓️ Phase-Wise Plan (Revised)

### **Phase 1: Setup & Data Prep (Week 1-2)**
| Role                | Tasks                                                                 |
|---------------------|----------------------------------------------------------------------|
| Data Engineer       | - Download datasets from Kaggle <br> - Run `data_cleaning.py`        |
| ML Engineer         | - Set up Colab notebook <br> - Research LSTM hyperparameters         |
| Full-Stack Dev      | - Initialize GitHub repo <br> - Draft Streamlit UI wireframe         |
| Project Manager     | - Create Trello board <br> - Schedule daily standups (15 mins)       |

### **Phase 2: Model Training (Week 3-4)**
| Role                | Tasks                                                                 |
|---------------------|----------------------------------------------------------------------|
| ML Engineer         | - Train LSTM model <br> - Share accuracy/F1 scores                   |
| Data Engineer       | - Generate padded sequences <br> - Handle class imbalance            |
| Full-Stack Dev      | - Build prediction API in Streamlit                                  |
| Project Manager     | - Document metrics in Google Sheets <br> - Resolve GPU access issues |

### **Phase 3: Deployment & Testing (Week 5-6)**
| Role                | Tasks                                                                 |
|---------------------|----------------------------------------------------------------------|
| Full-Stack Dev      | - Deploy UI via ngrok <br> - Add heuristic overrides (e.g., "CERN")  |
| ML Engineer         | - Optimize decision threshold <br> - Create test cases               |
| Project Manager     | - User testing <br> - Finalize documentation                        |

---

## 🔧 Collaboration Tools
- **Code**: [GitHub Repo](https://github.com/) (Branch: `main-dev`)  
- **Tasks**: [Trello Board](https://trello.com/) (Columns: Todo/Doing/Done)  
- **Docs**: [Google Drive Folder](https://drive.google.com/) (Shared with team)  
- **Communication**: Discord (Channels: #general, #bugs, #daily-standup)  

---

## 🚨 Risk Mitigation
| Risk                          | Solution                                  |
|-------------------------------|-------------------------------------------|
| Low LSTM accuracy             | Add data augmentation for "REAL" samples  |
| Colab disconnections          | Save checkpoints hourly to Google Drive   |
| UI latency                    | Cache tokenizer/model in Streamlit       |

---

## ✅ Success Metrics
- **Model**: >90% accuracy on test set  
- **UI**: <3 sec response time for predictions  
- **Team**: 100% tasks logged in Trello  

---

## ▶️ Next Steps
1. Clone repo: `git clone [your-repo-link]`  
2. Data Engineer: Upload datasets to `/data/raw`  
3. ML Engineer: Start `model_training.ipynb` in Colab  
4. Full-Stack Dev: Draft `app.py` with Streamlit  
5. Project Manager: Schedule kickoff meeting (Agenda: [here](https://docs.google.com/))  
