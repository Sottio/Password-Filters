# Password-Filters

Public offline breach filters for Ravelock.

[Download the current release](https://github.com/Sottio/Password-Filters/releases/tag/fuse8-20261030-553ef4a8).

| Dataset | Top-ranked hashes | Download size | Reported occurrence coverage | Measured false positives |
|---|---:|---:|---:|---:|
| Core | 10,000,000 | 10.88 MiB | 47.23% | 0.3748% |
| Medium | 50,000,000 | 53.75 MiB | 66.14% | 0.3917% |
| Large | 200,000,000 | 214.97 MiB | 83.52% | 0.3897% |

Ranked by HIBP occurrence count descending, then SHA-1 ascending for ties. These nested subsets replace the earlier 5% Bloom filters. The expected nonmember false-positive rate is 1/256 (about 0.39%); the measurements above use one million known nonmembers per file. Every selected source record was rechecked against the serialized output, with zero false negatives. Occurrence coverage describes the downloaded snapshot, not attack probability or customer protection. A possible match is not proof of a breach, and a negative result does not prove safety.

Download `ravelock-medium.fuse8.bin` or `ravelock-large.fuse8.bin`, then use Settings → Offline breach database → Import a downloaded database file. Core is already bundled with the updated app. Older Ravelock versions cannot read this format and must update first; the legacy Bloom downloads have been retired.

Ravelock has no INTERNET permission and uploads no password, hash or vault. Downloads happen in your browser under the browser and GitHub privacy policies. Imports are bounded and verified against metadata pinned inside the app, including SHA-256; changed or incompatible files are rejected.

Source: https://haveibeenpwned.com/Passwords, retrieved with https://github.com/HaveIBeenPwned/PwnedPasswordsDownloader.
Source SHA-256: `553EF4A84E4273A712920ECA22908FED766A08E26EF6FD215C2B9D036C96AB2C`.
Construction: https://github.com/FastFilter/xor_singleheader (pinned commit and Apache-2.0 license attached). See manifests, verification reports and SHA256SUMS.txt.
