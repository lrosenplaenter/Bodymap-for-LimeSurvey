# Bodymap-for-LimeSurvey
[![DOI](https://zenodo.org/badge/1003200779.svg)](https://doi.org/10.5281/zenodo.15678321)

An interactive bodymap for LimeSurvey that allows participants to select body regions directly on an image. Handy for medical, psychological, etc (e.g. pain-mapping) surveys.

## Online Demo

Try it here:  
[https://survey.hrz.uni-giessen.de/index.php/335653?newtest=Y](https://survey.hrz.uni-giessen.de/index.php/335653?newtest=Y)

## Features

- Interactive SVG overlay on a body image
- Clickable body regions, each mapped to a checkbox answer
- Works with LimeSurvey & its Community Edition (tested with CE 6.5.17+240715)
- All source files included (SVGs, PNGs, GIMP .xcf files, HTML)

## Requirements

- LimeSurvey installation (tested with version 6.5.17+240715)
- Survey admin access to upload images and import questions

## Installation & Usage

1. **Upload the Bodymap Image**

   - Place your `bodymap.png` file in the following directory on your LimeSurvey server:
     ```
     /upload/surveys/Your_Survey_ID/images/bodymap.png
     ```
     You do **not** need to manually replace the Survey-ID in the html. A `{SID}`-placeholder is filled in automatically by LimeSurvey when rendering the question.

2. **Import the Question**

   - In the LimeSurvey admin interface, go to your survey.
   - Import the provided `limesurvey_question.lsq` file using the "Import question" feature.
   - This will add a multiple-choice (checkbox) question with the interactive bodymap.

3. **Verify Functionality**

   - Preview the question in your survey.
   - The bodymap image should appear with interactive regions.
   - Clicking a region will select/deselect the corresponding checkbox (the checkboxes themselves are hidden).

## How It Works

- The question is a standard multiple-choice (checkbox) question.
- The bodymap image is overlaid with SVG regions, each mapped to a checkbox answer.
- When a region is clicked, the corresponding checkbox is checked/unchecked via JavaScript.
- The checkboxes are hidden from view for a clean interface.

## Included Files

- `bodymap.html` – HTML/JS template for the interactive bodymap
- `limesurvey_question.lsq` – LimeSurvey question export for easy import
- `bodymap.png` – The main body image (must be uploaded as described above)
- `*.svg` – SVG files for each body region (for editing or reference)
- `*.xcf` – GIMP source files for the bodymap and overlays
- `CITATION.cff` – Citation metadata for this software
- This README

## Customization

- To use your own body image, replace `bodymap.png` and adjust SVG overlays as needed.
- Edit the SVG paths in `bodymap.html` or the included SVG files for custom regions.

## Citation

If you use this software, please cite it using the metadata in the included `CITATION.cff` file.

## License

MIT License (see `LICENSE` file for details).

---

**Disclaimer:**  
This project is not affiliated with LimeSurvey CE or LimeSurvey GmbH.
