# AS Repository — Exercise Solutions

This repository contains complete and clearly formatted LaTeX solutions to exercises given by our teachers. The goal is to create a consistent, easy-to-read, and well-organized collection of solved problems that is accessible to all the students. This file explains how the repository is structured, how the LaTeX files work, how to compile them, and how others can contribute.

---

## 1. Purpose of This Repository

The main idea is to create a high-quality and unified collection of mathematical exercise solutions. The repository aims to:

* Keep all modules in one place,
* Use a single formatting style,
* Generate clean and professional PDFs,
* Allow work to continue over time,
* Encourage collaboration from other students or contributors.

This is not designed to be a full textbook or lecture notes, but rather a solution bank organized by module.

---

## 2. Repository Structure

The repository is organized into three main directories:

```Structure

AS-Repository/
│
├── Code/
│   ├── A Template.tex
│   ├── Module 1/
│   │   ├── Series 1.tex
│   │   ├── Series 2.tex
│   │   ├── Series 3.tex
│   │   └── ...
│   ├── Module 2/
│   │   ├── Series 1.tex
│   │   ├── Series 2.tex
│   │   ├── Series 3.tex
│   │   └── ...
│   │── Module 3/
│   │   ├── Series 1.tex
│   │   ├── Series 2.tex
│   │   ├── Series 3.tex
│   │   └── ...
│   └── .../
│       ├── Series 1.tex
│       ├── Series 2.tex
│       ├── Series 3.tex
│       ├── Series 3.tex
│       └── ...
│
├── Inputs/
│   └── global.tex
│
└── PDFs/
    ├── Module 1/
    │   ├── Series 1 - Worksheet.pdf
    │   ├── Series 1 - Solution.pdf
    │   ├── Series 2 - Worksheet.pdf
    │   ├── Series 2 - Solution.pdf
    │   └── ...
    ├── Module 2/
    │   ├── Series 1 - Worksheet.pdf
    │   ├── Series 1 - Solution.pdf
    │   ├── Series 2 - Worksheet.pdf
    │   ├── Series 2 - Solution.pdf
    │   └── ...
    ├── Module 3/
    │   ├── Series 1 - Worksheet.pdf
    │   ├── Series 1 - Solution.pdf
    │   ├── Series 2 - Worksheet.pdf
    │   ├── Series 2 - Solution.pdf
    │   └── ...
    └── ....
```

Each of the folders and sub-folders has a specific purpose.

### **Code/Module #**

This folder contains the actual LaTeX source files for every exercise list per module, with each inside their own directory. Inside, each file corresponds to a specific serie from a specific module. For example:

* `Module 1/Series 1.tex` is the solution `.tex` file of the 1st serie of module 1.
* `Module 1/Series 2.tex` is the solution `.tex` file of the 2nd serie of module 1.
* `Module 2/Series 1.tex` is the solution `.tex` file of the 1st serie of module 2.

Every `.tex` file in this folder includes shared LaTeX preambles stored in the `Inputs/` folder.

### **Inputs/**

This folder contains the shared LaTeX resources that define the project’s formatting. Currently it only includes the `global.tex` file, which is set to be the basic preamble used in every `.tex` file inside `Code/`. In general, every file should include it at the start of the document. The current preamble sets up:

* The most required LaTeX packages,
* Geometric layout,
* Header and footer appearance,
* Mathematical and typographic settings.

By centralizing all of this, every document in the repository remains consistent.

### **PDFs/**

This contains the compiled PDF output for each module, with the addition of the questions series as well. Every module can have its own folder inside `PDFs/` that stores both the questions and answers PDFs. For example:

* `PDFs/Module 1/Series 1 - Worksheet.pdf`
* `PDFs/Module 1/Series 1 - Solution.pdf`
* `PDFs/Module 1/Series 2 - Worksheet.pdf`
* `PDFs/Module 1/Series 2 - Solution.pdf`
* `PDFs/Module 2/Series 1 - Worksheet.pdf`
* `PDFs/Module 2/Series 1 - Solution.pdf`

Keeping PDFs separate prevents clutter and separates source files from output files.

---

## 3. How LaTeX Files Work in This Project

Each `.tex` file in `Code/` subfolders starts by loading the shared preambles located in `Inputs/` directory. This usually means that you do not rewrite the document class, nor the spacing rules. We have already decided on the format for most of the documents, though exceptions could occur.

A typical structure in these files is:

1. A title section
2. A sequence of exercises
3. A clear solution written under each exercise

---

## 4. Formatting Style and Conventions

The design of these documents aims to be clean, readable, and uniform across all modules. The shared preamble:

* Uses a matching footer with page numbers
* Improves text spacing
* Enhances mathematical typesetting
* Loads tools for physics notation, SI units, chemical notation, and TikZ support if needed

---

## 5. How to Compile the PDFs

To compile any module, open a terminal, move into your required subfolder inside the `Code/` directory, and run:

```
latexmk -pdf filename.tex
```

---

## 6. How to Contribute

Anyone is welcome to contribute new solutions or improvements.
To keep the repository clean and consistent, please follow these guidelines:

1. Add or modify `.tex` files inside their respective `Code` subfolders.
2. Always load the shared preamble using `\include{../../Inputs/global.tex}`.
3. Follow the same environment structure given in our template.
4. Ensure your LaTeX compiles without errors.
5. Place the compiled PDF in the appropriate subfolder under `PDFs/`.
6. In a pull request, describe clearly what you added or corrected.

If you create new commands or macros, you may add them to `Inputs` so that all modules can access them when required.

---

## 7. Possible Future Improvements

This project is designed to expand gradually. Possible additions include:

* A `macros.tex` file for extra custom commands,
* A Makefile or latexmk automation file,
* GitHub Actions for automatic PDF builds,
* Module index pages,
* Diagrams or visual explanations for selected solutions.

As the repository grows, these can help maintain clarity and structure.

---

## 8. Summary

This repository:

* Stores mathematical exercise solutions,
* Keeps everything neatly organized,
* Uses a single shared LaTeX preamble for consistency,
* Separates source files from outputs,
* Encourages clean contributions,
* Produces professional PDF documents.

The structure is simple, predictable, and easy to work with, making this repository suitable for long-term use and collaboration.
