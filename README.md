# UpToDate Expert AI · Use Cases by Specialty

English-language version of the [Korean site](https://icannotcodejusthci.github.io/EAI-Prompts/), preserving its layout, features, 19 specialties, 71 cases, and 119 questions.

The case data is maintained in `cases.json`. Cases and specialties can be added or deleted through the page's admin panel. Prompt sharing and feedback use email drafts opened through `mailto:` links.

## Deployment

1. Upload `index.html`, `cases.json`, `logo.png`, `favicon.png`, `favicon.svg`, and `README.md` to the `EAI-Prompts-Eng` repository.
2. In **Settings → Pages**, select **Deploy from a branch**, **main**, and **/ (root)**, then save.
3. The page is published at https://icannotcodejusthci.github.io/EAI-Prompts-Eng/ after the deployment finishes.

If the default branch is not `main`, or if a custom domain is used, update `owner`, `repo`, and `branch` in the `CONFIG` object in `index.html`.

## Admin panel

1. Click **Admin** at the bottom of the page.
2. Enter a GitHub fine-grained personal access token scoped to this repository, with **Contents → Read and write** permission.
3. Add cases or specialties, or remove cases, then click **Save (Commit)** to commit the changes to `cases.json`.
4. The token is not stored and is cleared when the panel closes. Do not share it.

You can also edit `cases.json` directly on GitHub. Its structure is:

```json
{
  "specialties": [{ "id": "em", "name": "Emergency Medicine" }],
  "cases": [
    {
      "specialtyId": "em",
      "title": "Example case title",
      "vignette": "Case description",
      "questions": [
        { "label": "Question", "text": "Question text" },
        { "label": "Follow-up Question", "text": "Follow-up question text" }
      ]
    }
  ]
}
```

## Prompt sharing and feedback

- **Share a Prompt** and **Send Feedback** open a prefilled email draft in the visitor's default email app. They do not send email automatically.
- The recipient is `jiseong.kim@wolterskluwer.com`, configured through `CONTACT_MAIL` in `index.html`.
- The email address can also be copied if no email app is configured.
- Shared prompts can be reviewed and added to the case list through the admin panel.

## Notes

- The email template asks contributors to exclude patient-identifying information. Check incoming messages for any such information before incorporating their content.
- This is a separate English edition. Its admin panel targets `EAI-Prompts-Eng`; it does not change the original Korean repository.
- The clinical cases and questions are translated examples. Existing clinical premises, including any deliberately incorrect or inconsistent premises in the original, are preserved rather than silently revised.
