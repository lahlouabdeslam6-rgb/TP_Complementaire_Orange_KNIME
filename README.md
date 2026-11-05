# TP complémentaire Orange et KNIME

**Ismail Lahlou — AI — G6**

Adaptation personnelle du [dépôt de référence ZED-abd](https://github.com/ZED-abd/TP_Complementaire_Orange_KNIME). Son historique et ses auteurs sont conservés ; les scripts de base proviennent de ce dépôt. Le compte rendu personnel porte uniquement le nom d’Ismail Lahlou.

## État de validation

Les données et la simulation préparatoire scikit-learn ont été recalculées localement. Orange 3.40.0 a été exécuté localement : les cinq modèles, les prédictions et la validation croisée ont été recalculés. Le workflow de 14 widgets et 16 liens a été rechargé et exécuté avec succès ; voir `reports/validation_ismail.json` et les journaux Orange. Les résultats KNIME hérités restent des **simulations scikit-learn** : aucun workflow natif KNIME exécuté ni export .knwf n’est revendiqué.

Le document personnel est un **compte rendu de travail**. Avant remise comme TP complet, les captures Orange demandées et le workflow/captures/résultats natifs KNIME doivent être présents. Aucun graphique Python n’est présenté comme une capture d’interface.

- [Compte rendu personnel](reports/Lahlou_Ismail_AI_G6_TP_lowcode.pdf)
- [Résultats Orange](reports/orange_resultats.md)
- [Guide KNIME et contrôles à réaliser](reports/guide_knime.md)
- [Questions et réponses](reports/questions_reponses.md)
- [Instructions techniques originales](README_REFERENCE.md)
- [Source initiale et attribution](https://github.com/ZED-abd/TP_Complementaire_Orange_KNIME)

## Reproduction locale

Orange est installé dans un environnement séparé du TP4/TP5. La version Python et les bibliothèques effectivement utilisées sont dans les JSON et dans le verrou personnel. Régénérer les données avec `scripts/donnees.py`, puis exécuter `scripts/orange_experiences.py` et `scripts/workflow_orange.py` avec le Python Orange. Les étapes KNIME sont décrites dans le guide ; la simulation Python ne les remplace pas.

Le résultat réel du TP04 d’Ismail (FLAML 60 s, lgbm, F1 0,8409) est conservé séparément dans `reports/tp4_ismail_reference.json`. Les découpages Orange/FLAML diffèrent : aucun classement statistique n’est déduit de leur simple écart de score.
