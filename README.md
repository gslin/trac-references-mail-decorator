# trac-references-mail-decorator

This single file plugin for Trac will add header's `Message-ID` field to `References` field.

## Background

Amazon SES will change header's `Message-ID` to its own format, which causes mail clients unable to identify the first mail and other followings are in the same thread.  (Mails from second mail have `References` field.)

This plugin is a workaround plugin.  It will copy `Message-ID` to `References` if no `References` field existed, which rebuild relationship between first mail and other followings.

## Install

* This plugin is a single file plugin, so you'll need to copy `ReferencesEmailDecorator.py` into Trac's `plugins/` directory.
* Restart Trac process.
* Enable it in admin interface's plugin section.

## License

See [LICENSE](LICENSE) file.
