# CRAB-template

## Structure

`.github/workflows/` (folders, contain GitHub Actions workflow file)

`jspsych/` (folder, contains CRAB and jsPsych code and css)

`index.html` (contains your CRAB instantiation)

## Setup
1. use this template - if hosting on GitHub Pages, put it in a repository and call it `<yourUsername>.github.io`.
2. modify `index.html` - add your dataset etc. Refer to the comments in the file and the [documentation](https://github.com/smhancode/jsPsych.git/tree/main/packages/plugin-crab/docs/crab-docs.md).
3. create repository-scoped access token with these permissions: read access to repository metadata, and read and write access to GitHub Actions.

## Example

```javascript
const trial = {
  type: jsPsychCrab,
  stylesheet: "../src/crab.css",
  dataset: [
    {"id": 0, "text": "This is a demo of CRAB.\n\nIMPORTANT: saving to GitHub will not work as no repository has been specified (and you do not have a corresponding access token)."},
    {"id": 1, "text": "This demo of CRAB is in single-label mode. Rapid mode is available. It is not available in multi-label mode."},
    {"id": 2, "text": "This item already came with a label assigned.", "label": 0},
    {"id": 3, "text": "Lorem ipsum dolor sit amet, consectetuer adipiscing elit."},
    {"id": 4, "text": "Aenean commodo ligula eget dolor. Aenean massa."},
    {"id": 5, "text": "Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus."},
    {"id": 6, "text": "Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim."},
    {"id": 7, "text": "Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu. In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo."},
    {"id": 8, "text": "Nullam dictum felis eu pede mollis pretium."},
    {"id": 9, "text": "Integer tincidunt."},
    {"id": 10, "text": "Cras dapibus."},
    {"id": 10, "text": "Vivamus elementum semper nisi."},
  ],
  labels: ["not ironic", "ironic"],
  guidelines: "Please read and adhere to these guidelines:<ol><li>They can be styled with HTML.</li><li>Aenean vulputate eleifend tellus.</li><li>Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim.</li></ol>",
  owner: "theOwner",
  repo: "theRepo",
};
```
