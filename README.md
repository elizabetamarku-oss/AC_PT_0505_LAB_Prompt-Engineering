How to Run the Project
Install dependencies:

bash
pip install -r requirements.txt
Add your API key to an environment variable:

bash
export OPENAI_API_KEY="your_key_here"
Run the main script:

bash
python main.py
To run consistency tests:

bash
python consistency_tests.py
Repository Structure
Code
├── main.py                     # Runs single examples of each prompt
├── consistency_tests.py        # Runs 15-run consistency tests for v1, v2, v3
├── prompts/
│   ├── sentiment_prompts.py    # v1, v2, v3 sentiment prompts
│   ├── extraction_prompts.py   # v1, v2, v3 extraction prompts
│   └── product_prompts.py      # v1, v2, v3 product prompts
├── utils/
│   ├── openai_client.py        # call_openai() wrapper
│   ├── cleaners.py             # JSON cleaners, text cleaners
│   └── scoring.py              # consistency scoring function
├── results/
│   ├── sentiment/              # run logs + outputs
│   ├── extraction/
│   └── product/
├── lab_summary.md              # Required narrative summary (NOT in README)
├── requirements.txt
└── README.md
