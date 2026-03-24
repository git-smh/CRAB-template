# CRAB-template

## Structure

`.github/workflows/` (folders, contain GitHub Actions workflow file)
`jspsych/` (folder, contains CRAB and jsPsych code and css)
`index.html` (contains your CRAB instantiation)

## Setup
1. use this template - if hosting on GitHub Pages, put it in a repository and call it `<yourUsername>.github.io`
2. modify `index.html` - add your dataset etc.

| Parameter          | Type                  | Default Value        | Description                                                                                                              |
|--------------------|-----------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------|
| stylesheet         | string                | "jspsych/crab.css"   | stylesheet for styling the GUI. Use default stylesheet, modify it, or provide your own stylesheet.                       |
| dataset            | array of JSON objects | undefined            | the dataset to annotate, which can already have labels, e.g. `[{"id": 0, "text": "text 0", "label": 0}]`.                |
| labels             | array of strings      | undefined            | The labels to label the dataset with, e.g. `["label0", "label1"]`.                                                       |
| multi_labels       | boolean               | false                | Whether data can be annotated with multiple labels.                                                                      |
| guidelines         | HTML string           | "No guidelines."     | Annotation guidelines for annotators.                                                                                    |
| keyboard_shortcuts | JSON object           | see below            | Keyboard shortcuts.                                                                                                      |
| owner              | string                | undefined            | Username of the GitHub account which owns the repository.                                                                |
| repo               | string                | undefined            | Name of the GitHub repository to save annotations to.                                                                    |
| workflow           | string                | save-annotations.yml | Name of the GitHub Actions file, which does the saving to GitHub. Use default file, modify it, or provide your own file. |

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
