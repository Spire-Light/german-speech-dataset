# German Speech Dataset

Free sample recordings from Spirelight's off-the-shelf German speech dataset. 1,534 hours of unscripted German recorded in January and February 2026: 1,012 hours of two-person conversation, each speaker on their own channel, and 522 hours of monologue, with machine transcripts and word-level timestamps. Speakers are mostly in Germany, with Austrian and Swiss speakers too. Download access within 24 hours of a signed order.

**Full dataset, pricing and quotes:** [spirelight.ai/datasets/german](https://www.spirelight.ai/datasets/german?src=github-german)

## Listen

Short excerpts, as played on the dataset page, are in [`excerpts/`](excerpts/):

- [`excerpts/german-conversation-excerpt.mp3`](excerpts/german-conversation-excerpt.mp3)
- [`excerpts/german-monologue-excerpt.mp3`](excerpts/german-monologue-excerpt.mp3)

The complete sample recordings (FLAC, with transcripts and a `datasets` loader) are on Hugging Face: [huggingface.co/datasets/SpeechDataAI/german-speech-dataset](https://huggingface.co/datasets/SpeechDataAI/german-speech-dataset). Their uncorrected machine transcripts, as TXT and JSON with word-level timestamps, are also in [`transcripts/`](transcripts/) here.

## Full sample recordings (on Hugging Face)

5 complete recordings, 178 minutes in total. The audio is unedited and compressed losslessly to FLAC on Hugging Face; buyers receive WAV plus one file per speaker for conversations. Each recording has its uncorrected machine transcript as TXT and JSON.

| File | Type | Length | Audio |
| --- | --- | --- | --- |
| [`conversation/german-conversation-01.flac`](https://huggingface.co/datasets/SpeechDataAI/german-speech-dataset/blob/main/conversation/german-conversation-01.flac) | Conversation | 25 min | 48 kHz, 16-bit, stereo |
| [`conversation/german-conversation-02.flac`](https://huggingface.co/datasets/SpeechDataAI/german-speech-dataset/blob/main/conversation/german-conversation-02.flac) | Conversation | 55 min | 48 kHz, 16-bit, stereo |
| [`monologue/german-monologue-01.flac`](https://huggingface.co/datasets/SpeechDataAI/german-speech-dataset/blob/main/monologue/german-monologue-01.flac) | Monologue | 32 min | 48 kHz, 24-bit, mono |
| [`monologue/german-monologue-02.flac`](https://huggingface.co/datasets/SpeechDataAI/german-speech-dataset/blob/main/monologue/german-monologue-02.flac) | Monologue | 30 min | 48 kHz, 24-bit, mono |
| [`monologue/german-monologue-03.flac`](https://huggingface.co/datasets/SpeechDataAI/german-speech-dataset/blob/main/monologue/german-monologue-03.flac) | Monologue | 36 min | 48 kHz, 24-bit, mono |

On Hugging Face, each audio folder has a `metadata.csv` with the full transcript text, so the dataset viewer and `datasets` can read it directly. Word-level timestamps are in the JSON files under `transcripts/`.

```python
from datasets import load_dataset

ds = load_dataset("SpeechDataAI/german-speech-dataset", "conversation", split="train")
print(ds[0]["text"][:300])
```

## The full dataset

| Recording type | Recordings | Hours | Average length |
| --- | ---: | ---: | ---: |
| Conversation, business topics | 989 | 506.5 | 31 min |
| Conversation, open topics | 982 | 505.9 | 31 min |
| Monologue | 1,013 | 521.8 | 31 min |

| Speaker location | Hours |
| --- | ---: |
| Germany | 1,175 |
| Austria | 224 |
| Switzerland | 60 |
| Other or not stated | 75 |

Speakers' home regions include Berlin, Hamburg, Bremen, Hesse, Saxony, Bavaria, Baden-Württemberg, North Rhine-Westphalia, Rhineland-Palatinate and Schleswig-Holstein in Germany, Vienna, Styria and Carinthia in Austria, and Zürich in Switzerland.

- **Speakers:** 58 registered contributors, 48 of whom also recorded monologues. Their conversation partners were not registered, so there are more than 58 distinct voices; that number is not counted.
- **Recorded:** 2026-01-25 to 2026-02-28
- **Audio:** 48 kHz WAV. Conversations: stereo, one speaker per channel, plus one file per speaker. Monologues: mono. Bit depth is 16 or 24 depending on the recording.
- **Devices and setting:** 96% recorded on a laptop or PC and about 4% on a phone, in quiet indoor settings.
- **Transcripts:** Machine transcripts with speaker labels, segment start and end times and word-level timestamps, as TXT and JSON, for 1,533 of the 1,534 hours. Not human-reviewed.
- **Topics:** More than 2,300 distinct topic labels, from job interviews and travel agency calls to food, music, AI and philosophy.
- **Licence:** commercial use under a written licence; voice cloning is excluded.
- **Price:** $35 per audio hour for all 1,534 hours ($53,690); a part of the dataset is quoted.
- **Delivery:** download access within 24 hours of a signed order.

## Good for

- Training and evaluating German ASR (speech recognition) on unscripted speech rather than read sentences.
- Speaker diarization: in the conversations each speaker has their own channel, so turns and overlaps can be read from the channels.
- Voice agents and turn-taking research: real interruptions, backchannels and topic changes.

Not for voice cloning or imitating a speaker.

## How the samples differ from free corpora

Common Voice and FLEURS are short sentences read aloud, and MLS is audiobooks read aloud. These recordings are unscripted conversation and monologue, 31 minutes per recording on average.

## Licence for this sample

The files in this repository are free to download and use to evaluate whether the full dataset fits your project. Training on them, redistributing them and voice cloning are not permitted. See [LICENSE.md](LICENSE.md). The full dataset is licensed commercially: [request a quote or the full sample pack](https://www.spirelight.ai/datasets/german?src=github-german#request-samples).

## About

Published by SpeechData.ai, part of Spirelight (Spire Light ApS, Denmark), which records, transcribes and licenses speech data for teams building voice AI. Browse every dataset at [spirelight.ai/datasets](https://www.spirelight.ai/datasets?src=github-german).
