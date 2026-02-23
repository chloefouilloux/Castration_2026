Hello! Welcome to the wonderful world of copepods.
Below is our readme for Fouilloux et al. 2026: ****From exposure to infection: divergent fitness consequences of parasite encounters in a trophically-transmitted system****
The paper is about the outcomes of parasite interactions between a two genotypes of trophically-transmitted tapeworm (Schistocephalus solidus) and its first intermediate host, the cyclopoid copepod!

| Variable                       | Type                  | Unit       | Definition                                                                                          |
| ------------------------------ | --------------------- | ---------- | --------------------------------------------------------------------------------------------------- |
| `ID`                           | categorical           | —          | Unique identifier of experimental female                                                            |
| `Temporary_ID`                 | categorical           | —          | Shorthand identifier of experimental female                                                         |
| `Stock`                        | categorical           | —          | Stock flask population from which female was drawn                                                  |
| `Infection_Status`             | categorical (3-level) | —          | Experimental infection status: Unexposed, Exposed, or Infected                                      |
| `Date_Iso`                     | date                  | YYYY-MM-DD | Date female was isolated from stock population                                                      |
| `Clutch_Num`                   | numeric               | count      | Sequential clutch number since isolation. Clutch present at isolation is coded as 1                 |
| `Death_Date`                   | date                  | YYYY-MM-DD | Date female died                                                                                    |
| `Date_Gravid`                  | date                  | YYYY-MM-DD | Date female was gravid with clutch                                                                  |
| `Date_Drop`                    | date                  | YYYY-MM-DD | Date nauplii hatched from clutch                                                                    |
| `Clutch_Est_R`                 | numeric               | eggs       | Estimated number of eggs in right clutch                                                            |
| `Clutch_Est_L`                 | numeric               | eggs       | Estimated number of eggs in left clutch                                                             |
| `Inf_Intensity`                | numeric               | count      | Number of tapeworms detected in female at dissection post-death                                     |
| `Strain`                       | categorical           | —          | Parasite strain used for exposure or infection. MER = Merrill Lake (local), KJER = Norway (foreign) |
| `Clutch_Total`                 | numeric               | eggs       | Total eggs across left and right clutches (`Clutch_Est_L + Clutch_Est_R`)                           |
| `Holding_Time`                 | numeric               | days       | Number of days between gravid date and hatch date (`Date_Drop − Date_Gravid`)                       |
| `Next_Date_Gravid`             | date                  | YYYY-MM-DD | Date female became gravid with subsequent clutch                                                    |
| `Time_Between_Clutches`        | numeric               | days       | Number of days between successive clutches                                                          |
| `age_post_iso`                 | numeric               | days       | Female lifespan after isolation (`Death_Date − Date_Iso`)                                           |
| `Maximum_Dens`                 | numeric               | count      | Number of nauplii present 24 hours post-hatch                                                       |
| `DOB`                          | date                  | YYYY-MM-DD | Date of birth of nauplii                                                                            |
| `prp_survival`                 | numeric               | proportion | Proportion of eggs that survived to nauplii (`Maximum_Dens / Clutch_Total`)                         |
| `Treatment_Fine`               | categorical           | —          | Experimental treatment including parasite identity for exposed individuals                          |
| `is_post`                      | categorical           | —          | Indicator variable specifying clutches occurring after isolation clutch (used to exclude clutch 1)  |
| `Clutch_tot_post`              | numeric               | eggs       | Total eggs excluding first clutch                                                                   |
| `Maximum_Dens_post`            | numeric               | count      | Number of nauplii hatched excluding first clutch                                                    |
| `prp_survival_post`            | numeric               | proportion | Survival proportion excluding first clutch                                                          |
| `PostTreat_Eggs_Ind`           | numeric               | eggs       | Total eggs produced per female after isolation clutch (individual-level sum)                        |
| `PostTreat_Nauplii_Ind`        | numeric               | count      | Total nauplii produced per female after isolation clutch (individual-level sum)                     |
| `has_post_clutch`              | categorical           | —          | Indicator variable specifying whether female produced ≥1 clutch post-isolation                      |
| `has_post_hatch`               | categorical           | —          | Indicator variable specifying whether female produced ≥1 successful hatch post-isolation            |
| `Oldest_nonzero_F1_minusfirst` | numeric               | days       | Maximum age at which female produced a clutch that yielded ≥1 nauplius, excluding first clutch      |


## Notes

- Dates are formatted as YYYY-MM-DD.
- Proportions range from 0 to 1.
- Missing values are coded as NA.
- First clutch refers to clutch present at time of isolation.
- Post-treatment variables exclude clutch 1 to avoid bias from pre-experimental reproductive investment.
