# Ao3-Export

This is just some quality of life stuff I'm sharing for Scrivener → Ao3 exports. The idea is to write in Scrivener, and then use the built-in compile function to export Ao3-friendly HTML. The compilation template exports text with the CSS classes defined in `workskin.css`.

As a note, I exclusively use the Windows version of Scrivener (version 3.1.5.1). I don't know if this works with the Mac/iOS versions.

### Preview

Example exported text (as it would appear on Ao3 with the "reversi" site skin): https://respheal.github.io/Scrivener-Ao3-Export/

## Notes

- Not all CSS style wizardry works in Scrivener, particularly the text gradient styles used in the workskin. They will be output in the compiled .txt document, even though they're not visibly formatted in Scrivener.
- Always check the compiled HTML! Save your work as a draft in Ao3 to preview before publishing!
- The styling for this workskin and template is relatively specific to my fandoms, so feel free to adjust as you please. The post linked in [Credits](#credits) is very good for explaining how to create/modify Scrivener compilation formats.
- The option to wrap italicized text in `<em>` tags only works on italic text without character styles (i.e. not using any of the colored text options). I've added additional styles that are both colored _and_ italicized, labeled as "Internal [Color]". For other styled text that should also be italicized, you'll need to check the export manually.

## How to Use

2. In Scrivener:
   1. Open the menu to create a new project, which should bring up the Project Templates (Ctrl+Shift+N).
   2. In the Project Templates window, click the "Options" dropdown and then "Import Templates..."
   3. Import [Ao3.scrivtemplate](Ao3.scrivtemplate) as a project template.
   4. Create a new project with that template. It will automatically generate all the styles required for the export, as well as a couple example folders/text files.
   5. In the "Compile For:" box at the top, switch to "Plain Text (.txt)". The Ao3 Project Format should be listed in the txt formats.
   6. As a test, hit "Compile" and choose where to save the output text file. It should generate a .txt file in the chosen location with CSS classes based on the body styles (Example file: [exported_text.txt](exported_text.txt))
3. On Ao3:
   1. Import [workskin.css](workskin.css) into a new workskin on Ao3: https://archiveofourown.org/faq/tutorial-creating-a-work-skin?language_id=en
   2. Apply the workskin to the chosen work: https://archiveofourown.org/faq/tutorial-creating-a-work-skin?language_id=en#wksknapply
   3. Import the contents of the compiled .txt from step 9 into the **HTML** text editor for a new chapter/work.
   4. Save your work as a draft to make sure everything looks right. This will also apply Ao3's HTML sanitization process, which may gently apply extra `<p>` tags where needed, etc.

## Credits

The foundational information for this comes from this post by @sineala: https://sineala.tumblr.com/post/172161779944/scrivener-3-and-ao3-a-workflow

## Note for me

I tried switching the colors to OKLCH colors, but Ao3 is currently not compatible. For future reference, the values I picked here:
Lightness/Chroma: 0.64 / 0.18
Red: 27
Green: 142
Blue: 251
Vio: 300
