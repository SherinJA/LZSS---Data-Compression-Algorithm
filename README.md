# LZSS Data Compression Algorithm

## Overview

This is a Python-based tool that implements the Lempel-Ziv-Storer-Szymanski (LZSS) algorithm, a lossless data compression technique. This project provides an interactive interface using Streamlit to compress and decompress text, display compression statistics, and visualize the step-by-step process. LZSS is an enhancement of the LZ77 algorithm, optimizing for efficiency by encoding repeated patterns as pointers or literals based on their benefit to compression.

This project was developed as part of an assignment for the course *Multimedia Compression Techniques* at PSG College of Technology, Anna University.

## Features

- **Lossless Compression:** Compresses text using the LZSS algorithm while ensuring no data loss.
- **Interactive Interface:** Streamlit-based GUI for inputting text and configuring buffer sizes.
- **Detailed Steps:** Displays compression and decompression steps in tabular format.
- **Compression Statistics:** Provides metrics like original size, compressed size, compression ratio, and space savings.
- **Verification:** Confirms successful decompression by comparing original and decompressed text.

## Prerequisites

To run this project, ensure you have the following:

- **Python 3.8+**
- **Operating System:** Windows, macOS, or Linux.
- **Dependencies:** All required Python libraries are listed in `requirements.txt`.

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/lzss-compression-demo.git
   cd lzss-compression-demo
   ```

2. **Create a Virtual Environment (Optional but Recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` should include:

   ```
   streamlit==1.38.0
   tabulate==0.9.0
   pandas==2.2.3
   ```

## Usage

1. **Run the Application:**

   ```bash
   streamlit run lzss_streamlit.py
   ```

2. **Interact with the Interface:**

   - Open the provided URL (usually `http://localhost:8501`) in your browser.
   - Enter the text to compress (default: "abracadabracabra").
   - Adjust the **Search Buffer Size** (1–15, default: 7) and **Lookahead Buffer Size** (1–10, default: 5) using sliders.
   - Click **Compress** to process the input.
   - View the original text, decompressed text, compression statistics, and detailed compression/decompression steps.

3. **Sample Output:**

   - **Original Text:** Displays the input text.
   - **Decompressed Text:** Shows the reconstructed text with a success/error message.
   - **Compression Statistics:** Includes original size, compressed size, compression ratio, and space savings percentage.
   - **Steps Tables:** DataFrames showing the state of buffers and outputs at each step.


## Limitations

- **Buffer Size Constraints:** Compression efficiency depends on search and lookahead buffer sizes, which are limited to balance performance.
- **Non-Repetitive Data:** Less effective for text with few repeated patterns, resulting in minimal compression.
- **Bit-Level Encoding:** The current implementation simplifies bit allocation for demonstration; real-world applications may optimize further.

## Future Enhancements

- Implement bit-level encoding for more accurate compressed size calculations.
- Support file compression in addition to text.
- Add visualization of buffer states during compression.
- Optimize for larger datasets with dynamic buffer sizing.



