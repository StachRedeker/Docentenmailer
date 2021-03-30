# De Docentenmailer
> De Docentenmailer is een simpele website gemaakt voor iedereen die te lui is om de mailadressen van docenten van het Erasmus College te Zoetermeer op te zoeken in het informatieboekje.

### Kernpunten

* Werkt alleen bij docenten van het Erasmus College.
* Mijn website zal je automatisch doorsturen naar jouw favoriete e-mailprogramma.
* Ik kan niet meelezen met wat je typt.
* En ik kan ook niet zien wie je bent.
* Alle informatie is gevonden in het informatieboekje.
* Tot slot: de broncode is openbaar; je kunt mij altijd controleren ;)

## Hoe werkt het

Het 'programma' is een simpel HTML-formulier dat gebruik maakt van `mailto`-links.
De eerste regel zorgt dat de imput van het formulierveld (variable `mail`) tussen `mailto:` en `@erasmuscollege.nl` wordt geplaatst:
```
<form onsubmit="window.location = 'mailto:' + mail.value + '@erasmuscollege.nl'; return false;">
```
Vervolgens wordt de variable `mail` gemaakt en gelinkt aan het formulierveld:
```
<input list="mail" name="mail" value="">
```
Dan wordt een dataset gemaakt. De dataset bestaat uit de namen en bijbehorende e-mailadressen (zonder `@erasmuscollege.nl`) van alle docenten:
```
<datalist id="mail">
  <option value="eerste mailpersoon">Eerste</option>
  <option value="tweede mailpersoon">Tweede</option>
  ...
  ...
  ...
</datalist>
```
En tot slot krijgt het formulier ook nog een verzendknop:
```
  <input type="submit" value="Mail!">
</form>
```

## Hoe te gebruiken

De website vind je, zolang ik besluit deze te hosten, [hier](https://vault.stachredeker.nl/docent/). Begin met het typen van de achternaam van een docent in het formulierveld en de rest gaat vanzelf!

## Updates

Ik ben niet van plan dit programma verder te gaan ontwikkelen of de lijst met e-mailadressen bij te werken. De lijst met e-mailadressen is voor het laatst bijgewerkt in 2019.
