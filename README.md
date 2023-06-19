# ncaanext.com website

Production domain: [www.ncaanext.com](https://www.ncaanext.com)

As a non-commercial, free and open-source project, NCAA NEXT uses Google Blogger for its free website CMS and hosting. The site design is based on the "VibeBlog" theme by TemplatesYard.

## Theme customization documentation

- [Theme Demo](https://vibeblog-templatesyard.blogspot.com)
- [Setup Guide](https://www.sorabloggingtips.com/2023/01/how-to-setup-vibeblog-blogger-template.html)

## Development and Theme Edits

*IMPORTANT: Be sure to **make a backup** of the current theme XML before making any edits to the XML code (Theme > Customize: Backup).*

*ALSO: **Changes to widgets in the Blogger GUI will write to the XML!** So, if you change anything in the Layout, Widgets, Settings or anywhere in the Blogger GUI, and you want to work on the code locally, be sure to copy and paste the XML code from Blogger to your local file because the edits you did in the GUI probably changed the XML code.*

Unfortunately, to my knowledge, there is no easy way to setup a local development environment for Blogger. You can edit the XML locally, but you will need to copy the XML code to the Blogger site each time you want to see the affect of your code changes. You can choose between uploading the XML file (Theme > Customize: Restore) or pasting in the XML code (Theme > Customize: Edit HTML). 

Alternatively, if you prefer editing directly in the Blogger Edit HTML view, you can do that instead of editing locally, and copy the code to your local file for git commits. Either way, be sure to make a backup of the current theme XML before starting your round of development (Theme > Customize: Backup). 

After testing the new code thoroughly on the staging site, if there are no issues and you are ready to deploy it to the live site, push your commits to Github, and then go to Theme > Customize: Restore in the NCAA NEXT production Blogger site. Paste in your XML, but first – especially on the live production site – be sure to make a backup of the theme! Although we are tracking changes in Github and can restore previous versions of the code that way, a backup of the XML from Blogger is quicker to restore and only takes a couple of seconds to do.

## Editing and Posts

### Thumbnails

The post thumbnail should be a specific size and aspect ratio. You can find a PSD template for this in [assets > templates](https://github.com/j26w/nccanext-website/tree/main/assets/templates). The template is compatible with Photopea.com.

The image you create must be somewhere in the post body. It needs to be the first image used in the post to be the thumbnail. So, if it is the only image, you can put it at the end of the post.

In the template, there is a layer group called "CORNER BADGES". You can enable one of these (or create a new one) to help identify the type of post it is. Consistent use of these badges for hot fixes, guides, version upgrades, etc., will help the reader to more quickly discern what type of content the post contains, improving the user experience.

### Buttons

You can enable button styling in your post links if you edit the html to add the "next-button" class to the anchor element. Example:

Change `<a href=""></a>`

to `<a class="next-button" href=""></a>`
