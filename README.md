# OCR_P7_POC
Ce projet concerne une preuve de concept (POC) sur Vision Transformers.

Le but est de comparer ce nouveau type de réseau de neurones à un réseau "plus classique" de neurones convolutionnels, type MobileNetV2, concernant la classification d'images de style cartoon.

Une base de 1000 images de style cartoon a été constituée, classée en 10 classes de 100 images : chien, chat, fleur, arbre, avion, voiture, tigre, pingouin, oiseau, panda.

Les modèles comparés sont :
- Modèle de référence : MobileNetV2 pré-entrainé sur ImageNet en utilisant Keras, 
- Modèle testé : Vision Transformers ViT-B 32 [vit-keras](https://github.com/faustomorales/vit-keras) pré-entrainé sur ImageNet21k

L'apprentissage s'est fait par en 2 temps :
- "gel des couches" pré-entrainées et entrainement de la dernière couche qui sert de classifieur
- puis fine-tuning en ré-entrainant toutes les couches des modèles.

### Résulats
Après fine tuning des modèles, il s’avère que le modèle ViT a montré de meilleures performances en terme de classification. Mais son poids excessif ne peut pas une utilisation pour toutes les plateformes.

Un notebook (exécuté sous GoogleColab), un rapport et une présentation sont disponibles.
