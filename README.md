# SPIRAL Dataset

[![arXiv](https://img.shields.io/badge/arXiv-2412.12009-b31b1b.svg)](https://arxiv.org/pdf/2412.12009)

SPIRAL (Speech Information Retrieval And Lookup) is a dataset designed to test speech language models' ability to process long spoken inputs.

## Dataset Description

SPIRAL consists of spoken lectures and conversations with corresponding transcripts, questions, and metadata. The dataset is specifically crafted to evaluate models' comprehension and information retrieval capabilities from extended audio content.

## Download

The wavs can be downloaded from this [url](https://duke.box.com/v/spiral-dataset).

## Dataset Structure

```
spiral/
├── wavs/           # Directory containing main audio files
├── data.jsonl      # Main dataset annotations
└── data_h.jsonl    # Hard subset of the dataset
```

## Data Format

Each entry in the JSONL files contains:

### Transcript

- Speaker-attributed text segments
- Multiple utterances per speaker
- Includes speech disfluencies (e.g., "uh")

### Test Questions

- Question text
- Multiple choice options (A-D)
- Correct answer

### Metadata

- Main topic
- Subtopic
- Transcript type
- Unique identifier

### Audio Data

- References to audio files
- Key sentence timestamps
- Speaker prompts used
- Audio file paths

## Example Entry

Each entry contains structured information about:

- Complete transcript with speaker attribution
- A key sentence selected from the transcript
- A test question related to the content
- Topic metadata
- Audio file references and paths

## Usage

This dataset can be used for:

- Training and evaluating Speech LLMs in the context of long-form audio
- Testing information retrieval from long-form audio
- Evaluating question-answering capabilities

## Citation

If you use this dataset, please cite it as follows:

```
@inproceedings{lin2025speechprune,
  title     = {SpeechPrune: Context-aware Token Pruning for Speech Information Retrieval},
  author    = {Lin, Yueqian and Fu, Yuzhe and Zhang, Jingyang and Liu, Yudong and Zhang, Jianyi and Sun, Jingwei and Li, Hai and Chen, Yiran},
  booktitle = {2025 IEEE International Conference on Multimedia and Expo (ICME)},
  year      = {2025}
}
```
