**Lucky Cement Urdu ASR and NER System:**

<p>
This repository contains the implementation of an Automatic Speech Recognition (ASR) and Named Entity Recognition (NER) system for Lucky Cement Limited, developed as part of Joyn Digital's AI/ML initiatives. The project involved fine-tuning OpenAI's Whisper model for Urdu and mixed-language speech transcription, along with a custom NER model to extract market-relevant entities.
</p>

**Project Overview:**
<p>
Field staff of Lucky Cement visit various outlets to collect market intelligence. This project automates the process by:
</p>
  -Capturing audio conversations.

  -Transcribing them into text.

  -Extracting actionable insights, such as:

  -Cement prices (retail, landed rate, etc.)

  -Stock availability

  -Transport details

  -Competitive brand analysis (DG, Falcon, PakLand, etc.)

**Workflow:**

graph TD
    A[Audio Data Collection] -->|Preprocessing| B[Voice Activity Detection (VAD)]
    B -->|Noise Reduction| C[Speech-to-Text (STT) with Whisper]
    C -->|Transcription Output| D[Named Entity Recognition (NER)]
    D -->|Entity Extraction| E[Market Insights]

**Components**

Voice Activity Detection (VAD):

  Tool Used: Silero-VAD

  Purpose: Isolates speech segments and removes noise for cleaner transcription inputs.

**Speech-to-Text (STT):**
  Model Used: OpenAI Whisper (fine-tuned for Urdu and mixed-language transcription).

  Outcome: Improved transcription accuracy across 4 iterations with reduced word error rates.

**Named Entity Recognition (NER):**
  Approach: Extracts relevant entities like product prices, stock details, and competitor information.

  Performance: Achieved an overall accuracy of 67.2% after 3 iterations.

**Deployment:**
  Fully deployed on AWS.

  Automated daily processing of audio data at 9:00 PM.

  Outputs integrated into Lucky Cement's Secondary Sales System under Market Intel Analytics.


**Results and Insights:**

  -Transcription Examples: Available in data/example_transcriptions/.

  -NER Outputs: Available in data/example_ner_outputs/.

  -Detailed progress and accuracy reports are available in the results/ directory.

**Technologies Used:**
  -Silero-VAD for noise filtering and speech isolation.

  -OpenAI Whisper for ASR.

  -Custom NER model for extracting domain-specific entities.

  -AWS for deployment and integration.

**Contact:**

  For any inquiries, please contact zainulabideen1796@gmail.com
