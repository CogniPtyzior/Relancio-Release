# Changelog

## v0.9.2

Maintenance release following the initial public preview.

### Changed

* Improved desktop mail list refresh behavior.
* Incoming and sent mail lists now refresh without interrupting the currently edited draft.
* The selected draft row and editor content are preserved during background refreshes.
* Manual/automatic inbox sync, AI batch updates, and successful mobile sends can update the desktop list without prompting.
* Filters, sorting, mode changes, and manual selection changes still ask for confirmation when unsaved draft changes could be lost.
* Successful mobile sends now notify the desktop view so sent items appear sooner.
* Optimized indexes for internal DB
* Improved received/sent refreshed for item lists (with smarter logic around drafts)

* Clarify reply provenance and preserve mobile draft edits

- Separate automatic AI replies from user-edited replies
- Reset model_used on desktop/mobile save and send
- Restore DB replies with or without model_used
- Ensure mobile-saved reply content is shown on desktop reload
- Stabilize the Generate button label and spinner content
- Add coverage for DB round-trips, mobile save, and send provenance

* Clarify AI-generated reply state and preserve manual draft edits

* Simplify mail dismissal flow and improve confirmation dialogs

* Add the existing unsaved-changes confirmation flow before regenerating an AI reply.

This prevents the Generate action from replacing a user-edited draft without giving the user a chance to save, discard, or cance

### Notes

Windows x64 remains the primary supported platform.

Linux x64 is provided as an experimental build. It is less tested and may not include all Windows features.
