# Chargeur de batterie de véhicule électrique.

## Contexte:
Ceci est un projet d'élève ingénieur visant à concevoir en simulation (Via PSIM) la structure et la commande d'un chargeur pour batteries.

## Sujet:
- Chargeur de batterie du réseau alternatif (230V, 50Hz) vers une batterie en courant continu (Tension Nominale:320V; C=100Ah)
- Première Phase de charge: Courant de sortie constant, la tension de la batterie monte petit à petit
- Seconde phase: Tension de la batterie constante, le courant monte petit à petit


- Mode Balance: ?? (bonus?)
  
## Contraintes (cahier des charges?)
- !temperature (Ri^2)
- ieff prise<12A
- On arrête la charge à Vbat=365V
- Si (Vbat> 370V ou) Vbat<265V on ne recharge pas (refus de charge)
- 
## Solution
### Structure
- Redresseur (pont de Graetz) puis hacheur redresseur
- redresseur (mli) pur abandonné
### Commande
- rapport cyclique calculé pour correspondre à la tension de la batterie (block mli ... avec rapport  calculé depuis Vbat...)
