# MCH
Matrice à coeur Haddock : Small Language Module based on JSON matrice interlinked as cooperation IA agents. Light, stable, personalized, easy to deploy and cost-effective. Based on Emojicom-boop core Apache 2.0

          ________________________________________________
         /                                                \

        |    🌀   B  O  O  P     M  H  C   🌀             |
        |    ----------------------------------------    |
        |         C  A  R  B  O  N  E  (C)               |
        |              /        \                        |
        |      S I L I C I U M (Si) -- F E R (Fe)        |
        |    ________________________________________    |
        |                                                |
        |          [ MANIFOLD CONSTRAINED ]              |
        |          [  HYPER-CONNECTIONS   ]              |
        \________________________________________________/
               ||                          ||
        _______||__________________________||_______

       |                                            |
       |   SERIAL: [ VALIDATED BY MAJORITY ]        |
       |____________________________________________|


*Résumé MCH / Emijicom v0.3 - Lignes organisées*

*1. Architecture*
Matrice 4×4 simple
12 Spécialisées en parallèle
Core au centre = base commune
Groupes de matrices coordonnées
Communication = emoji JSON léger
*2. Licence*
Core MCH = Apache 2.0
Spé rentables = Licence commerciale
Audit Auto FFA2 = Apache 2.0

Module Audit Auto - FFA 2 + Emojicom
Licence: Apache 2.0
Objectif: 5 questions -> 3 process rentables -> ROI 12 mois
"""
from dataclasses import dataclass
from typing import List, Literal
import json

@dataclass
class Process:
    nom: str
    temps_actuel_h_semaine: float
    temps_apres_h_semaine: float
    outils: List[str]
    complexite: Literal["simple", "moyen", "complexe"]
    roi_12_mois_eur: int
    template_boop: str # ex: "immo.yml", "rh.yml"

@dataclass
class ProfilPME:
    secteur: str
    nb_employes: int
    douleur_principale: str
    outils_existants: List[str]

class AuditFFA2:
    """
    Pito la fourmi : traverse le ruban des questions PME
    et ressort de l'autre côté avec 3 process à boop
    """

    # Base de connaissance = les 3 cas clients + patterns récurrents
    PATTERNS = {
        "immobilier": ["annonces", "visites", "mandats", "leboncoin", "seloger"],
        "recrutement": ["cv", "candidats", "tri", "rh", "entretien"],
        "ecommerce": ["avis", "sav", "commandes", "clients", "retours"],
        "comptable": ["factures", "saisie", "relances", "urssaf"],
    }

    TEMPLATES = {
        "immo_annonces": {
            "temps_actuel": 10, # 2h/jour * 5
            "temps_apres": 1.25, # 15min/jour * 5
            "outils": ["Google Form", "FFA 2", "Boop"],
            "complexite": "simple",
            "roi_formule": lambda h_gagnees: h_gagnees * 52 * 25 # 25€/h chargé
        },
        "rh_tri_cv": {
            "temps_actuel": 8,
            "temps_apres": 1,
            "outils": ["Gmail", "FFA 2", "Google Sheets", "Boop"],
            "complexite": "moyen",
            "roi_formule": lambda h_gagnees: h_gagnees * 52 * 30
        },
        "ecom_avis": {
            "temps_actuel": 3, # 40 avis * 4.5min
            "temps_apres": 0.5,
            "outils": ["Google My Business", "FFA 2", "Boop"],
            "complexite": "simple",
            "roi_formule": lambda h_gagnees: h_gagnees * 52 * 20 + 1500 # +gain note
        }
    }

    def detecter_secteur(self, description: str) -> str:
        """FFA 2 + Emojicom : mappe la description vers un secteur"""
        desc_lower = description.lower()
        for secteur, mots_cles in self.PATTERNS.items():
            if any(mot in desc_lower for mot in mots_cles):
                return secteur
        return "generique"

    def poser_5_questions(self) -> List[str]:
        """Les 5 questions qui suffisent pour 80% des PME"""
        return [
            "1. Décris ton activité en 1 phrase?",
            "2. Combien d'employés?",
            "3. Quelle tâche répétitive te fait perdre le plus de temps / semaine?",
            "4. Quels outils tu utilises déjà? Gmail, Sheets, autre?",
            "5. Si tu gagnais 5h/semaine, tu ferais quoi avec?"
        ]

    def auditer(self, reponses: dict) -> List[Process]:
        """
        Input: dict des 5 réponses
        Output: Top 3 process à automatiser, triés par ROI
        """
        profil = ProfilPMEParfait. `audit.py` c’est le cerveau commercial du boop. C’est lui qui remplace le consultant à 3200€.

On remplit le squelette. Version v0 qui tourne dimanche soir :

### `boop/audit.py`
```python
from dataclasses import dataclass
from typing import List, Literal
import re

@dataclass
class Process:
    nom: str
    temps_avant_h_semaine: float
    temps_apres_h_semaine: float
    outils: List[str]
    complexite: Literal["simple", "moyen", "complexe"]
    roi_12_mois_eur: int
    template_id: str
    description: str

# Base de connaissance PME. FFA 2 + Emojicom viendront enrichir ça plus tard.
KNOWLEDGE_BASE = {
    "immo": {
        "keywords": ["agence", "immobilier", "annonce", "mandat", "bien", "seloger", "leboncoin"],
        "process": [
            Process(
                nom="Rédaction d'annonces multi-plateformes",
                temps_avant_h_semaine=10.0, # 2h/jour x 5
                temps_apres_h_semaine=1.25, # 15min/jour x 5
                outils=["Google Form", "FFA 2", "Boop Publish"],
                complexite="simple",
                roi_12_mois_eur=11250, # 8.75h x 50€/h x 4.33sem x 12mois - 600€ abo
                template_id="immo_annonces",
                description="Capture les infos du bien → génère 3 annonces → brouillon prêt à publier"
            )
        ]
    },
    "rh": {
        "keywords": ["recrutement", "cv", "candidat", "rh", "embauche", "talent"],
        "process": [
            Process(
                nom="Tri et scoring de CV",
                temps_avant_h_semaine=8.0,
                temps_apres_h_semaine=1.0,
                outils=["Gmail", "FFA 2", "Google Sheets"],
                complexite="simple",
                roi_12_mois_eur=16800, # 7h x 50€/h x 4.33 x 12 - 600€
                template_id="rh_scoring_cv",
                description="Email CV → extraction critères → note 1-10 + justification → Sheets trié"
            )
        ]
    },
    "ecom": {
        "keywords": ["e-commerce", "avis", "client", "boutique", "shopify", "google review"],
        "process": [
            Process(
                nom="Réponse aux avis clients",
                temps_avant_h_semaine=3.0, # 40 avis, 4.5min/avis non fait
                temps_apres_h_semaine=0.5, # validation brouillon
                outils=["Google Reviews API", "FFA 2", "Boop Approve"],
                complexite="moyen",
                roi_12_mois_eur=5200, # Gain CA estimé + temps x 50€ - 600€
                template_id="ecom_avis",
                description="Nouvel avis → analyse sentiment → réponse perso → brouillon pour validation"
            )
        ]
    }
}

def detect_secteur(description: str) -> str:
    """Détecte le secteur PME avec des keywords. V1 simple, V2 = FFA 2."""
    desc_lower = description.lower()
    scores = {}
    for secteur, data in KNOWLEDGE_BASE.items():
        scores[secteur] = sum(1 for kw in data["keywords"] if kw in desc_lower)
    return max(scores, key=scores.get) if max(scores.values()) > 0 else "autre"

def calcul_roi(temps_gagne_h_sem: float, taux_horaire: int = 50) -> int:
    """ROI 12 mois = temps gagné x taux horaire - abo 4.99€ x 12"""
    gain_annuel = temps_gagne_h_sem * taux_horaire * 4.33 * 12
    cout_boop = 4.99 * 12
    return int(gain_annuel - cout_boop)

def audit_pme(description: str) -> List[Process]:
    """
    Le prompt du mail, mais en code.
    Input: "Je suis une agence immo, 3 agents, on perd du temps sur les annonces"
    Output: Liste de 3 Process max, triés par ROI
    """
    secteur = detect_secteur(description)

    if secteur == "autre":
        return [Process(
            nom="Audit personnalisé requis",
            temps_avant_h_semaine=0, temps_apres_h_semaine=0,
            outils=["Boop Call"],
            complexite="moyen",
            roi_12_mois_eur=0,
            template_id="custom",
            description="Cas spécifique. Le boop te propose un call de 15min pour mapper le process."
        )]

    process

