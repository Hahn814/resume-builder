# Resume Builder

This project is designed to work in a Visual Studio Code devcontainer environment. The devcontainer provides a pre-configured Linux environment with all necessary tools (Pandoc, LaTeX, etc.) for building and previewing your resume.

You can open this project in VS Code and use the built-in Markdown and PDF preview extensions to view your resume as you edit. The environment ensures
consistent builds and easy setup for anyone cloning the repository.

## Devcontainer Prerequisites

To use this project in a VS Code devcontainer, you need:

- **Visual Studio Code** (latest recommended)
- **Remote - Containers extension** (or Dev Containers extension)
- **Docker** installed and running on your host system

When you open the project in VS Code, it will prompt you to reopen in the devcontainer. The devcontainer automatically installs all required tools (Pandoc, LaTeX, etc.) and configures the environment for resume editing and PDF generation.

## How to Update Your Resume

1. **Edit your resume:**
   - Update `resume.md` with your latest experience, skills, and education.
   - Use standard markdown formatting. For section breaks, you can use LaTeX commands like `\noindent\rule{\linewidth}{0.4pt}` for professional line separators.
   - For colored dates, use: `\datecolor{Sep 2016 -- Present}` (no backticks).

2. **Edit the template (optional):**
   - Update `resume-template.tex` to change colors, fonts, or layout.

## How to Generate the PDF

1. **Generate the PDF:**
   - Run the following command in the project directory:

     ```bash
     pandoc resume.md -o resume.pdf --template=resume-template.tex --pdf-engine=xelatex
     ```

   - The output will be `resume.pdf`.

## Tips

- Preview the PDF after each change to ensure formatting is correct.
- For advanced styling, edit `resume-template.tex` and use raw LaTeX in `resume.md` as needed.
- If you encounter errors, check that all LaTeX commands used in the markdown are defined in the template.

---

## Roadmap

- **More Templates:**
  - Add a variety of LaTeX and Markdown templates for different resume styles and industries.
  - Enable easy switching between templates for personalized PDF output.

- **Streamlined PDF Generation:**
  - Integrate VS Code tasks to automate Pandoc commands for building the PDF.
  - Provide one-click or shortcut-based PDF generation directly from the editor.
  - Document and maintain these tasks for ease of use and onboarding.

- **Copilot Resume Suggestions:**
  - Integrate GitHub Copilot to provide AI-powered suggestions for resume improvements directly in VS Code.
  - Offer actionable feedback and keyword optimization for better ATS and recruiter visibility.

**Contact:** For questions or improvements, reach out via GitHub.
