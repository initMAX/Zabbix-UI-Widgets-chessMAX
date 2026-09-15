<div align="center">

<h1>chessMAX</h1>

<p>Vyvíjí a spravuje <a href="https://www.initmax.cz"><img alt="initMAX" src="./logo/initmax-logo-framed.svg" height="22" valign="middle"></a> a komunita</p>

<p><strong>Zahrajte si šachy přímo na dashboardu Zabbixu.</strong><br>
Vyzvěte Stockfish, pozvěte kolegu nebo hrajte ve dvou u jedné obrazovky. S přehlednými SVG figurkami, nápovědou povolených tahů a volitelnými šachovými hodinami.</p>

<p>
<img src="./badge/zabbix.svg" alt="Zabbix 6.0-7.4">
<img src="./badge/version.svg" alt="Verze uvedená na odznaku">
<img src="./badge/php.svg" alt="PHP 7.4+">
<img src="./badge/free.svg" alt="FREE AGPLv3">
<img src="./badge/gpg.svg" alt="Podepsáno GPG">
</p>

<p><a href="../README.md">English</a> · <a href="#možnosti">Možnosti</a> · <a href="#příklady">Příklady</a> · <a href="#instalace">Instalace</a> · <a href="https://portal.initmax.com/catalog/zabbix-chessmax">Portál</a></p>

<img src="./screen/01-overview.png" width="880" alt="Šachová partie Toma a Jacka ve widgetu chessMAX">
</div>

## Proč chessMAX

Udělejte si šachovou přestávku bez opuštění dashboardu. Aktuální partie zůstane uložená po obnovení stránky i po opětovném přihlášení a synchronizuje se mezi vašimi widgety. Stockfish běží v prohlížeči; tahy ověřuje a ukládá frontend Zabbixu. Fonty, ikony, skripty i šachový engine jsou součástí balíčku. Hra nepotřebuje externí CDN, službu pro fonty ani šachové API.

## Možnosti

<table>
<tr><td width="50%"><b>Hra proti Stockfish</b><br>Čtyři obtížnosti: začátečník, pokročilý, expert a velmistr. Engine je součástí widgetu.</td><td width="50%"><b>Partie s kolegou</b><br>Super admin může pozvat povoleného uživatele Zabbixu. Ten pozvánku přijme nebo odmítne ve svém widgetu.</td></tr>
<tr><td><b>Dva hráči u jedné obrazovky</b><br>Střídejte se na stejné šachovnici. Druhého hráče pojmenujte a podle potřeby otočte hrací plochu.</td><td><b>Časový limit</b><br>Každý hráč má 5, 10 nebo 15 minut. Lze hrát i bez hodin.</td></tr>
<tr><td><b>Nápověda tahů</b><br>Po najetí nebo výběru figurky se zobrazí povolená cílová pole. Vedle šachovnice vidíte sebrané figurky, šach a materiální převahu.</td><td><b>Hra napříč dashboardy</b><br>Aktuální partie je spojená s účtem Zabbixu a je dostupná i v jiných kartách a widgetech.</td></tr>
</table>

## Příklady

<table><tr>
<td width="32%" align="center" valign="top"><img src="./screen/03-portrait.png" alt="Tom a Jack hrají na šachovnici na výšku"><br><small><b>Na výšku</b> - karty hráčů nad a pod šachovnicí</small></td>
<td width="68%" align="center" valign="top"><img src="./screen/02-local.png" alt="Stejná partie Toma a Jacka v širokém widgetu"><br><small><b>Na šířku</b> - šachovnice a karty hráčů vedle sebe</small></td>
</tr></table>

## Nastavení a ovládání

Formulář widgetu obsahuje dvě nastavení: zobrazování nápovědy povolených tahů a výchozí šachové hodiny. V dialogu nové hry vyberete barvu (nebo hod mincí), soupeře, obtížnost a hodiny. Tyto volby platí pro novou partii. Žádné ovládací prvky nejsou placené.

<table><tr>
<td width="50%" align="center" valign="top"><img src="./screen/06-settings.png" alt="Nastavení nápovědy a výchozích hodin"><br><small><b>Nastavení widgetu</b> - nápověda a výchozí hodiny</small></td>
<td width="50%" align="center" valign="top"><img src="./screen/04-new-game.png" alt="Volba barvy, soupeře, obtížnosti a hodin"><br><small><b>Nová hra</b> - vyberte způsob hry</small></td>
</tr></table>

Klikněte na figurku a cílové pole, nebo ji přetáhněte. Při rošádě přesuňte krále na cílové pole nebo na jeho věž. Po příchodu pěšce na poslední řadu vyberte figurku pro proměnu. Klávesnicí se po zaměření widgetu pohybujete šipkami a vybíráte pomocí Enter nebo mezerníku; ovládací prvky dialogů zachovávají běžné klávesové chování.

Každý účet má jednu aktuální partii. Pozvánku smí odeslat pouze Super admin, příjemcem však může být běžný uživatel Zabbixu. Odesílatel uvidí oznámení o odmítnutí. Pro příjem pozvánky musí mít druhý hráč otevřený widget chessMAX. Aktivní šachovnice se obvykle synchronizují každé tři sekundy.

Hra rozpoznává mat, pat a nedostatek materiálu. Opakování pozice a pravidlo 50 tahů vedou automaticky k remíze; jde o zjednodušení pro příležitostné hraní, nikoli turnajový postup pro reklamaci remízy. Po vypršení času je výsledkem remíza, pokud soupeř nemá materiál potřebný k matu. Tato kontrola neřeší všechny možné zablokované pozice a pevnosti. Bezpečnostní limit partie je 600 půltahů (300 celých tahů). Vzdání nebo opuštění aktivní partie ji ukončí.

## Instalace

chessMAX se distribuuje v podepsaných balíčcích deb a rpm; dostupné jsou také archivy se zdrojovým kódem.

**Nejjednodušší postup nabízí [průvodce instalací na portálu](https://portal.initmax.com/catalog/zabbix-chessmax#how-to-install).**

Instalátor deb/rpm nový modul automaticky zaregistruje a povolí. Pokud ho správce dříve zakázal, tento stav zachová. Po instalaci přidejte chessMAX na dashboard. V prostředí s více frontendovými uzly nainstalujte balíček na každý z nich.

Při ruční instalaci ze ZIP postupujte podle souboru **INSTALL.md** v archivu, vyberte adresář odpovídající verzi Zabbixu, nechte načíst adresář modulů v **Administrace > Obecné > Moduly** a chessMAX povolte. Umístění stránky Moduly se může podle verze Zabbixu lišit. Balíčky přepínají odpovídající variantu automaticky při změně verze Zabbixu; u ZIP instalace je nutné při upgradu nebo návratu frontendu postup zopakovat podle přiloženého návodu.

## FREE a PRO

chessMAX je celý zdarma. Nemá PRO edici ani placenou sadu funkcí.

| Funkce | FREE |
|---|:---:|
| Lokalizace do všech 27 podporovaných jazykových katalogů Zabbixu | Ano |
| Připraveno pro vysokou dostupnost | Ano |
| Vestavěný engine se čtyřmi obtížnostmi | Ano |
| Partie s kolegou na jiném dashboardu | Ano |
| Dva hráči u jedné obrazovky | Ano |
| Šachové hodiny | Ano |
| Nápověda povolených tahů | Ano |
| Licence | [AGPLv3](../LICENSE.md) |

## Požadavky

| Požadavek | Podrobnosti |
|---|---|
| Zabbix | 6.0, 6.2, 6.4, 7.0, 7.2 a 7.4; jeden balíček obsahuje obě generace modulů frontendu |
| PHP | 7.4 nebo novější, podle požadavků použité verze Zabbixu |
| Prohlížeč | Moderní prohlížeč s JavaScriptem; pro Stockfish také WebAssembly a Web Workers |
| Operační systém | Podporovaná instalace frontendu Zabbixu na distribuci s balíčky deb nebo rpm |
| Edice | Pouze FREE |
| Jazyky | 27 katalogů: 25 aktuálních jazyků a nizozemština s rumunštinou pro starší Zabbix; widget respektuje jazyk uživatele |
| Vysoká dostupnost | Záznamy partií jsou ve sdílené databázi Zabbixu. chessMAX musí být nainstalovaný na každém frontendovém uzlu. |

## Podpora a odkazy

- [Portál initMAX](https://portal.initmax.com/catalog/zabbix-chessmax) - balíčky a průvodce instalací
- [Dokumentace chessMAX](https://www.initmax.cz/wiki/chessmax/) - instalace, nastavení a příklady
- [Produkt chessMAX](https://www.initmax.cz/produkt/chessmax/) - funkce a stažení zdarma
- Zdrojový kód FREE pod AGPLv3 je v každém balíčku a v [archivu zdrojového kódu](https://repo.initmax.com/zabbix/free/zip/chessmax/)
- [Stockfish](https://stockfishchess.org/) - přibalený engine pod GPLv3; verze a kontrolní součty závislostí uvádí [VENDOR.md](./vendor.md)
- Podpora: [info@initmax.com](mailto:info@initmax.com)

---

FREE: [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.html) · (c) 2021-2026 initMAX s.r.o.
