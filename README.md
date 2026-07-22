# TP PKI — Certificat SSL pour serveur Apache

## Objectif

Mettre en place une PKI entre une machine **CA** et une machine **Serveur**, afin de générer et signer un certificat SSL utilisé par Apache pour sécuriser le site en HTTPS.

## Fichiers du TP

| Fichier | Description |
|---|---|
| `certif.ca` | Certificat auto-signé de la CA |
| `server.cert` | Certificat du serveur, signé par la CA |
| `server.pfx` | Enveloppe PKCS#12 regroupant le certificat et la clé privée du serveur |

## Étapes

### Côté CA
1. Génération de la clé privée de la CA
2. Génération du certificat auto-signé (`certif.ca`)

### Côté Serveur
3. Génération de la clé privée du serveur
4. Création d'une demande de certificat (CSR)
5. Envoi de la CSR à la CA

### Retour côté CA
6. Signature de la CSR avec `certif.ca` et la clé privée de la CA → génère `server.cert`
7. Envoi du certificat signé au serveur

### Côté Serveur
8. Création de l'enveloppe `server.pfx` (certificat + clé privée)

## Démo
[![asciicast](https://asciinema.org/a/VlFrSDYSEd1sqDVA.svg)](https://asciinema.org/a/VlFrSDYSEd1sqDVA)
