# SIMULATION scikit-learn, pas une mesure KNIME

Provenance : **simulation scikit-learn**. Aucun nœud KNIME n’a été exécuté. Partage stratifié 75/25, graine 42 : 3750 lignes dont 426 fraudes ; test 1250 dont 142 fraudes. Les indices et prédictions sont dans knime_simulation_predictions.csv ; versions et paramètres complets dans knime_simulation_resultats.json.

Hypothèses : quatre attributs numériques, sans standardisation ajoutée ; LR avec max_iter=2000 pour convergence ; RF 100 arbres ; GB 100 arbres, profondeur 4, learning_rate=0.1 ; graines des trois modèles 42, un seul processus. Les algorithmes, encodages et lignes du partage peuvent différer des nœuds KNIME.

| Modèle | AUC | CA | F1 classe 1 | Précision 1 | Rappel 1 |
|---|---|---|---|---|---|
| Logistic Regression | 0.979420 | 0.940800 | 0.701613 | 0.820755 | 0.612676 |
| Random Forest | 0.980589 | 0.956800 | 0.792308 | 0.872881 | 0.725352 |
| Gradient Boosting | 0.986535 | 0.960000 | 0.813433 | 0.865079 | 0.767606 |

- Logistic Regression : matrice réelle/prédite [0,1] = `[[1089, 19], [55, 87]]` ; total 1250, lignes réelles [1108,142] contrôlées.
- Random Forest : matrice réelle/prédite [0,1] = `[[1093, 15], [39, 103]]` ; total 1250, lignes réelles [1108,142] contrôlées.
- Gradient Boosting : matrice réelle/prédite [0,1] = `[[1091, 17], [33, 109]]` ; total 1250, lignes réelles [1108,142] contrôlées.

L’énoncé indique 0,75 à 0,85 comme ordre de grandeur KNIME, pas comme égalité de validation. Notre LR simulée vaut 0.701613 : elle est sous cette plage indicative. La simulation conserve les attributs bruts, les paramètres sklearn explicites et son propre tirage de lignes ; elle ne reproduit pas l’optimiseur, les réglages internes ni le tirage exact de KNIME. L’identité des causes avec une future exécution KNIME ne peut pas être établie avant cette exécution ; aucune valeur n’est forcée.

Les F1 KNIME réels restent **[À FAIRE PAR L'ÉTUDIANT]**, voir guide_knime.md.
