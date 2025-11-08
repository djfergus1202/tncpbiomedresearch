# 🚀 Quick Start Guide - BioMed Research Suite v4.0

## Immediate Deployment (3 Steps)

### Step 1: Push to GitHub
```bash
git init
git add .
git commit -m "Deploy Comprehensive BioMed Suite v4.0"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/biomed-suite.git
git push -u origin main
```

### Step 2: Deploy on Render
1. Go to [dashboard.render.com](https://dashboard.render.com)
2. Click **"New +"** → **"Web Service"**
3. Connect your GitHub repository
4. Render auto-detects everything from `render.yaml`
5. Click **"Create Web Service"**

### Step 3: Test Your API
```bash
# Wait 2-3 minutes for deployment, then test:
curl https://your-app.onrender.com/api/health

# Expected response:
{
  "status": "healthy",
  "version": "4.0.0",
  "platform": "Node.js",
  "deployment": "Render",
  "modules": [
    "molecular_docking",
    "cell_dynamics",
    "retrosynthesis",
    "structure_prediction",
    "antibody_engineering",
    "quantum_chemistry",
    "cdr_generation"
  ]
}
```

---

## Test All Features

### 1. Molecular Docking
```bash
curl -X POST https://your-app.onrender.com/api/docking/run \
  -H "Content-Type: application/json" \
  -d '{
    "proteinId": "6LU7",
    "ligandId": "remdesivir",
    "numModes": 5,
    "algorithm": "vina"
  }'
```

### 2. Retrosynthesis
```bash
curl -X POST https://your-app.onrender.com/api/retrosynthesis/generate \
  -H "Content-Type: application/json" \
  -d '{
    "smiles": "CC(=O)Oc1ccccc1C(=O)O",
    "numPathways": 10,
    "maxSteps": 5
  }'
```

### 3. Antibody CDR Generation
```bash
curl -X POST https://your-app.onrender.com/api/antibody/generate-cdrs \
  -H "Content-Type: application/json" \
  -d '{
    "target_cdr": "H3",
    "num_designs": 100,
    "diversity": "high"
  }'
```

### 4. Cell Simulation
```bash
curl -X POST https://your-app.onrender.com/api/cells/simulate \
  -H "Content-Type: application/json" \
  -d '{
    "cellLineName": "HeLa",
    "experimentParams": {
      "initialCells": 50,
      "duration": 48,
      "timeInterval": 2
    }
  }'
```

---

## What's Included

✅ **13 Computational Toolkits**
- Molecular Docking
- Cell Simulation
- Retrosynthesis
- Structure Prediction
- Antibody Engineering
- CDR Generation
- Quantum Chemistry
- Drug Efficacy
- Molecular Dynamics (framework)
- Genomics (framework)
- Machine Learning (framework)
- Protein Engineering
- Visualization

✅ **15 API Endpoints**

✅ **Comprehensive Data**
- 6 Protein Targets
- 7 Drug Ligands
- 4 Cell Lines
- Antibody Templates
- CDR Libraries

✅ **Production Ready**
- Error handling
- Input validation
- CORS enabled
- Health checks
- Statistics

---

## Local Testing

```bash
npm install
npm start

# Test locally:
curl http://localhost:10000/api/health
```

---

## Your App is Ready!

Visit: `https://your-app-name.onrender.com`

Features:
- 🧬 Full BioMed computational platform
- 📡 RESTful API with 15 endpoints
- 🔬 All ComputeLab features integrated
- ⚗️ Scientific disclaimers included
- 📚 Complete documentation

**Remember**: All computational predictions require experimental validation!
