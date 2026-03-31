# Git/GitHub Commands

## Het mentale model

```
werkmap → (git add) → bakje → (git commit) → lokaal → (git push) → GitHub
```

Tegenovergestelde richting:

```
GitHub → (git pull) → lokaal
```

Branches zijn parallelle werelden. Verkenner laat altijd alleen de **actieve branch** zien.

```
lokaal:   add-my-name  ●──●──●   (jij loopt voor → git push)
GitHub:   add-my-name  ●──●──●──●  (GitHub loopt voor → git pull)
```

---

## Oriëntatie — waar ben ik?

```bash
git branch          # welke branches bestaan er? (* = waar je nu zit)
git status          # wat is de toestand van mijn werkmap?
git log --oneline   # geschiedenis van commits op deze branch
git diff bestand.txt  # wat is er veranderd ten opzichte van de laatste commit?
```

---

## Bewegen tussen branches

```bash
git checkout main           # ga naar main
git checkout add-my-name    # ga naar je eigen branch
git switch main             # nieuwere variant van checkout
```

---

## Bestand ophalen uit andere branch

```bash
git checkout main -- bestand.txt    # haal één bestand op uit main
```

---

## De drie stappen: lokaal opslaan

```bash
git add bestand.txt         # zet in het bakje (staging)
git add .                   # zet ALLES in het bakje
git commit -m "bericht"     # sla officieel op (altijd aanhalingstekens!)
```

---

## Synchroniseren met GitHub

```bash
git push    # stuur jouw commits naar GitHub (jij loopt voor)
git pull    # haal commits op van GitHub (GitHub loopt voor)
```

---

## Branches aanmaken

```bash
git branch add-my-name              # maak een nieuwe branch aan
git checkout -b add-my-name         # maak aan én ga er meteen naartoe
git push origin add-my-name         # zet de nieuwe branch op GitHub
```

---

## Handige ezelsbruggetjes

| Commando | Wat het eigenlijk betekent |
|---|---|
| `git add` | "leg in het bakje klaar voor verzending" |
| `git commit` | "sla officieel op in git's geheugen" |
| `git push` | "haal GitHub bij tot waar ik ben" |
| `git pull` | "haal mij bij tot waar GitHub is" |
| `git checkout` | "verplaats mij" óf "haal dit op" (verwarrend!) |
| `git switch` | "verplaats mij" (nieuwer, duidelijker) |
| `git restore` | "haal dit op" (nieuwer, duidelijker) |
| `origin` | de naam die git geeft aan GitHub |
| `HEAD` | waar je nu staat in de geschiedenis |

---

*Vul dit lijstje zelf aan als je nieuwe dingen leert — dan wordt het jóuw lijstje.* 🌱
