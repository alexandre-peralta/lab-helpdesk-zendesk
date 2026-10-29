Laboratoire Helpdesk Zendesk et Active Directory 

[Lire le PDF du laboratoire](Laboratoire%20Helpdesk%20Zendesk%20-%20Active%20Directory.pdf)

Traitement de tickets de niveau 1 avec Zendesk et Active Directory, pour une entreprise fictive: Peralta IT Services, domaine peralta.local.

Objectif

Pratiquer le ticketing helpdesk de niveau 1 sur un scénario complet. Chaque ticket est suivi de bout en bout: réception et qualification, premier contact avec le demandeur, diagnostic, action dans Active Directory, vérification sur le poste client, puis clôture.

Environnement

	•	Zendesk (essai) pour la gestion des tickets
	•	Windows Server avec le rôle AD DS, domaine peralta.local
	•	Poste client Windows 11 joint au domaine
	•	VMware Fusion, réseau virtuel isolé

Les 4 tickets

Ticket	Type	Priorité	Résolution
Compte verrouillé	Incident	Élevée	Déverrouillage du compte dans Active Directory, sans réinitialiser le mot de passe
Accès refusé au dossier partagé Comptabilité	Incident	Normale	Correction de l'appartenance aux groupes selon la méthode AGDLP
Arrivée d'un nouvel employé	Tâche	Normale	Création du compte, changement de mot de passe obligatoire, appartenance au groupe du service
Départ d'un employé	Tâche	Élevée	Compte désactivé avec date d'expiration, retiré des groupes, déplacé dans l'UO Comptes désactivés

Méthode de traitement

Pour chaque ticket, le même parcours:

	1.	Réception, qualification (type, priorité) et assignation
	2.	Première réponse publique au demandeur
	3.	Diagnostic
	4.	Action dans Active Directory
	5.	Vérification sur le poste client
	6.	Clôture: note interne de diagnostic, réponse finale au demandeur, statut Résolu

Bonnes pratiques expliquées dans le document

	•	Déverrouiller un compte sans réinitialiser le mot de passe quand l'utilisateur le connaît
	•	Déconnexion et reconnexion pour appliquer les nouveaux groupes
	•	gpupdate /force pour appliquer une stratégie immédiatement
	•	Méthode AGDLP: comptes dans des groupes globaux, groupes globaux dans des groupes de domaine local, droits donnés aux groupes de domaine local
	•	Droits de partage et permissions NTFS séparés, sans jamais donner le contrôle total aux utilisateurs
	•	Séparation du système et des données sur deux volumes
	•	Désactivation d'un compte avec date d'expiration et retrait des groupes lors d'un départ

Compétences démontrées

Ticketing helpdesk niveau 1, Zendesk, Active Directory, gestion des utilisateurs et des groupes, stratégie de groupe, méthode AGDLP, permissions NTFS, arrivée et départ d'employés, communication avec l'utilisateur, documentation de chaque intervention.

Documentation

Le PDF complet de 22 pages, avec 37 captures d'écran, se trouve dans ce repository.
