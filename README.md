# Polish Automatic Speech Recognition Challenge
The goal of this challenge is to benchmark open Polish ASR systems against commercial ASR services on a wide range of datasets.

## Introduction
Automatic speech recognition (ASR) has made significant progress over the last decade. Improvements in deep learning and increased data availability have resulted in accuracy levels for artificial speech transcription that are on par with human transcription, at least in specific domains, tasks, and speech characteristics. ASR technology has expanded to cover many new languages, use cases, user demographics, and devices. However, achieving robust speech recognition remains a challenge for many low-resource languages, specific speaker groups, application domains, and acoustic conditions.

## Task Description
We are introducing the Open Challenge for Polish ASR to gauge the technological advancements in Polish ASR technology. This initiative draws inspiration from the Multi-Domain End-to-End Speech Recognition Benchmark (End-to-end Speech Benchmark) for the English language [1]. In order to promote multi-domain evaluation across a wide array of speech datasets, we have introduced a new test dataset named BIGOS (Benchmark Intended Grouping of Open Speech) [2], which comprises recordings from 13 open datasets and has been manually curated to ensure dependable evaluation results.

### Dataset
#### Training data
We provide training, development and test datasets under a BIGOS corpora, which combines 13 publically available datasets.
The corpora is available on hugging face: https://huggingface.co/datasets/michaljunczyk/pl-asr-bigos 

#### Test data
The test data consists of selected recordings from test suites available in BIGOS and on-purpose collected recordings.
All recordings in test data available in test-A and test-B were manually transcribed to ensure consistent evalauation results.

### Evaluation
We will calculate three measures of accuracy for each provided submission:
 - SER - the accuracy of provided expanded forms of abbreviations (case insensitive string match),
 - WER - the accuracy of provided base forms of abbreviations (case insensitive string match).
 - CER - 

Based on these measures, the final score will be calculated using a weighted average:
Acc = 0.1\*SER + 0.5\*WER + 0.4\*CER

### Metadata
Tags: poleval-2023
