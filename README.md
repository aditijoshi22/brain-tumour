# Explainable AI-Based Brain Tumor Detection

This is a complete end-to-end full-stack project for Brain Tumor Detection, Segmentation, and Risk Assessment using Deep Learning and Explainable AI.

## Project Structure
- `ai-model/`: Python ML scripts, Flask API, and the training pipeline.
- `backend/`: Node.js Express server to handle uploads.
- `frontend/`: React Vite application with Tailwind CSS.
- `outputs/`: Generated masks, heatmaps, and reports.

## Setup Instructions

### 1. AI Model & Flask API
1. Open a terminal and navigate to the project root `brain-tumor-ai/`.
2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   - Windows: `venv\Scripts\activate`
   - Mac/Linux: `source venv/bin/activate`
4. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
5. **(Optional) Train the Model:** 
   Place tumor images in `ai-model/dataset/yes/` and non-tumor images in `ai-model/dataset/no/`. Then run:
   ```bash
   python ai-model/train_model.py
   ```
6. Start the Flask API:
   ```bash
   python ai-model/app.py
   ```
   *(Runs on port 5000)*

### 2. Node.js Backend
1. Open a new terminal and navigate to `brain-tumor-ai/backend/`.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the server:
   ```bash
   npm start
   ```
   *(Runs on port 4000)*

### 3. React Frontend
1. Open a new terminal and navigate to `brain-tumor-ai/frontend/`.
2. Start the dev server:
   ```bash
   npm run dev
   ```
   *(Usually runs on port 5173)*

## How to use
Once all three servers are running:
1. Open your browser to the React frontend URL (e.g., http://localhost:5173).
2. Click "Go to Dashboard" or "Upload MRI".
3. Upload an MRI image (JPG or PNG).
4. View the AI prediction, confidence score, risk assessment, segmentation mask, and Grad-CAM heatmap!
5. Click "Download Report" to get a JSON summary.
