# QA – Medicofit PROM v1.3

Preverjeno:
- JavaScript sintaksa: OK (Node --check).
- 27 vprašalnikov ostaja v DATA.
- Application ID nespremenjen: si.medicofit.prom.
- versionCode: 4.
- versionName: 1.3.0.
- storage key nespremenjen: medicofit_prom_android_history_v1.
- nove meritve vsebujejo answerDetails + answers + metrics.
- arhiv ima filtre: patient, therapist, questionnaire, sort.
- podrobnosti meritve izračunajo/prikažejo vse metrike in odgovore.
- stare meritve imajo fallback prikaz iz raw answers.

- projekt vsebuje stabilni podpisni ključ `app/medicofit-prom-keystore.jks`.
- debug in release build uporabljata isti Medicofit signingConfig za prihodnje posodobitve.
