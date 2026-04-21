Le dataset Olist n'est pas un seul gros tableau, mais 9 pièces de puzzle qui s'assemblent. Voici comment je vais les utiliser pour mon analyse :

🔴 Le Cœur du Projet : Les Commandes (orders)
C’est ma table de référence. Elle contient les dates clés (achat, expédition, livraison).

Mon but : Calculer les délais de livraison réels.

🟢 Le Lien "Ventes" : Produits & Articles (items & products)
Ces tables me disent ce qui a été vendu et à quel prix.

Liaison : order_id relie la commande aux articles.

Mon but : Identifier les catégories de produits les plus populaires.

🔵 Le Lien "Client" : Localisation (customers)
Cette table me dit où habitent les acheteurs.

Liaison : customer_id relie la commande au client.

Mon but : Voir quels États du Brésil commandent le plus.

🟡 Le Lien "Satisfaction" : Avis (reviews)
Ici, on trouve les notes de 1 à 5 étoiles.

Liaison : order_id.

Mon but : Voir si un retard de livraison fait baisser la note (corrélation).

🟠 Le Lien "Argent" : Paiements (payments)
Comment les gens paient-ils ? (Carte, ticket, plusieurs mensualités).

Liaison : order_id.

Mon but : Analyser le nombre moyen de mensualités par achat.

🛠 Ma stratégie pour la suite
Puisque je débute, je ne vais pas essayer de lier les 9 tables d'un coup.

Je vais d'abord nettoyer la table Orders (Dates, valeurs nulles).

Ensuite, j'utiliserai la fonction RECHERCHEV (VLOOKUP) dans Excel pour ramener les informations des autres tables quand j'en aurai besoin.
