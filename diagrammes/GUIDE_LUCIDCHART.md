# Guide Lucidchart — recréer les 5 diagrammes UML

Les fichiers `.mmd` de ce dossier sont la **source unique** des diagrammes. Ce sont eux qui ont servi
à produire les figures du PDF, et ce sont eux qu'on importe dans Lucidchart.

| Fichier | Diagramme | Nom du document Lucidchart à créer |
|---|---|---|
| `01_cas_utilisation.mmd` | Cas d'utilisation | `TP GL Motos UNSTIM — 1. Cas d'utilisation` |
| `02_classes.mmd` | Classes | `TP GL Motos UNSTIM — 2. Classes` |
| `03_activite.mmd` | Activité | `TP GL Motos UNSTIM — 3. Activité` |
| `04_sequence.mmd` | Séquence | `TP GL Motos UNSTIM — 4. Séquence` |
| `05_composants.mmd` | Composants | `TP GL Motos UNSTIM — 5. Composants` |

Fichier complémentaire (hors des 5 diagrammes demandés) : `06_schema_fonctionnement.mmd`, schéma de
fonctionnement du dispositif (figure du § 4).

## 1. Import (identique pour les 5 diagrammes)

1. Ouvrir <https://lucid.app> et se connecter.
2. **+ Nouveau → Lucidchart → Document vierge**.
3. Renommer le document (clic sur « Document sans titre » en haut à gauche) avec le nom du tableau ci-dessus.
4. Menu **Insérer → Diagramme sous forme de code** (en anglais : *Insert → Diagram as code*).
5. Dans le panneau qui s'ouvre, choisir le langage **Mermaid**.
6. Supprimer l'exemple, coller **tout** le contenu du fichier `.mmd` (les lignes `%%` sont des commentaires et ne posent pas de problème).
7. Vérifier l'aperçu, puis cliquer sur **Insérer** (*Insert*).
8. Centrer le diagramme sur la page : sélectionner tout (Ctrl + A), puis **Organiser → Aligner → Centrer**.
9. Ajouter au-dessus du diagramme une zone de texte « Figure n — titre » identique à la légende du PDF.

> Si l'option « Diagramme sous forme de code » n'apparaît pas : **Fichier → Importer → Mermaid**,
> ou la bibliothèque de formes UML (voir § 3) pour recréer le diagramme à la main à partir de la figure du PDF.

## 2. Étapes propres à chaque diagramme

**Cas d'utilisation.** Après import, remplacer les trois rectangles « «acteur» » par la forme UML
**Acteur** (bonhomme) de la bibliothèque *UML Cas d'utilisation*, en gardant les noms Propriétaire,
Agent de sécurité, Administrateur. Vérifier : flèches `«include»` du cas de base vers le cas inclus,
flèche `«extend»` de « Déclencher l'alarme » vers « Démarrer la moto », garde `[3 échecs consécutifs]`.

**Classes.** Vérifier les trois compartiments, les visibilités `-` / `+`, les multiplicités aux deux
extrémités, le losange plein de la composition côté Utilisateur et la flèche pointillée `«compare»`.

**Activité.** Vérifier que le nœud initial est un disque plein et que les nœuds finaux sont des
cibles (disque cerclé). Sinon, les remplacer par les formes *UML Activité → Nœud initial / Nœud final*.
Gardes entre crochets sur chaque sortie de losange.

**Séquence.** Vérifier la numérotation des messages, les retours en pointillés, le cadre `alt` avec
sa séparation `else`, et le cadre `opt` imbriqué dans la branche d'échec.

**Composants.** Si besoin, remplacer les rectangles « «composant» » par la forme UML **Composant**
(rectangle avec deux petits rectangles). Conserver les 4 conteneurs de couche et leurs couleurs.

## 3. Liste de contrôle de mise en forme (à cocher pour chaque diagramme)

- [ ] Police unique : **Segoe UI** ou **Arial**, 11 pt pour les éléments, 10 pt pour les libellés de relations, 14 pt gras pour le titre.
- [ ] Couleurs de la charte : bleu nuit `#1F3A5F` (traits, titres), bleu `#2E6DB4` (éléments inclus, gestion), vert `#2E8B57` (traitement, succès), or `#B7860B` (matériel, décisions), violet `#7B3FA0` (données), rouge `#C0392B` (alarme, échec).
- [ ] Alignement : **Organiser → Aligner** et **Répartir** horizontalement / verticalement ; aucun chevauchement de libellés.
- [ ] Les flèches ne se croisent pas inutilement (utiliser les connecteurs coudés).
- [ ] Libellés identiques au glossaire (`GLOSSAIRE.md`) : aucun synonyme.
- [ ] Seuil écrit « 3 échecs consécutifs » / `compteurEchecs ≥ 3` / `SEUIL_ECHECS = 3`.
- [ ] Titre et légende « Figure n » présents.
- [ ] Marges de page : **Page → Ajuster la page au contenu**.

## 4. Partage et lien

1. Bouton **Partager** (en haut à droite).
2. Section « Accès général » : **Toute personne disposant du lien** → **Peut afficher** (lecture seule).
3. **Copier le lien** et le reporter dans `LIENS.md`.

État des liens : voir `../LIENS.md`.
