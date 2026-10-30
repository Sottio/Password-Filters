# Password-Filters

Public offline breach-database filters for Ravelock, provided by Sottio Studio.

Download prepared binary files from Releases. Large database files are release assets, not Git source files. Each release records its source snapshot, coverage, size, estimated false-positive rate, and SHA-256 checksum.

The source is Have I Been Pwned Pwned Passwords, retrieved with its official downloader: https://github.com/HaveIBeenPwned/PwnedPasswordsDownloader

The compact filter represents the most commonly breached passwords selected by reported occurrence counts. The optional expanded filter represents every hash in its downloaded source snapshot. Neither covers breaches absent from that snapshot. Bloom matches are probabilistic; a possible match is rejected conservatively.

Ravelock checks passwords locally. Browser downloads do not upload passwords, password hashes, or vault contents from Ravelock. GitHub handles download requests under its own privacy practices.

Use only the database matching your app version. Ravelock verifies imported files against a fingerprint shipped in the app. Do not upload vault files or personal credentials to this repository.
