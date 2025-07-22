# 📊 COVID-FLU-TREATMENT-ACCESS-FLORIDA

Analyzes therapeutic access for COVID-19 and flu across Florida using public health provider data to identify geographic treatment gaps, provider disparities, and government program participation. Leverages Tableau for geospatial dashboards and granular availability analysis to inform equitable resource distribution and public health planning.



## 🔍 Problem Statement

While COVID-19 and flu remain persistent threats to public health, access to treatments like **Paxlovid**, **Lagevrio**, and **Tamiflu** varies widely across Florida. Certain communities, particularly rural areas, may lack nearby providers with available therapeutics, creating **treatment deserts** that put vulnerable populations at risk.

Despite the availability of **USG-supported programs** like **PAP (Patient Assistance Program)** and **ICATT (Increasing Community Access to Testing)**, participation among pharmacy providers remains inconsistent. Similarly, some major pharmacy chains stock treatments more consistently than others. There is limited transparency around these access patterns.

This project uses provider-level therapeutic availability data to explore access inequalities, identify underserved areas, and guide data-driven public health response efforts across Florida.



## 🎯 Project Objectives

- Map COVID-19 and flu treatment availability across Florida  
- Identify underserved counties or ZIP codes lacking access to key therapeutics  
- Compare provider participation in PAP and ICATT programs  
- Analyze availability trends by pharmacy chain (CVS, Walgreens, Publix, etc.)  
- Determine overlap of providers offering both flu and COVID-19 treatments  
- Reveal geographic clusters of low access to Paxlovid, Lagevrio, or Tamiflu  
- Assess commercial vs. government-supplied product distribution  
- Recommend focus areas for health policy or outreach efforts  


## 🗂️ Data Source

**Source:** HHS (Health and Human Services) Provider Therapeutics Data (Extracted Sample)  

**Key Columns:**

- Provider Name, City, State, Latitude, Longitude  
- Is PAP Site / Is ICATT Site  
- Has Paxlovid / Has USG Paxlovid / Has Commercial Paxlovid  
- Has Lagevrio / Has USG Lagevrio / Has Commercial Lagevrio  
- Has Veklury  
- Has Oseltamivir (Generic / Suspension / Tamiflu)  
- Has Baloxavir, Zanamivir, Peramivir  
- Is COVID-19 Site / Is Flu Site  



## 🧰 Tools Used

| Tool    | Purpose                                               |
|---------|-------------------------------------------------------|
| Excel   | Data cleaning, recoding pharmacy chains               |
| Tableau | Interactive dashboards, geographic and KPI analysis   |
| SQL     | Querying joined demographic or ZIP datasets (optional)|
| Python  | Generating calculated fields or clustering (optional) |


## 📊 Key Analyses to Perform

### 1. 📍 Geographic Access & Treatment Gaps

- Map Florida providers using **latitude/longitude**
- Color-code by treatment availability (Paxlovid, Lagevrio, Veklury)
- Apply filters for **PAP** and **ICATT** participation
- Use **density maps** to reveal underserved rural areas



### 2. 🏥 Provider Type Analysis

- Create calculated field for **Pharmacy Chain Name**  
  (_e.g., if “CVS” in name → "CVS"_)
- Compare treatment availability by chain
- Rank chains by:
  - Paxlovid availability
  - PAP participation
  - Flu vs COVID coverage



### 3. 🔁 Flu vs. COVID Treatment Coverage

- Classify sites as offering:
  - Only Flu
  - Only COVID
  - Both
- Use **stacked bar charts** or **matrix visuals** for comparison



### 4. 🧪 PAP / ICATT Program Participation

- Visualize participation by:
  - City / ZIP code
  - Provider chain
- Compare against therapeutic availability
- Identify gaps where providers lack USG support



### 5. 🧮 Commercial vs. USG Product Analysis

- Side-by-side bar charts comparing **commercial vs USG** product stock
- Identify providers stocking **only commercial products**
- Highlight **distribution equity issues**


## 📈 Tableau Dashboard Ideas

| Component               | Description                                                   |
|------------------------|---------------------------------------------------------------|
| 🌍 Interactive Map     | Plot providers with color/shape filters for treatment access  |
| 📊 Bar Chart by Pharmacy | Compare availability by chain (CVS, Walgreens, etc.)         |
| 🧾 KPI Cards           | Show % with Paxlovid, % in PAP, % with both treatments         |
| 🧱 Matrix Heatmap      | Provider vs. medications (binary availability)                 |
| 🔁 Flu vs COVID Chart  | Pie or bar chart: providers by treatment type                 |
| 🔬 USG vs Commercial   | Side-by-side comparison of supply source                       |
| 📌 ZIP Code Gaps       | Highlight areas with no access to COVID/flu treatments         |



## 📦 Deliverables

- ✅ Cleaned and enriched dataset (ZIP codes, geocoding, pharmacy classification)
- ✅ Tableau dashboard with multiple interactive views
- ✅ KPI summary cards for executive insights
- ✅ PDF/Slide report with visuals, gaps, and strategic recommendations



## 🧠 Stakeholder Impact

| Stakeholder          | Benefit                                                                 |
|----------------------|-------------------------------------------------------------------------|
| **Florida DOH**      | Identify underserved areas, plan drug distribution, ICATT/PAP expansion |
| **Pharmacy Chains**  | Benchmark against competitors, increase participation visibility        |
| **NGOs / Clinics**   | Target outreach to underserved ZIPs                                     |
| **Public Health Researchers** | Study systemic gaps in access and policy effectiveness             |


## 📁 Project Structure (Optional)

```bash
.
├── README.md
├── /data
│   ├── cleaned_provider_data.xlsx
│   └── raw_provider_sample.csv
├── /tableau
│   └── covid_flu_dashboard.twbx
├── /docs
│   ├── summary_slide_deck.pdf
│   └── treatment_gap_analysis.pdf


-MoH/Government	Track rollout progress, promote equitable distribution
