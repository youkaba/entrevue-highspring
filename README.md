# Book Rental SAAS!

l'application Book rental est une application de location de livres. Elle permet de gérer les livres, les clients, les locations et les retours.
la location est confirmée par un email envoyé au client.

## Cas d'usage : Location de livre

Ce projet implémente un système simple de location de livres avec un cas d'usage principal :

### 📚 "Louer un livre" doit etre realise en full clean architecture et TDD

**Acteur** : Un locataire (Renter)  
**Objectif** : Louer un livre disponible

#### Règles métier
- ✅ Le locataire doit avoir l'âge minimum requis par le livre
- ✅ Le livre doit être disponible (pas déjà loué)
- ✅ Une fois loué, le livre devient indisponible
#### Scénarios
1. **Succès** : Locataire éligible + livre disponible → Location créée
2. **Échec** : Locataire trop jeune → `TooYoungForRentalException`
3. **Échec** : Livre déjà loué → `BookNotAvailableException`
