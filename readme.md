# Project 2: The Unofficial Guide — Testing

## Project Overview

This project evaluates a document-based question-answering system using the supplied campus-life documents. The goal is to test retrieval, source attribution, relevance filtering, and answer accuracy, then make one improvement based on the results.

My Project 1 submission contained only a README. I have since prepared the application files, five test questions, and five acceptance criteria. The full evaluation remains incomplete.

## Run Log — Before

The following targets were written during the preparation of the missing baseline, before the full evaluation.

| Criterion | Target | Run 1 | Run 2 | Run 3 | Verdict |
|---|---|---|---|---|---|
| Retrieved information contains the complete answer | 4 of 5 | Not run | Not run | Not run | Pending |
| Generated answers name a retrieved source | 5 of 5 | Not run | Not run | Not run | Pending |
| Relevance gate rejects questions outside the corpus | 4 of 5 | Not run | Not run | Not run | Pending |
| Each expected source document remains complete in one chunk | 5 of 5 | Not run | Not run | Not run | Pending |
| Generated answers include every required fact without contradictions | 4 of 5 | Not run | Not run | Not run | Pending |

### Preliminary Check

An offline check ran `ingest.py::load_documents` and
`chunker.py::split_documents` with a minimal configuration substitute.

The check produced this output:

    88 documents, 27,908 characters, ~317 characters per document
    88 chunks, 317 characters on average (shortest 178, longest 549), produced by chunker.py::split_documents
    All five expected source documents remain complete in single chunks.

The output is saved in `local-chunk-check.txt`. This verifies document loading and chunk preservation only. It does not replace the required retrieval and generation evaluations.

## Verdicts

Final verdicts are pending because the three evaluation passes have not been completed. The preliminary check confirmed that the five expected source documents remain intact, but it did not measure the other criteria.

## Diagnoses

Required dependencies could not be installed in the preparation environment, so the full pipeline was not tested there.

No retrieval or generation failures have been diagnosed yet. After testing, I would compare incorrect answers with their retrieved chunks to determine whether the necessary evidence was missing or whether generation failed to use available evidence correctly.

## The Improvement

No measured Project 2 improvement has been completed.

While preparing the missing baseline, I changed the chunking function to preserve each short campus-life post as one chunk. This keeps related information, such as prices and exceptions, together.

This was baseline preparation. The required Project 2 improvement still needs to be chosen from an observed failure.

### Run Log — After

The after-evaluation has not been run. It requires a completed baseline evaluation and one change connected to a diagnosis.

### Did It Help?

The preliminary check confirmed that the expected source posts remain complete. The effect on retrieval accuracy and generated answers has not been measured.

## What's Still Broken

The full application still needs to be verified with its dependencies and Gemini configuration. I also need to calibrate the relevance cutoff, complete both evaluations, assign verdicts, and diagnose any missed criteria.

Setup difficulties and the submission deadline prevented me from completing these steps.

## What I'd Do Differently

I would get the application running before the first deadline and commit the criteria before testing. I would also check answers against complete factual answer keys, since a keyword match can hide missing or incorrect details.

## How I Used AI

I used ChatGPT to review the starter files, prepare questions and criteria from the supplied documents, and implement a strategy that preserves complete short posts.

ChatGPT performed the preliminary document and chunk checks and helped organize this report. The full AI evaluations were not performed, so this submission contains no measured before-and-after comparison.
