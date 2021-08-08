# no\_perimeter\_unsupported\_algo

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Périmètre et enveloppe](../print_settings/print_settings.md#périmètre-et-enveloppe) - [Haladó](../print_settings/print_settings.md#Haladó)
* Mód : Haladó

## Pas de périmètres dans un pont

### Leírás

Option expérimentale pour supprimer les périmètres où il n'y a rien en dessous et où un remplissage ponté devrait être meilleur.

* Retirer les périmètres : supprimez les périmètres non soutenus, laissez la zone de pont en l'état.
* Ne garder que les ponts : supprimez les périmètres dans les zones de pont, ne gardez que les ponts qui se terminent dans une zone pleine.
* Conserver les ponts et les surplombs : supprimez les périmètres non soutenus, ne conservez que les ponts qui se terminent dans une zone pleine, remplissez le reste avec des périmètres de surplomb+ponts.
* Remplir les vides avec des ponts : supprimez les périmètres non soutenus, créer des ponts sur l'ensemble du trou.\* !! Celui-ci peut entraîner des problèmes avec des surplombs en forme de /\, donc vous devriez l'utiliser seulement sur une couche à la fois via le modificateur de hauteur!

**!! Intensif en termes de calcul !!**

[Vissza a változók listájához](variable_list.md)
