# course-ci
A GitHub action that automates parts of the development of LibreLingo courses

## Usage

In order to enable automated checks in your course repository, you have to create a `.github`
folder in your repository, if it does not exist yet. Make sure there is a `workflows` folder
in this `.github` folder.

Then create the `.github/workflows/main.yml` file. The contents of this file should be:

```yaml
on: [push]

jobs:
  verify-course:
    runs-on: ubuntu-latest
    name: Verify course
    steps:
      - uses: actions/checkout@v2
      - uses: LibreLingo/course-ci@main
```

