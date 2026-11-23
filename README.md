# smc-social-media-drop

Pass-through image host for Sun Motor Cars Automotive Group scheduled social posts. Metricool takes images by public URL only, so finished cards land here and posts point at their raw URLs.

## Layout

```
STORE/SERIES/YYYY-MM/<same filename as the OneDrive FINALS file>
```

Example: `MB/OWNER-REVIEWS/2026-11/11.26_MB_REVIEWS_P1-SCOTT_1-REVIEW.jpg`

One repo for all stores and series. Split only if access, visibility or automation ever differs.

## Image URL pattern

```
https://raw.githubusercontent.com/WestillSMC/smc-social-media-drop/main/<path>
```

## Rules

- Finished cards and the photo log only. Raw library photos never go in (they stay in OneDrive LIBRARY).
- Never delete or rename a file. Scheduled posts may fetch the image at publish time.
- Only the pipeline pushes. Vendors work in shared OneDrive folders and Metricool, never in GitHub.
- Source of truth for files is OneDrive SMC_MRKTNG2.0. This repo mirrors finals for hosting.

## PHOTO_LOG.csv

Source of truth for photo usage (repeat checks). One row per use of a cleared library photo.

| Column | Meaning |
|---|---|
| photo_id | Cleared photo ID, format MB-SVC-014 |
| store | MB, BMW, AUDI, COLLISION |
| category | Photo category (service bay, showroom, exterior, etc.) |
| text_zone | Open area where card text sits |
| library_path | Path under 02_ASSETS/LIBRARY/<STORE>_CLEARED |
| post_date | Publish date, YYYY-MM-DD |
| series | Series tag, e.g. OWNER-REVIEWS |
| post_slug | Post identifier, e.g. P1-SCOTT |
| asset | Asset filename in this repo |
