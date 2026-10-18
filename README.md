# MediaPager.App.EmailTemplates

Built-in MediaPager email templates. This component is included as the
`MediaPager.App.EmailTemplates` submodule of the Official superproject. Community plugins
package and own any plugin-specific notification templates separately.

Templates live in `templates/<template-id>/` as plain-text Blade-style views:

- `subject.blade` renders the subject.
- `text.blade` renders the plain-text body.
- `html.blade` renders the HTML body.

These are template assets, not PHP source files. Use Blade-style expressions and view data,
for example `{{ $email }}`, `{{ $actionUrl }}`, and `{{ $logoUrl }}`. Escaped echo
(`{{ ... }}`) should be used for values, especially in HTML views, so interpolated content
is HTML-encoded. A consumer supplies the view data and renders each of the three views for
the selected built-in template ID.

Built-in template IDs are `invitation`, `password-reset`, and `email-change-verification`.
Plugin-specific notification templates are packaged by their owning plugin.

The intended GitHub repository is `MediaPager/MediaPager.App.EmailTemplates`. Repository
commits should use the local repository identity `No Bugs Given <nobugsgiven@gmail.com>`.
