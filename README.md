# README — Configuration Mobexler sur Kali Linux (VirtualBox dans VMware)

## Étape 1 — Téléchargement de l'OVA

### 1.1 Télécharger
- Lien officiel (Google Drive) : https://drive.google.com/file/d/1rd8g3bmK_XMTtb6PlcfIwjyoJ-mEhAk5/view
- Taille : **14 Go**

### 1.2 Vérifier l'intégrité (SHA256)

```bash
sha256sum ~/Téléchargements/Mobexler.ova

──(salma㉿kali)-[~/Téléchargements]
└─$ sha256sum Mobexler.ova
07c40d1456b564313996f8a8bd5402e9ebb825d7b817c5031c52396231ddf188  Mobexler.ova

```

**Hash officiel** (source : mobexler.com/set-up) :
```
07c40d1456b564313996f8a8bd5402e9ebb825d7b817c5031c52396231ddf188
```


## Étape 2 — Import de l'OVA dans VirtualBox

1. Ouvrir **VirtualBox**
2. **File → Import Appliance**
3. Sélectionner `Mobexler.ova`
4. Cliquer **Import**

---

## Étape 4 — Prérequis VirtualBox (modules kernel)

>  VirtualBox doit tourner sur Kali — il faut que les modules kernel correspondent.
> <img width="536" height="536" alt="image" src="https://github.com/user-attachments/assets/604912e2-c683-47ea-9e91-fa5bf3dd3550" />

```

```

## Étape 3 — Vérifications réseau (tests santé)

Depuis le terminal **Mobexler** :

```
# Voir toutes les interfaces
ip a
•	Interface Host-Only 192.168.56.101
•	Interface NAT 10.0.2.15
<img width="725" height="278" alt="image" src="https://github.com/user-attachments/assets/d0e7eadb-6fae-4994-9f91-a0dd0e39ce36" />

# Tester Internet (via NAT)
ping  3 8.8.8.8
ping  3 google.com
```
<img width="499" height="171" alt="image" src="https://github.com/user-attachments/assets/50ecc239-ac8b-431e-a943-e6c41d0f7d39" />

<img width="624" height="169" alt="image" src="https://github.com/user-attachments/assets/d74076b9-30e0-415f-8b9e-bffaf2d84824" />



