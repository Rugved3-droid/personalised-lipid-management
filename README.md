# personalised-lipid-management
Artificial intelligence based personalised lipid management tool 

# Voice-Driven Clinical Decision Support for Lipid Management

A clinical decision support tool that integrates structured clinical trial data with artificial intelligence to provide personalized lipid management recommendations.

## Overview

This tool addresses key barriers to optimal lipid management through:
- *Voice-driven input* using natural language processing
- *Quantitative trial matching* to 9 landmark lipid-lowering trials
- *AI-powered guideline synthesis* comparing 5 international guidelines
- *Personalized treatment recommendations* with evidence-based rationale

## Features

- *Natural Language Input*: Describe patients verbally - the system extracts structured data automatically
- *Trial Eligibility Assessment*: Detailed analysis of inclusion/exclusion criteria for each trial
- *Multi-Guideline Comparison*: ACC/AHA, ESC/EAS, NICE, CCS, and JAS recommendations
- *Specific Treatment Plans*: Drug recommendations with expected LDL reductions

## Video Demonstration

📺 Watch the tool in action: [https://youtu.be/evuxQ61AEPc](https://youtu.be/evuxQ61AEPc)

## Installation

### Prerequisites

- Python 3.8+
- OpenAI API key

### Setup

1. Install dependencies:
bash
pip install -r requirements.txt


2. Set up your OpenAI API key:
bash
export OPENAI_API_KEY='your-api-key-here'


3. Run the application:
bash
streamlit run app.py


## Requirements


streamlit>=1.24.0
openai>=1.0.0
python-dotenv>=1.0.0


## Clinical Trial Database

The tool includes 9 landmark trials:

| Trial | Drug Class | Key Population |
|-------|-----------|----------------|
| 4S | Statin | Secondary prevention, high cholesterol |
| PROVE-IT TIMI 22 | Statin | Post-ACS (within 10 days) |
| JUPITER | Statin | Primary prevention, elevated hsCRP |
| IMPROVE-IT | Ezetimibe | Post-ACS, on statin therapy |
| FOURIER | PCSK9 inhibitor | ASCVD, on statin, LDL ≥70 |
| ODYSSEY OUTCOMES | PCSK9 inhibitor | Post-ACS |
| ORION-10 | PCSK9 inhibitor (siRNA) | ASCVD, elevated LDL |
| CLEAR Outcomes | Bempedoic acid | Statin intolerant |
| REDUCE-IT | Icosapent ethyl | Elevated triglycerides |

## Usage

1. *Click the microphone* to start recording
2. *Describe your patient* naturally:
   - Age and sex
   - Cardiovascular history (MI, stroke, etc.)
   - Laboratory values (LDL, HDL, TG, HbA1c, eGFR)
   - Current medications
   - Risk factors (diabetes, hypertension, smoking)
   - Any intolerances
3. *Review extracted data* for accuracy
4. *Examine trial matching results* - see which trials apply and why
5. *Receive guideline-based recommendations* with specific targets and medications

## Example Input

> "64-year-old male, had an MI 3 months ago, has diabetes and hypertension. Currently on atorvastatin 40mg. Labs show LDL 138, HDL 38, triglycerides 165, HbA1c 7.8, eGFR 72."

## Output Components

1. *Patient Summary*: Structured extraction of clinical data
2. *Trial Matching*: Detailed eligibility for each trial with:
   - Inclusion criteria met
   - Inclusion criteria not met
   - Exclusion criteria triggered
   - Match percentage
3. *Guideline Comparison*: Recommendations from multiple societies
4. *Final Recommendations*: Specific treatment plan with rationale

## Important Disclaimers

⚠️ *This tool is for educational and decision support purposes only.*

- Does NOT replace clinical judgment
- Requires validation before clinical implementation
- AI outputs are probabilistic and may contain errors
- Patient data is processed in-session only (no permanent storage)
- Always verify recommendations against current guidelines

## Privacy & Data Handling

- *Stateless operation*: No patient data permanently stored
- Audio transmitted to OpenAI Whisper API for transcription
- Clinical text processed by GPT-4 for analysis
- Users advised to avoid entering actual patient identifiers
- Compliant with research/educational use cases


## Author

- *Rugved Parmar, MD* - SUNY Downstate Health Sciences University

## Contact

For questions or collaboration inquiries:
- Email: Rugved.parmar@downstate.edu
- Institution: SUNY Downstate Health Sciences University, Brooklyn, NY

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- OpenAI for Whisper and GPT-4 APIs
- Clinical trial investigators whose work forms the evidence base
- International guideline committees (ACC/AHA, ESC/EAS, NICE, CCS, JAS)

## Future Development

- Electronic health record integration
- Expanded trial database
- Coronary artery calcium score integration
- Lipoprotein(a) assessment
- Pharmacogenomic considerations (SLCO1B1)
- Cost-effectiveness analysis
- Multi-language support

---

Note: This is a proof-of-concept tool. Formal validation studies are required before clinical implementation.
