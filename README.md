# CrawlBrief 0.2.1-pilot

[日本語の使い方](はじめに-日本語.md) · [Download the free pilot](https://github.com/TTTBtools/crawlbrief-pilot-downloads/releases/tag/v0.2.1-pilot) · [Free-pilot permission](PILOT-PERMISSION.txt)

Turn an existing crawl CSV into a reviewed client report, on your own computer.

This is an early, AI-assisted pilot for people who already use crawl exports in client work. The pilot is free. No account, installation or AI API key is needed to run the single HTML app.

## Patch in 0.2.1

HTML-only checks now require the actual HTML media type. A different media type that merely contains the text `text/html` is no longer treated as HTML, including during previous-export comparison. This patch passed 50 automated checks; real-user acceptance and broad export compatibility are still unverified. The free-pilot conditions are unchanged.

## Start with the fictional sample

1. Download the authorized pilot ZIP from the release assets and extract it.
2. Open `dist/CrawlBrief.html` in a modern desktop browser.
3. Choose **Try sample data**. Expect 5 URLs and 3 findings.
4. Choose the findings to include, add notes and check the summary.
5. Confirm your review, then download the HTML report or action CSV.
6. To create a PDF, open your saved report and print to PDF. Turn off browser headers and footers if you do not want local file paths printed.

The summary is written by you. Selecting or excluding findings does not rewrite it.

## Supported input

English, UTF-8, comma-separated CSVs, up to 5 MB and 5,000 URL rows. Required columns: `Address` and `Status Code`. Optional columns: `Content Type` or `Content`, `Title 1`, `Meta Description 1`, `H1-1`, `Indexability Status`. Do not include both `Content` and `Content Type`.

The target workflow is Screaming Frog **Internal → All → Export**, but compatibility with unmodified real exports is still being tested. Missing columns disable their checks and are disclosed in the report. XLSX and localized headers are not supported.

## What it does

- Highlights seven supported observations: HTTP errors, missing responses, redirects, noindex and missing HTML title, description or first H1.
- Lets you select findings and add your own notes and summary.
- Compares exact URLs between two files; missing pages are not marked fixed.
- Downloads a report HTML and a selected action CSV with a simplified client name in the filename.

It does not crawl websites or verify live repairs. It is not a complete SEO audit, a security assessment, an accessibility certification or a ranking forecast.

## Data and limitations

The app contains no built-in upload, AI API request or analytics. Your browser and extensions are outside its control. Work is not automatically saved. Reports retain URLs and query strings; review them before sharing. The examples use fictional `.example` addresses.

Automated tests and earlier sample checks do not prove that all real data or browser combinations work. The 0.2.1 pilot interface still needs real-user acceptance. It was built with AI assistance; no independent customer results or verified time-saving claims are available yet.

## Feedback

Try the fictional sample first, then a non-sensitive export on your own computer. Tell us your browser, export tool/version, whether you could finish, and the exact error wording if any. Do not upload client data, credentials or confidential screenshots to a public issue.

[Share pilot feedback](https://github.com/TTTBtools/crawlbrief-pilot-downloads/issues/new?template=pilot-feedback.yml) using the short form, or [report another issue](https://github.com/TTTBtools/crawlbrief-pilot-downloads/issues). GitHub sign-in is required to submit feedback; it is not required to run the app. Your answers will be public. Do not post confidential files.

## Free pilot

The [free-pilot permission](PILOT-PERMISSION.txt) accompanies the authorized download. There is no purchase obligation or automatic charge. A future US$19 one-time price is only a proposal. No subscription, lifetime updates or response-time commitment is included.

CrawlBrief is independent software and is not affiliated with or endorsed by Screaming Frog. The name is a working product name; do not infer trademark registration from this page.
