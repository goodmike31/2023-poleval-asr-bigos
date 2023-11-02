# Polish Automatic Speech Recognition Challenge
The goal of this challenge is to benchmark open Polish ASR systems against commercial ASR services on a wide range of datasets.

## Introduction
Automatic speech recognition (ASR) has made significant progress over the last decade. Improvements in deep learning and increased data availability have resulted in accuracy levels for artificial speech transcription that are on par with human transcription, at least in specific domains, tasks, and speech characteristics. ASR technology has expanded to cover many new languages, use cases, user demographics, and devices. However, achieving robust speech recognition remains a challenge for many low-resource languages, specific speaker groups, application domains, and acoustic conditions.

## Task Description
We are introducing the Open Challenge for Polish ASR to gauge the technological advancements in Polish ASR technology. This initiative draws inspiration from the Multi-Domain End-to-End Speech Recognition Benchmark (End-to-end Speech Benchmark) for the English language [LINK](https://huggingface.co/esb). In order to promote multi-domain evaluation across a wide array of speech datasets, we have introduced a new test dataset named BIGOS (Benchmark Intended Grouping of Open Speech) [LINK](https://huggingface.co/datasets/michaljunczyk/pl-asr-bigos 
), which comprises recordings from 13 open datasets and has been manually curated to ensure dependable evaluation results.

### Dataset
#### Training data
We provide training, development and test datasets under a BIGOS corpora, which combines 13 publically available datasets.
The corpora is available on [Hugging Face](https://huggingface.co/datasets/michaljunczyk/pl-asr-bigos)

#### Test data
The test data consists of selected, perturbated recordings from test suites available in BIGOS corpora and additional recordings from other sources. All recordings in test-A and test-B datasets were manually transcribed to ensure consistent evaluation results.
Transcripton protocol is available [here](https://docs.google.com/document/d/15lMDe72_obEg6eOmz--6bVpd3v6bM3fDtSyunadwCqs/edit)

### Evaluation
In automatic evaluation, errors are automatically detected by comparing ASR outputs with manual transcriptions (references).

#### Metrics
We will calculate two measures of accuracy for each provided submission:
 - WER - the number of incorrectly transcribed words (tokens) divided by the total number of tokens in the reference sentences.
 - CER - the number of incorrectly transcribed characters divided by the total number of characters in the reference sentences.

WER will be used for scoring and ranking of provided solutions.

#### Text normalization 
Both references (human transcriptions) and hypotheses (ASR systems outputs) are normalized and post-processed to minimize the probability of false errors. All punctuation marks are removed and tokens are converted to lowercase. Numeral expressions remain in the normalized format.

#### Baselines 
3 commercial ASR systems with support for the Polish language (Google, Microsoft, Whisper) and vanilla OpenAI Whisper models (large_v2, medium, small, base, and tiny)

### Metadata
Tags: poleval-2023
