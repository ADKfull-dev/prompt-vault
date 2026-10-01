# Prompt Vault

Landing page de vente de l'ebook « Prompt Vault » (116 prompts IA, PDF).

- Page publique : `index.html`
- Réglages du site : `config.json` (lien Chariow + avis clients), lu au chargement de la page.
- Espace admin : `admin.html` (ex. `https://<compte>.github.io/prompt-vault/admin.html`)

## Espace admin

1. Créez un token GitHub « fine-grained » limité à ce dépôt, permission **Contents : Read and write**
   (https://github.com/settings/personal-access-tokens/new).
2. Ouvrez `admin.html`, indiquez le dépôt (`propriétaire/nom`, pré-rempli sur GitHub Pages) et le token.
3. **Compte Chariow** : collez le lien de votre boutique et le lien de paiement du produit, puis « Lier le compte ».
   Tous les boutons d'achat du site pointent alors vers ce lien. « Délier » le retire.
4. **Avis clients** : ajoutez ou supprimez de vrais avis (la section reste cachée tant qu'il n'y en a aucun).
5. « Enregistrer et publier » fait un commit de `config.json` ; le site est à jour après la republication GitHub Pages (1 à 2 min).

Le token reste dans l'onglet du navigateur (sessionStorage) et n'est jamais écrit dans le dépôt.
Seules les personnes ayant un accès en écriture au dépôt peuvent modifier le site.
