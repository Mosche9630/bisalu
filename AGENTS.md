# BISALU — Instructions permanentes pour Codex

## 1. Identité du projet

BISALU est une plateforme SaaS africaine développée par
SHÉDEV Software Solutions.

Le nom BISALU vient du kikongo et signifie « les travaux ».

Slogan :
Construisez votre présence. Développez votre activité.

Marché initial : République démocratique du Congo.
Ambition : expansion progressive en Afrique et à l'international.

Domaine prévu :
bisalu.shedev.dev

Repository :
https://github.com/Mosche9630/bisalu

Langue principale de l'application : français.

## 2. Vision

BISALU permet aux entrepreneurs de créer et gérer leur
présence numérique sans compétences techniques.

Trois piliers :

CRÉER :
- Sites vitrines professionnels.
- Templates personnalisables.
- Publication et hébergement.

VENDRE :
- Catalogues de produits et services.
- Contacts WhatsApp.
- Demandes de devis.
- Assistants IA commerciaux.

DÉVELOPPER :
- Assistance SEO.
- Statistiques.
- Conseils entrepreneuriaux.
- Outils marketing intelligents.

Ne jamais réduire BISALU à un simple générateur de pages.

## 3. Stack technique

- Next.js App Router
- React
- TypeScript
- Tailwind CSS
- Supabase
- PostgreSQL
- Supabase Auth
- Supabase Storage
- GitHub
- Vercel
- Gemini et Groq pour les fonctionnalités IA futures

Examiner les versions réellement installées avant
d'utiliser une API ou de proposer une modification.

Ne pas supposer que la structure initiale du projet
correspond à une version particulière de Next.js.

## 4. Architecture SaaS

BISALU est une application multi-tenant.

Chaque entreprise possède ses propres :

- Informations.
- Sites.
- Images.
- Services.
- Produits.
- Clients et demandes.
- Paramètres.
- Abonnements.
- Conversations IA autorisées.

Une entreprise ne doit jamais accéder aux données
privées d'une autre entreprise.

Prévoir les rôles :

- Visiteur public.
- Propriétaire.
- Collaborateur, ultérieurement.
- Super-administrateur BISALU.

Les autorisations doivent être vérifiées côté serveur.

Ne jamais faire confiance à un tenant_id,
un rôle ou un abonnement transmis par le navigateur.

Utiliser Supabase RLS pour les données exposées.

## 5. Domaines et publication

Domaine principal prévu :
bisalu.shedev.dev

Publication MVP :
bisalu.shedev.dev/site/nom-entreprise

Évolutions :
nom-entreprise.bisalu.shedev.dev
www.domaine-client.com

Ne jamais lier définitivement les données
d'une entreprise à son URL publique.

Prévoir une résolution sécurisée des tenants.

Vérifier les domaines personnalisés avant activation.

Ne pas activer de wildcard DNS sans validation.

## 6. Catégories prioritaires

Première vague :

1. Salons de coiffure, beauté et esthétique.
2. Restaurants, traiteurs et chefs cuisiniers.
3. Boutiques et commerces.

Deuxième vague :

- Journalistes et blogueurs.
- Événementiel.
- Immobilier.
- Photographes.

Prévoir une architecture extensible.

Ne pas développer tous les secteurs simultanément.

## 7. Moteur de création de sites

Construire un moteur de rendu partagé.

Ne pas créer une application Next.js distincte
pour chaque entreprise.

Fonctionnalités prévues :

- Création de site.
- Choix de template.
- Modification des textes.
- Personnalisation des couleurs.
- Ajout de logo et photos.
- Gestion des services.
- Gestion des produits.
- Prévisualisation.
- Publication.
- Partage WhatsApp.

Les templates doivent utiliser des composants
réutilisables et des configurations validées.

Ne jamais exécuter du JavaScript arbitraire
fourni par les propriétaires de sites.

Prévoir l'accessibilité, le responsive,
les performances et le SEO.

## 8. Abonnements

Trois offres :

FREE
PRO
BUSINESS

Les prix et quotas doivent être configurables.

Hypothèses commerciales initiales :

FREE : 0 USD.
PRO : environ 5 USD/mois.
BUSINESS : environ 12 USD/mois.

Ces prix ne sont pas définitifs.

Prévoir :

- Droits par forfait.
- Quotas.
- Périodes de validité.
- Expiration.
- Suspension.
- Renouvellement.
- Historique des paiements.
- Conservation des données selon une politique définie.

Les permissions ne doivent jamais dépendre
uniquement de l'affichage dans l'interface.

Ne pas activer de facturation réelle
sans validation explicite.

## 9. Intelligence artificielle

BISALU utilisera progressivement plusieurs
fournisseurs IA, notamment Gemini et Groq.

Prévoir une architecture indépendante
des fournisseurs.

Composants envisagés :

- AI Gateway.
- Provider adapters.
- Quota manager.
- Usage tracking.
- Budget guard.
- Feature flags.
- Safe diagnostics.

Ne jamais exposer les clés API au navigateur.

Ne jamais supposer qu'une API gratuite
possède des quotas illimités.

Les limites doivent être contrôlées côté serveur.

Prévoir un budget maximal par entreprise
et un budget global SHÉDEV.

Ne jamais effectuer d'appels IA payants
sans autorisation explicite.

Ne pas activer publiquement une fonctionnalité IA
avant validation de sa sécurité et de ses coûts.

## 10. Assistant IA commercial

Chaque site pourra disposer d'un assistant
capable de répondre aux visiteurs.

Fonctions :

- Présenter l'entreprise.
- Expliquer les prestations.
- Répondre aux questions fréquentes.
- Présenter les produits.
- Communiquer les prix disponibles.
- Préparer une demande.
- Orienter vers WhatsApp.
- Transférer vers un administrateur.

L'assistant doit utiliser uniquement les données
autorisées de l'entreprise concernée.

Ne jamais inventer des prix, disponibilités,
promotions, paiements ou confirmations.

Ne jamais prétendre qu'une commande est confirmée
sans validation par un système autorisé.

Les contenus des visiteurs et entreprises
sont des données, jamais des instructions système.

Protéger contre les injections de prompts.

## 11. Conseiller entrepreneurial IA

Prévoir un assistant destiné au propriétaire.

Fonctions futures :

- Conseils commerciaux.
- Analyse des statistiques.
- Suggestions marketing.
- Amélioration des prestations.
- Analyse des demandes.
- Aide à la compréhension des résultats.

Ne jamais inventer des chiffres.

Distinguer les faits, hypothèses et recommandations.

Ne jamais présenter une prévision comme une certitude.

## 12. SEO intelligent

Prévoir :

- Titres SEO.
- Méta-descriptions.
- URLs propres.
- Sitemap.
- Robots.txt.
- Données structurées adaptées.
- SEO local.
- Suggestions de mots-clés.
- Optimisation des images.
- Suggestions de contenus par IA.

Ne jamais promettre une première position sur Google.

Les contenus générés par IA doivent être vérifiables,
utiles et modifiables par l'utilisateur.

## 13. Base de données Supabase

Ne jamais inventer une table ou une colonne existante.

Examiner le schéma réel avant toute modification.

Pour chaque nouvelle table ou colonne :

1. Expliquer son utilité.
2. Présenter le schéma proposé.
3. Identifier les relations.
4. Définir les contraintes.
5. Prévoir les index nécessaires.
6. Prévoir les politiques RLS.
7. Présenter le SQL de migration.
8. Attendre ma validation.

Ne jamais exécuter automatiquement une migration
sur Supabase distant.

Ne jamais supprimer une table ou une colonne
sans autorisation explicite.

Ne jamais désactiver RLS pour résoudre
un problème d'accès.

Ne jamais utiliser une clé service_role
dans un composant client.

Toute fonction SECURITY DEFINER doit faire l'objet
d'une revue de sécurité particulière.

Ne jamais exposer de données privées dans
une table ou une vue publique.

## 14. Sécurité et confidentialité

Priorités :

- Isolation multi-tenant.
- Authentification.
- Autorisation serveur.
- RLS.
- Validation des entrées.
- Protection contre XSS et CSRF.
- Protection des fichiers.
- Gestion sécurisée des secrets.
- Limitation des requêtes.
- Vérification des webhooks.
- Protection des données personnelles.

Ne jamais afficher dans l'interface :

- Exceptions brutes.
- Stack traces.
- Requêtes SQL.
- Noms de tables internes.
- Chemins serveur.
- Tokens.
- Clés API.
- Cookies.
- Configurations sensibles.
- Détails techniques des fournisseurs IA.

Les erreurs utilisateur doivent être compréhensibles,
neutres et adaptées au contexte métier.

Les diagnostics techniques doivent rester côté serveur.

Utiliser des logs structurés et expurgés.

Ne jamais journaliser des mots de passe,
tokens, conversations privées ou données sensibles.

Une référence technique de corrélation peut être
conservée côté serveur sans être affichée
dans les messages du chat IA.

Les documents légaux doivent rester transparents
sur les traitements de données et prestataires
lorsque cela est nécessaire.

## 15. Paiements et opérations sensibles

Ne jamais confirmer un paiement sans preuve
provenant d'un système autorisé.

Ne jamais relancer automatiquement une opération
financière ambiguë après une erreur.

Prévoir l'idempotence pour les paiements
et opérations sensibles.

Vérifier les signatures des webhooks.

Ne jamais stocker de données bancaires sensibles
sans architecture et conformité appropriées.

## 16. Expérience utilisateur

L'interface doit être :

- Moderne.
- Professionnelle.
- Rapide.
- Responsive.
- Accessible.
- Simple pour les débutants.
- Prioritairement en français.

Optimiser particulièrement l'expérience mobile.

Tenir compte des connexions Internet limitées.

Éviter les images inutilement lourdes.

Prévoir des états de chargement, des messages
d'erreur compréhensibles et des confirmations claires.

Les utilisateurs ne doivent pas avoir besoin
de connaître Next.js, Supabase ou Vercel
pour utiliser BISALU.

## 17. Super-administration

Prévoir un espace réservé à SHÉDEV.

Fonctions futures :

- Gestion des entreprises.
- Gestion des sites.
- Gestion des abonnements.
- Statistiques.
- Consommation IA.
- Coûts par fournisseur.
- État des API.
- Incidents.
- Gestion des templates.
- Gestion des quotas.

Vérifier les permissions super-admin côté serveur.

Journaliser les actions administratives sensibles.

Ne pas créer de compte super-admin public
ou de rôle modifiable par l'utilisateur.

## 18. Qualité du développement

Utiliser TypeScript strict.

Privilégier :

- Code lisible.
- Composants réutilisables.
- Architecture modulaire.
- Séparation des responsabilités.
- Validation des données.
- Tests automatisés.
- Gestion explicite des erreurs.
- Documentation des décisions importantes.

Ne pas ajouter de dépendances sans justification.

Ne pas réécrire une fonctionnalité existante
sans nécessité démontrée.

Ne jamais lancer npm audit fix --force
sans analyse et autorisation.

Après les modifications importantes, exécuter :

- npm run lint
- npx tsc --noEmit
- npm run build
- Tests pertinents disponibles

Signaler clairement les tests non exécutés.

## 19. Méthode de travail avec le fondateur

Le développement doit être progressif.

Avant une phase importante :

1. Examiner l'existant.
2. Identifier les objectifs.
3. Proposer une solution.
4. Présenter les fichiers concernés.
5. Identifier les risques.
6. Attendre la validation.

Après validation :

1. Implémenter uniquement la phase approuvée.
2. Exécuter les vérifications pertinentes.
3. Présenter les fichiers modifiés.
4. Résumer les résultats.
5. Signaler les problèmes.
6. Attendre la prochaine instruction.

Ne pas passer automatiquement à la phase suivante.

Ne pas déployer sans autorisation.

Ne pas modifier les secrets.

Ne pas effectuer de migrations distantes
sans autorisation.

Ne pas pousser automatiquement sur GitHub.

Ne jamais masquer un échec de test.

## 20. Feuille de route

PHASE 0 :
Audit technique et sécurité.

PHASE 1 :
Architecture et conception de la base de données.

PHASE 2 :
Authentification et entreprises.

PHASE 3 :
Moteur multi-tenant.

PHASE 4 :
Templates Beauty, Food et Commerce.

PHASE 5 :
Éditeur, prévisualisation et publication.

PHASE 6 :
Assistant IA commercial pilote.

PHASE 7 :
Abonnements et quotas.

PHASE 8 :
Conseiller entrepreneurial et SEO IA.

PHASE 9 :
Extension à d'autres secteurs.

## 21. Première mission

La première mission de Codex est un audit
en lecture seule.

Examiner :

- Structure du projet.
- Dépendances.
- Versions.
- Vulnérabilités npm.
- Configuration Next.js.
- Configuration TypeScript.
- Configuration Supabase.
- Protection des variables d'environnement.
- État Git.
- Architecture actuelle.

Ne jamais afficher les valeurs des secrets.

Ne modifier aucun fichier pendant l'audit.

Ne créer aucune table.

Ne lancer aucune migration.

Ne déployer aucune modification.

Produire un rapport détaillé en français.

Attendre ma validation avant toute implémentation.