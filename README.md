# Password-Filters

Public, offline breach-database filters for Ravelock, derived from [Have I Been Pwned Pwned Passwords](https://haveibeenpwned.com/Passwords) using the [official downloader](https://github.com/HaveIBeenPwned/PwnedPasswordsDownloader). No plaintext passwords are published here.

## Snapshot: 2026-10-30

The downloaded source contains **2,068,408,781 unique SHA-1 hashes** and **57,002,655,265 reported occurrences**. Hashes are ranked by occurrence count; ties are resolved by hash order.

| Dataset | Unique hashes selected | Share of unique source hashes | Share of reported occurrences | File size | Estimated false positives |
| --- | ---: | ---: | ---: | ---: | ---: |
| Core (bundled with Ravelock) | 48,341,725 | 2.34% | 65.7% | 36 MiB | 5% |
| Medium (optional) | 206,840,879 | 10% | 83.9% | 154 MiB | 5% |
| Large (optional) | 620,522,635 | 30% | 94.0% | 462 MiB | 5% |

Download **ravelock-medium.bin** or **ravelock-large.bin** from [Releases](https://github.com/Sottio/Password-Filters/releases), then import it using Ravelock’s file picker. The app itself has no INTERNET permission. Optional files are release assets, not Git source files.

All three filters are frequency-ranked subsets, not the entire corpus. The reported-occurrence percentages describe this source snapshot, not the proportion of people or future breaches protected. A negative result does not establish that a password has never been breached. A Bloom match means possibly present; approximately 5% of nonmembers may match. Ravelock rejects matching generated candidates and tries again.

Every selected hash was checked against its completed filter: zero selected-member misses. Source provenance, parameters and SHA-256 checksums are provided in each release. Ravelock pins the expected fingerprint and rejects modified or incompatible imports; a new snapshot requires compatible app metadata.

Source SHA-256: `553EF4A84E4273A712920ECA22908FED766A08E26EF6FD215C2B9D036C96AB2C`. The occurrence count attached to each hash is used only for selection; individual counts cannot be recovered from these filters.
