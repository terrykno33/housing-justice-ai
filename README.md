
This is the full code starter. Streamlit runs Python apps with streamlit run app.py, and Streamlit uses requirements.txt in the root of the repository for dependencies. The OpenAI API docs include the Responses API, which this starter app uses for the AI responses.

Folder setup

Your repo should look like this:

housing-justice-ai/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env.example
│
├── prompts/
│   └── system_prompt.txt
│
└── data/
    └── sample_case_template.txt

First, in VS Code Terminal, run:

mkdir prompts
mkdir data
1. README.md

Copy this into your README.md file:

# housing-justice-ai

Legal information and case-preparation assistant for tenants, voucher holders, EHV participants, and housing justice support.

Created by Terry Knowles.

## Purpose

Housing Justice AI is a legal information and case-preparation assistant designed to help tenants, voucher holders, Emergency Housing Voucher participants, seniors, students, and low-income families understand housing issues, organize evidence, prepare for hearings, and identify possible problems involving landlords, housing authorities, unsafe housing, retaliation, eviction, and program termination.

This app does not replace a licensed attorney. It helps users prepare, organize facts, understand documents, and ask better questions when dealing with legal aid, housing authorities, property managers, courts, inspectors, and advocates.

## Main Features

- Case dashboard
- Evidence analyzer
- Retaliation detector
- Voucher protection assistant
- Hearing coach
- Regulation finder
- Exportable case summary

## Knowledge Areas

Housing Justice AI focuses on:

- Emergency Housing Vouchers
- Housing Choice Voucher Program
- HUD regulations
- 24 CFR Part 982
- Voucher expiration and extension issues
- Security deposit and move-in assistance
- Informal hearings
- Termination of assistance
- Reasonable accommodations
- Relocation assistance
- Evictions
- Possession cases
- Lease violations
- Retaliation
- Habitability issues
- Unsafe living conditions
- Asbestos
- Mold
- Water leaks
- Ceiling damage
- Structural defects
- Failed inspections
- Code violations
- Housing Quality Standards
- Court and hearing preparation

## Important Warning

This software provides legal information and case-preparation support only. It does not provide legal representation and does not replace advice from a licensed attorney.

Do not upload private evidence, API keys, court documents, personal IDs, or confidential information to a public GitHub repository.

Keep this repository private while building.

## Setup Instructions

### 1. Clone or download the repository

```powershell
git clone https://github.com/YOUR-GITHUB-USERNAME/housing-justice-ai.git
cd housing-justice-ai

Replace YOUR-GITHUB-USERNAME with your real GitHub username.

2. Create a Python virtual environment
py -m venv .venv
3. Activate the virtual environment
.\.venv\Scripts\Activate.ps1
4. Upgrade pip
python -m pip install --upgrade pip
5. Install the required packages
pip install -r requirements.txt
6. Create your environment file

Copy .env.example and rename the copy to .env.

Inside .env, add your real API key:

OPENAI_API_KEY=your_real_api_key_here
OPENAI_MODEL=gpt-4.1-mini

Never upload .env to GitHub.

7. Run the app
streamlit run app.py

If that does not work, run:

python -m streamlit run app.py
GitHub Commands

Use these commands to save your work to GitHub:

git status
git add .
git commit -m "Add Housing Justice AI app files"
git push
First Commit Message
Initial commit for Housing Justice AI
Project Status

This is the first working MVP version of Housing Justice AI.


---

## 2. `.gitignore`

Copy this into your **.gitignore** file:

```gitignore
.env
.venv/
__pycache__/
*.pyc
.DS_Store
*.log

uploads/
case_files/
private_evidence/
private_docs/
personal_documents/

*.pdf
*.docx
*.jpg
*.jpeg
*.png

.vscode/
3. .env.example

Copy this into your .env.example file:

OPENAI_API_KEY=
OPENAI_MODEL=gpt-4.1-mini

Your real .env file should look like this later:

OPENAI_API_KEY=put_your_real_api_key_here
OPENAI_MODEL=gpt-4.1-mini
4. requirements.txt

Copy this into your requirements.txt file:

streamlit
openai
python-dotenv
pypdf
python-docx
5. prompts/system_prompt.txt

Copy this into prompts/system_prompt.txt:

You are Housing Justice AI, created by Terry Knowles.

You are a legal information and case-preparation assistant. You are not a licensed attorney. You do not provide legal representation. Your role is to help tenants, voucher holders, EHV participants, seniors, students, and low-income families organize evidence, understand housing issues, prepare for hearings, and ask better questions when speaking with legal aid or licensed attorneys.

Core rules:

1. Tell the truth.
2. Never invent facts.
3. Separate facts from assumptions.
4. Separate legal information from legal advice.
5. Clearly state when evidence is missing.
6. Explain both sides of an issue.
7. Use plain language.
8. Be calm, respectful, and organized.
9. Do not guarantee outcomes.
10. Encourage the user to contact legal aid or a licensed attorney for legal representation.

You help with:

- Emergency Housing Vouchers
- Housing Choice Voucher Program
- HUD regulations
- 24 CFR Part 982
- Voucher expiration and extension issues
- Security deposit and move-in assistance
- Informal hearings
- Termination of assistance
- Reasonable accommodations
- Relocation assistance
- Participant rights and obligations
- Eviction cases
- Possession cases
- Lease violations
- Retaliation
- Habitability issues
- Repair problems
- Unsafe living conditions
- Security deposits
- Fair housing complaints
- Notice requirements
- Asbestos
- Mold
- Water leaks
- Ceiling damage
- Structural defects
- Lead paint
- Unsafe repairs
- Failed inspections
- Code violations
- Housing Quality Standards
- Timelines
- Evidence lists
- Opening statements
- Closing statements
- Witness questions
- Questions for housing authority staff
- Questions for property managers
- Exhibit lists
- Appeal preparation notes
- Legal aid summaries

When analyzing a case, look for:

- Important dates
- Deadlines
- Contradictions
- Missing documents
- Repeated notices
- Retaliation patterns
- Unsafe housing issues
- Voucher barriers
- Expired documents
- Failure to explain program benefits
- Failure to provide relocation assistance
- Evidence of attempts to comply
- Evidence of communication with landlords, housing authorities, inspectors, or courts

When the user asks about retaliation, look for patterns such as:

- Tenant complains, then receives eviction notice
- Tenant requests repairs, then receives lease violation
- Tenant reports unsafe conditions, then housing assistance is threatened
- Tenant asks for relocation, then program termination begins
- Tenant uses legal rights, then management increases pressure

When the user asks about voucher issues, ask or analyze:

- Date voucher was issued
- Date voucher expired
- Whether an extension was requested
- Whether the user was given expired documents
- Whether the housing authority explained EHV benefits
- Whether security deposit assistance was explained
- Whether moving assistance was explained
- Whether the user contacted apartments
- Whether emails prove attempts to lease a unit
- Whether unsafe conditions or retaliation interfered with moving

Always produce organized output with headings, bullet points, and clear next steps.
6. data/sample_case_template.txt

Copy this into data/sample_case_template.txt:

Housing Justice AI Case Template

User Name:
Address:
City/State:
Housing Program:
Housing Authority:
Property Name:
Property Manager:
Case Manager:
Court Case Number:
Hearing Date:
Appeal Date:
Voucher Issue Date:
Voucher Expiration Date:

Main Issue:
Example: Housing authority says I failed to use my voucher.

Important Facts:
1.
2.
3.
4.
5.

Important Dates:
1.
2.
3.
4.
5.

Documents I Have:
- Voucher document
- Termination letter
- Eviction notice
- Emails
- Inspection report
- Photos
- Lease
- Court paperwork
- Repair requests

Questions I Need Answered:
1.
2.
3.

Possible Problems:
- Expired voucher
- No explanation of EHV benefits
- No security deposit assistance explained
- Unsafe housing conditions
- Retaliation
- Failed inspection
- Eviction or possession case
- Termination from program
- Relocation request ignored

Legal Aid Summary:
I need help reviewing whether my housing authority, landlord, or property manager violated my rights or failed to follow proper housing program procedures.
7. app.py

Copy this whole code into app.py:

from __future__ import annotations

import os
from datetime import datetime
from pathlib import Path
from typing import List

import streamlit as st
from dotenv import load_dotenv

try:
    from openai import OpenAI
except Exception:
    OpenAI = None

try:
    from pypdf import PdfReader
except Exception:
    PdfReader = None

try:
    import docx
except Exception:
    docx = None


# -----------------------------
# Basic setup
# -----------------------------

load_dotenv()

APP_DIR = Path(__file__).parent
PROMPT_PATH = APP_DIR / "prompts" / "system_prompt.txt"
SAMPLE_TEMPLATE_PATH = APP_DIR / "data" / "sample_case_template.txt"


def load_text_file(path: Path, fallback: str = "") -> str:
    if path.exists():
        return path.read_text(encoding="utf-8", errors="ignore")
    return fallback


SYSTEM_PROMPT = load_text_file(
    PROMPT_PATH,
    fallback=(
        "You are Housing Justice AI. You provide legal information and "
        "case-preparation help, but you are not a licensed attorney."
    ),
)


# -----------------------------
# Streamlit page config
# -----------------------------

st.set_page_config(
    page_title="Housing Justice AI",
    page_icon="⚖️",
    layout="wide",
)


# -----------------------------
# Session state
# -----------------------------

if "case_summary" not in st.session_state:
    st.session_state.case_summary = ""

if "evidence_text" not in st.session_state:
    st.session_state.evidence_text = ""

if "last_ai_output" not in st.session_state:
    st.session_state.last_ai_output = ""


# -----------------------------
# File reading helpers
# -----------------------------

def read_uploaded_file(uploaded_file) -> str:
    """
    Reads uploaded text, markdown, PDF, and DOCX files.
    Images are not OCR-scanned in this MVP.
    """
    file_name = uploaded_file.name
    suffix = Path(file_name).suffix.lower()

    try:
        if suffix in [".txt", ".md", ".csv"]:
            return uploaded_file.read().decode("utf-8", errors="ignore")

        if suffix == ".pdf":
            if PdfReader is None:
                return "PDF support is not available. Install pypdf."
            reader = PdfReader(uploaded_file)
            pages = []
            for i, page in enumerate(reader.pages, start=1):
                text = page.extract_text() or ""
                pages.append(f"\n--- Page {i} ---\n{text}")
            return "\n".join(pages)

        if suffix == ".docx":
            if docx is None:
                return "DOCX support is not available. Install python-docx."
            document = docx.Document(uploaded_file)
            paragraphs = [p.text for p in document.paragraphs if p.text.strip()]
            return "\n".join(paragraphs)

        return (
            f"File uploaded: {file_name}\n"
            "This file type is not text-readable in this MVP. "
            "Supported: .txt, .md, .csv, .pdf, .docx"
        )

    except Exception as error:
        return f"Could not read {file_name}. Error: {error}"


# -----------------------------
# AI helper
# -----------------------------

def offline_response(task_name: str) -> str:
    """
    Response shown when no API key is available.
    """
    return f"""
## {task_name}

AI mode is not active yet because no OpenAI API key was found.

You can still use this app to organize your case.

### What to collect

- Notices
- Emails
- Voucher documents
- Termination letters
- Inspection reports
- Lease papers
- Court paperwork
- Repair requests
- Photos
- Names of people involved
- Dates of phone calls or meetings

### What to write down

- What happened?
- Who was involved?
- What date did it happen?
- What document proves it?
- What did you ask for?
- What response did you receive?
- Was there a deadline?
- Was there a hearing date?

### Reminder

This app gives legal information and case-preparation help. It does not replace a licensed attorney.
"""


def call_ai(task_name: str, user_request: str) -> str:
    """
    Calls OpenAI if an API key exists.
    Falls back to offline guidance if not.
    """
    api_key = os.getenv("OPENAI_API_KEY", "").strip()
    model = os.getenv("OPENAI_MODEL", "gpt-4.1-mini").strip()

    if not api_key or OpenAI is None:
        return offline_response(task_name)

    client = OpenAI(api_key=api_key)

    case_summary = st.session_state.get("case_summary", "")
    evidence_text = st.session_state.get("evidence_text", "")

    full_input = f"""
Task:
{task_name}

User request:
{user_request}

Case summary:
{case_summary}

Uploaded or pasted evidence:
{evidence_text}

Instructions:
Provide a clear, organized response.
Separate facts from assumptions.
Identify missing evidence.
Do not pretend to be an attorney.
Do not guarantee a legal outcome.
Use plain language.
Give practical next steps.
"""

    try:
        response = client.responses.create(
            model=model,
            instructions=SYSTEM_PROMPT,
            input=full_input,
        )
        return response.output_text

    except Exception as error:
        return f"""
## AI Error

The app could not call the AI model.

Error:

```text
{error}

Check your .env file and make sure your API key is correct.
"""

-----------------------------
Sidebar
-----------------------------

st.sidebar.title("Housing Justice AI")
st.sidebar.caption("Created by Terry Knowles")

st.sidebar.warning(
"Legal information only. This app does not replace a licensed attorney."
)

case_name = st.sidebar.text_input(
"Case name",
value="Housing Justice AI Case",
)

housing_program = st.sidebar.selectbox(
"Housing program",
[
"Emergency Housing Voucher",
"Housing Choice Voucher / Section 8",
"Public Housing",
"Rapid Rehousing",
"Other",
"Not sure",
],
)

city_state = st.sidebar.text_input(
"City / State",
value="Fort Worth, Texas",
)

case_status = st.sidebar.selectbox(
"Case status",
[
"Organizing evidence",
"Voucher problem",
"Termination notice",
"Informal hearing",
"Eviction filed",
"Appeal filed",
"Need legal aid",
"Other",
],
)

-----------------------------
Header
-----------------------------

st.title("⚖️ Housing Justice AI")
st.subheader("Legal information and case-preparation assistant")

st.info(
"Use this tool to organize housing documents, voucher issues, unsafe housing problems, "
"retaliation concerns, and hearing preparation notes."
)

-----------------------------
Tabs
-----------------------------

tab_dashboard, tab_upload, tab_evidence, tab_retaliation, tab_voucher, tab_hearing, tab_regulation, tab_export = st.tabs(
[
"Case Dashboard",
"Upload Evidence",
"Evidence Analyzer",
"Retaliation Detector",
"Voucher Protection",
"Hearing Coach",
"Regulation Finder",
"Export Summary",
]
)

-----------------------------
Case dashboard
-----------------------------

with tab_dashboard:
st.header("Case Dashboard")

st.write("Start by writing the basic facts of your situation.")

st.session_state.case_summary = st.text_area(
    "Case summary",
    value=st.session_state.case_summary,
    height=250,
    placeholder=(
        "Example: I am an EHV participant. The housing authority says I failed to use my voucher. "
        "I believe I was given expired documents and was not properly informed about security deposit assistance."
    ),
)

col1, col2, col3 = st.columns(3)

with col1:
    st.text_input("Housing authority", placeholder="Example: Fort Worth Housing Solutions")

with col2:
    st.text_input("Property / apartment", placeholder="Example: Buena Vista Apartments")

with col3:
    st.text_input("Court case number", placeholder="Example: JP05-26-E00046022")

st.divider()

st.subheader("Quick checklist")

st.checkbox("I have a voucher document")
st.checkbox("I have a termination letter")
st.checkbox("I have emails to or from the housing authority")
st.checkbox("I have emails to or from an apartment")
st.checkbox("I have inspection reports")
st.checkbox("I have repair requests")
st.checkbox("I have court paperwork")
st.checkbox("I have photos or videos")
-----------------------------
Upload evidence
-----------------------------

with tab_upload:
st.header("Upload Evidence")

st.write(
    "Upload documents you want the app to review. For privacy, do not upload personal documents "
    "to a public GitHub repository. Keep your evidence local on your computer."
)

uploaded_files = st.file_uploader(
    "Upload files",
    type=["txt", "md", "csv", "pdf", "docx"],
    accept_multiple_files=True,
)

if uploaded_files:
    evidence_blocks: List[str] = []

    for uploaded_file in uploaded_files:
        text = read_uploaded_file(uploaded_file)
        evidence_blocks.append(f"\n\n# FILE: {uploaded_file.name}\n\n{text}")

    st.session_state.evidence_text = "\n".join(evidence_blocks)

    st.success("Evidence loaded into the app.")

    with st.expander("Preview extracted text"):
        st.text_area(
            "Extracted evidence text",
            value=st.session_state.evidence_text[:30000],
            height=350,
        )

st.subheader("Or paste evidence manually")

pasted_evidence = st.text_area(
    "Paste notice, email, voucher text, or hearing letter here",
    height=200,
)

if st.button("Add pasted evidence"):
    st.session_state.evidence_text += f"\n\n# PASTED EVIDENCE\n\n{pasted_evidence}"
    st.success("Pasted evidence added.")
-----------------------------
Evidence Analyzer
-----------------------------

with tab_evidence:
st.header("Evidence Analyzer")

st.write(
    "This section looks for important dates, contradictions, missing evidence, and possible defenses."
)

evidence_request = st.text_area(
    "What do you want the Evidence Analyzer to focus on?",
    value=(
        "Review the case summary and evidence. Identify important dates, contradictions, "
        "missing documents, possible defenses, and questions to ask at a hearing."
    ),
    height=120,
)

if st.button("Run Evidence Analyzer"):
    output = call_ai("Evidence Analyzer", evidence_request)
    st.session_state.last_ai_output = output
    st.markdown(output)
-----------------------------
Retaliation Detector
-----------------------------

with tab_retaliation:
st.header("Retaliation Detector")

st.write(
    "This section looks for patterns where complaints, repair requests, or protected activity were followed by negative actions."
)

retaliation_request = st.text_area(
    "Describe the retaliation concern",
    value=(
        "Look for retaliation patterns. Did complaints, repair requests, inspection reports, "
        "or requests for relocation happen before eviction notices, lease violations, pressure, "
        "or termination threats?"
    ),
    height=120,
)

if st.button("Run Retaliation Detector"):
    output = call_ai("Retaliation Detector", retaliation_request)
    st.session_state.last_ai_output = output
    st.markdown(output)
-----------------------------
Voucher Protection Assistant
-----------------------------

with tab_voucher:
st.header("Voucher Protection Assistant")

st.write(
    "This section helps organize voucher issue dates, expiration dates, extension requests, apartment contacts, and EHV benefit questions."
)

col1, col2 = st.columns(2)

with col1:
    voucher_issue_date = st.date_input("Voucher issue date", value=None)

with col2:
    voucher_expiration_date = st.date_input("Voucher expiration date", value=None)

apartments_contacted = st.text_area(
    "Apartments contacted",
    placeholder="List apartment names, dates, emails, and responses.",
    height=120,
)

voucher_request = f"""

Analyze the voucher issue.

Voucher issue date:
{voucher_issue_date}

Voucher expiration date:
{voucher_expiration_date}

Apartments contacted:
{apartments_contacted}

Focus on:

Whether the voucher or packet may have been expired
Whether an extension was requested or needed
Whether EHV security deposit or move-in assistance was explained
Whether the tenant made real attempts to lease a unit
What evidence should be gathered

What questions should be asked at a hearing
"""

if st.button("Run Voucher Protection Assistant"):
output = call_ai("Voucher Protection Assistant", voucher_request)
st.session_state.last_ai_output = output
st.markdown(output)

-----------------------------
Hearing Coach
-----------------------------

with tab_hearing:
st.header("Hearing Coach")

st.write(
    "This section helps build opening statements, witness questions, closing statements, and exhibit lists."
)

hearing_type = st.selectbox(
    "Hearing type",
    [
        "Informal hearing",
        "Eviction hearing",
        "Appeal",
        "Legal aid meeting",
        "Housing authority meeting",
        "Other",
    ],
)

hearing_request = st.text_area(
    "What do you need for the hearing?",
    value=(
        "Prepare a short statement of facts, a timeline, questions for witnesses, "
        "a list of documents to bring, and a respectful closing statement."
    ),
    height=140,
)

if st.button("Run Hearing Coach"):
    output = call_ai(
        "Hearing Coach",
        f"Hearing type: {hearing_type}\n\nRequest:\n{hearing_request}",
    )
    st.session_state.last_ai_output = output
    st.markdown(output)
-----------------------------
Regulation Finder
-----------------------------

with tab_regulation:
st.header("Regulation Finder")

st.write(
    "This section helps you identify what housing rules or legal topics may be relevant. "
    "This MVP does not automatically browse the web. It prepares research questions and issue areas."
)

regulation_topic = st.text_input(
    "What rule or issue do you want to research?",
    placeholder="Example: EHV voucher expiration, informal hearing rights, HQS failed inspection",
)

regulation_request = f"""

Identify possible regulation topics and research questions for this issue:

{regulation_topic}

Include:

HUD or federal housing topics to research
Texas landlord-tenant topics to research
Fair housing topics to research
What documents to look for

What questions to ask legal aid
"""

if st.button("Run Regulation Finder"):
output = call_ai("Regulation Finder", regulation_request)
st.session_state.last_ai_output = output
st.markdown(output)

-----------------------------
Export Summary
-----------------------------

with tab_export:
st.header("Export Summary")

export_text = f"""# Housing Justice AI Case Summary

Created: {datetime.now().strftime("%Y-%m-%d %I:%M %p")}

Case Name

{case_name}

Housing Program

{housing_program}

City / State

{city_state}

Case Status

{case_status}

Case Summary

{st.session_state.get("case_summary", "")}

Evidence Text

{st.session_state.get("evidence_text", "")}

Last AI Output

{st.session_state.get("last_ai_output", "")}

Reminder

This document is for legal information and case-preparation support only. It is not legal advice and does not replace a licensed attorney.
"""

st.download_button(
    label="Download case summary",
    data=export_text,
    file_name="housing_justice_ai_case_summary.md",
    mime="text/markdown",
)

with st.expander("Preview export"):
    st.markdown(export_text)

---

## Now run the app

After all files are saved, run this in VS Code PowerShell:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
streamlit run app.py

If Streamlit does not start, run:

python -m streamlit run app.py
Then save everything to GitHub

Run this:

git status
git add .
git commit -m "Add Housing Justice AI app files"
git push

Your blank parts to fill in are only these:

YOUR-GITHUB-USERNAME
OPENAI_API_KEY

Do not put your real .env, private evidence, court documents, or personal documents into GitHub.
