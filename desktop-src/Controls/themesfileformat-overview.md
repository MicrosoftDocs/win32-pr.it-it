---
title: Formato del file del tema
description: Questo documento illustra il formato dei file di tema (con estensione theme). Un file con estensione theme è un .ini di testo suddiviso in sezioni, che specificano gli elementi visivi visualizzati in un Windows desktop. I nomi delle sezioni sono racchiusi tra parentesi quadre (\ \ ) nel file .ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67fc2d73e54e4f9c319108c2b29ed62fb58266f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472307"
---
# <a name="theme-file-format"></a>Formato del file del tema

Questo documento illustra il formato dei file di tema (con estensione theme). Un file con estensione theme è un .ini di testo suddiviso in sezioni, che specificano gli elementi visivi visualizzati in un Windows desktop. I nomi delle sezioni vengono racchiusi tra parentesi quadre ( \[ \] ) nel file .ini.

Un nuovo formato di file, .themepack, è stato introdotto con Windows 7 per consentire agli utenti di condividere i temi. I temi possono essere selezionati nel Pannello di controllo di personalizzazione solo in Windows 7 Home Premium o versione successiva oppure solo in Windows Server 2008 R2 quando viene installato il componente Desktop.

In questo articolo vengono illustrati gli argomenti seguenti.

-   [Creazione di un file di tema](#creating-a-theme-file)
-   [Descrizione di un file di tema](#description-of-a-theme-file)
    -   [\[Sezione \] Theme](#theme-section)
    -   [\[Pannello di controllo \\ Colors \]](#control-panelcolors-section)
    -   [\[Pannello di controllo \\ cursori \]](#control-panelcursors-section)
    -   [\[Pannello di controllo \\ Desktop \]](#control-paneldesktop-section)
    -   [\[Sezione \] Presentazione](#slideshow-section)
    -   [\[Sezione \] Metriche](#metrics-section)
    -   [\[Sezione Stili di \] visualizzazione](#visual-styles-section)
    -   [\[Sezioni \] Sounds \[ e AppEvents \] (Suoni)](#sounds-and-appevents-sections-sounds)
    -   [\[Sezione \] di avvio](#boot-section)
    -   [\[Sezione MasterThemeSelector \]](#masterthemeselector-section)
-   [Esempio di file di tema](#example-of-a-theme-file)
-   [Installazione dei file dei temi](#installing-theme-files)
-   [Theme Pack](#theme-packs)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-theme-file"></a>Creazione di un file di tema

Un file con estensione theme consente di modificare l'aspetto di determinati elementi del desktop. È possibile creare o modificare un file con estensione theme in due modi:

-   Modificare le impostazioni di personalizzazione o visualizzazione Pannello di controllo e salvare le impostazioni come file con estensione theme. Per istruzioni, Windows guida.
-   Creare manualmente un file con estensione theme per un maggiore livello di controllo sui dettagli del tema.

Per rendere disponibile il tema ad altri utenti, è necessario specificare il file con estensione theme, nonché l'immagine di sfondo, screen saver e le icone. È possibile eseguire questa operazione con un [pacchetto di temi](#theme-packs).

## <a name="description-of-a-theme-file"></a>Descrizione di un file di tema

I file dei temi hanno una serie di sezioni obbligatorie e facoltative. Di seguito vengono descritte le sezioni dei file con estensione theme e vengono forniti esempi di come specificare le modifiche per i diversi elementi.

### <a name="theme-section"></a>\[Sezione \] Theme

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, il sistema usa le impostazioni predefinite.

 

La sezione Tema identifica il nome del tema personalizzato e specifica il logo del marchio del tema e le icone \[ \] del desktop.

La prima parte della \[ sezione Theme contiene i due elementi \] seguenti:



| Elemento                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName=name<br/> oppure<br/> DisplayName= @module ,-stringId<br/> esempio: DisplayName= @themeui.dll ,-2013 | DisplayName è il nome del tema che verrà visualizzato nel campo Personalizzazione Pannello di controllo. Può essere una stringa o un riferimento a un nome localizzato.<br/> Questo campo è facoltativo. Se manca, come nome del tema viene usato il nome del tema.<br/>                                                                                                                                                                                                                                         |
| BrandImage=path to image<br/> esempio: BrandImage=c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 e versioni successive** BrandImage specifica il percorso di un file grafico personalizzato incorporato nell'anteprima del tema nel riquadro di personalizzazione Pannello di controllo.<br/> L'icona deve essere un file PNG. L'immagine viene ridimensionata a 80x240 pixel, quindi è consigliabile fornire un'immagine di tale dimensione. La raccolta di temi rispetta le aree trasparenti dell'icona del marchio.<br/> Questo campo è facoltativo. Se manca, non viene visualizzato alcun logo come icona del tema.<br/> |



 

Il resto della sezione Tema specifica icone personalizzate per le funzionalità desktop, ad esempio \[ \] Computer, Documenti, Rete e Cestino. Se non si specificano icone desktop personalizzate, sul desktop vengono visualizzate le icone del desktop predefinite del sistema.

Di seguito sono riportati due esempi di come un file con estensione theme imposta **l'icona Computer.**


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



Di seguito sono riportati i valori per le icone del desktop predefinite in Windows 7.


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a>\[Pannello di controllo \\ Colors \]

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, il sistema usa le impostazioni predefinite. Se il tema usa lo stile di visualizzazione Blu, è consigliabile evitare di eseguire l'override dei valori predefiniti in questa sezione.

 

Il colore degli elementi, ad esempio barre di scorrimento, testo e pulsanti, è personalizzabile. Il file con estensione theme specifica i valori RGB da modificare per questi elementi. I valori eseguono l'override dei valori predefiniti dello stile di visualizzazione e vengono usati quando il tema è basato su Windows classico, Windows 7 Basic o su Contrasto elevato tema.

Di seguito è riportato un esempio di come vengono impostati i colori.


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a>\[Pannello di controllo \\ cursori \]

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, il sistema usa i cursori predefiniti.

 

Un tema può anche modificare l'aspetto dei cursori. A tale scopo, creare file con estensione cur per sostituire i cursori Windows predefiniti. L'esempio seguente deriva da un file con estensione theme che definisce i cursori per un tema denominato *Sports.*


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a>\[Pannello di controllo \\ Desktop \]

> [!Note]  
> Questa sezione è obbligatoria Se non si include questa sezione nel file con estensione theme, il sistema ignora il tema e non visualizza il tema in Pannello di controllo.

 

È possibile creare uno sfondo del desktop personalizzato e specificare un percorso al file di immagine. Nell'esempio seguente viene illustrato come modificare l'aspetto del desktop.


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a>\[Sezione \] Presentazione

**Windows 7 e versioni successive.**

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, il sistema usa l'immagine di sfondo del desktop specificata nella Pannello di controllo \[ \\ \] Desktop. Se si include questa sezione, è necessario specificare qui le impostazioni della presentazione.

 

Lo sfondo del tema può essere una presentazione di immagini archiviate in locale o di immagini servite da un feed RSS. La \[ sezione Presentazione del file contiene gli attributi \] seguenti:




| Attributo | Descrizione | 
|-----------|-------------|
| Interval=number of milliseconds | Obbligatorio. Interval è un numero che determina la frequenza di modifica dello sfondo. Viene misurato in millisecondi. | 
| Shuffle=0 o 1 | Obbligatorio. Shuffle identifica se lo sfondo è in ordine casuale.<br /> 0 = Disabilitato<br /> 1 = Abilitato<br /> | 
| RSSFeed=URL al feed RSS | Obbligatorio se imagesRootPath non è specificato. RSSFeed specifica un feed RSS da usare come presentazione di sfondo. Per il funzionamento del feed, è necessario fare riferimento a immagini ad alta risoluzione che rispettano lo standard "enclosure" usato dalla Windows <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">RSS.</a> A causa di questa limitazione, i file con estensione theme che includono un feed RSS devono essere creati manualmente. <br /><blockquote>[!Note]<br />Non è possibile specificare sia RSSFeed che ImagesRootPath.</blockquote><br /><br /> | 
| ImagesRootPath=percorso della cartella dell'immagine | Obbligatorio se RSSFeed non è specificato. ImagesRootPath specifica il percorso di un set di immagini da usare come presentazione di sfondo. Le immagini nelle sottocartelle non sono incluse nella presentazione.<br /> ImagesRootPath supporta le sostituzioni delle variabili di ambiente nel percorso.<br /><blockquote>[!Note]<br />Non è possibile specificare sia RSSFeed che ImagesRootPath.</blockquote><br /><br /> | 
| Item<em>N</em>Path=path(s) to specific image(s) | Da usare con ImagesRootPath. <br /> Item N Path (Percorso elemento<em>N)</em>specifica i percorsi di immagini specifiche, in modo che sia possibile limitare la presentazione a immagini specifiche anziché a tutte le immagini in una cartella. Se non viene specificato alcun percorso, tutte le immagini nel percorso ImagesRootPath vengono usate nella presentazione, incluse le immagini aggiunte dopo la creazione e l'installazione del tema.<br /> Il<em>percorso dell'elemento N</em>supporta le sostituzioni delle variabili di ambiente nel percorso. <em>N</em> è 0, 1, 2 e così via. <br /> | 




 

Gli esempi seguenti illustrano come un file con estensione theme specifica la presentazione per includere un set di immagini archiviate in locale.


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



L'esempio seguente è un modello per un file con estensione theme che crea una presentazione di sfondo del desktop usando le immagini di un feed RSS. Seguire questa procedura per personalizzare il modello:

1.  Copiare l'esempio seguente e incollarlo in un editor di testo.
2.  Sostituire {themename} con il nome che si vuole visualizzare nella raccolta Di Pannello di controllo temi.
3.  Sostituire {rssfeedurl} con il percorso completo di un feed RSS compatibile.
4.  Salvare le modifiche come file con l'estensione "theme".


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a>\[Sezione \] Metriche

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, il sistema usa le impostazioni predefinite dello stile di visualizzazione.

 

È possibile specificare le metriche di sistema in un file con estensione theme. Le metriche di sistema sono le dimensioni di vari elementi di visualizzazione, ad esempio la larghezza del bordo della finestra, l'altezza dell'icona o la larghezza della barra di scorrimento. I valori NonclientMetrics e IconMetrics sono strutture binarie definite da NONCLIENTMETRICS e ICONMETRICS in winuser.h. Di seguito è riportato un esempio di come modificare le metriche di sistema.


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a>\[Sezione Stili di \] visualizzazione

> [!Note]  
> Questa sezione è obbligatoria Se non si include questa sezione nel file con estensione theme, il sistema ignora il tema e non visualizza il tema in Pannello di controllo.

 

È possibile fornire informazioni specifiche relative alle dimensioni e al colore degli elementi del desktop nei file con estensione msstyles. Le sezioni relative al colore e alle dimensioni dei file con estensione theme possono essere sostituite da file con estensione msstyles che consentono di modificare gli elementi del desktop in modo più dettagliato. Questi file vengono specificati nella sezione degli stili di visualizzazione di un file con estensione theme. Di seguito è riportato un esempio di sezione relativa agli stili di visualizzazione.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



L'aggiunta di un elemento Path a un file con estensione msstyles è facoltativa. Se si specifica un percorso, è necessario rimuovere le sezioni relative alle metriche e ai colori dal file con estensione theme. Quando queste sezioni vengono rimosse, i colori, i tipi di carattere e le dimensioni di un tema provengono dal file con estensione msstyles e corrispondono alla finalità dell'autore .msstyles. Se non si rimuovono le sezioni relative alle metriche e ai colori, Windows o alle applicazioni possono verificarsi problemi di disegno.

**Windows Vista/Windows 7:** Quando il percorso punta a Aero.msstyles, è possibile specificare il Colore cristallo desiderato, come illustrato nell'esempio seguente.

**Windows 7:** Quando il percorso punta a Alfa.msstyles, è anche possibile specificare il valore di Trasparenza desiderato, come illustrato nell'esempio seguente.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Se i valori ColorizationColor e Transparency corrispondono esattamente a un colore di sistema, il Pannello di controllo personalizzazione visualizza il nome del sistema per il colore. In caso contrario, il colore viene etichettato come "Personalizzato".

Di seguito viene illustrata una sezione VisualStyles per il tema Windows 7 Basic.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



Di seguito è illustrata una sezione VisualStyles per il Windows classico.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



Di seguito viene illustrata una sezione VisualStyles per un Contrasto elevato nero.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[Sezioni \] Sounds \[ e AppEvents \] (Suoni)

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, il sistema usa le impostazioni audio predefinite.

 

L'utente può selezionare **l'icona** Suono Pannello di controllo per associare i suoni agli eventi che si verificano nelle applicazioni. Ad esempio, un file wav può essere riprodotto all'apertura di un'applicazione. Un file con estensione theme può specificare file wav per sostituire quelli predefiniti. L'esempio seguente illustra come farlo.


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



**Windows 7 e versioni successive:** È possibile specificare un nome di schema audio anziché elencare separatamente ogni suono.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



Il valore SchemeName specifica il nome dello schema audio o il nome della combinazione audio localizzata, come illustrato nell'esempio precedente.

### <a name="boot-section"></a>\[Sezione \] di avvio

> [!Note]  
> **Gli screen saver sono deprecati nell'aggiornamento Windows 10'anniversario e oltre.**

 

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione theme, non screen saver viene usata alcuna sezione.

 

Nel file con estensione theme è possibile specificare la screen saver da Windows da usare. Nell'esempio riportato di seguito viene illustrata questa situazione.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[Sezione MasterThemeSelector \]

> [!Note]  
> Questa sezione è obbligatoria Se non si include questa sezione nel file con estensione theme, il sistema ignora il tema e non visualizza il tema in Pannello di controllo.

 

La sezione del selettore del tema master del file con estensione theme deve essere sempre inclusa come tag che indica che il file è valido. Non è possibile scegliere i valori per questo parametro. Di seguito viene illustrato questo.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Esempio di file di tema

L'esempio seguente mostra un file con estensione theme completo.


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a>Installazione dei file dei temi

Quando Windows viene inizializzata, il sistema operativo enumera le sottodirectory di primo livello di %WinDir% Resources per identificare \\ \\ i temi disponibili. I file dei temi predefiniti del sistema si trovano in %WinDir% \\ Resources \\ Themes. I file dei temi utente vengono archiviati in %WinDir% \\ Users \\ <username> \\ AppData \\ Local Microsoft Windows \\ \\ \\ Themes.

Un file con estensione theme ha associazioni di file. Pertanto, le applicazioni del programma di installazione dei temi  possono chiamare [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) in un file con estensione theme per aprire la finestra Personalizzazione Pannello di controllo al tema specificato.

## <a name="theme-packs"></a>Theme Pack

**Windows 7 e versioni successive.** Un pacchetto di temi è un file .cab che contiene non solo il file con estensione theme, ma anche i file necessari per implementare il tema in un altro computer, ad esempio file audio e immagini. Gli utenti possono creare pacchetti di temi tramite l'Pannello di controllo.

I tipi di file supportati includono:



| Tipo file    | Estensione                           |
|--------------|-------------------------------------|
| Tema        | .theme                              |
| Immagine        | .jpg, jpeg, .bmp, dib, tif, .png |
| Suoni        | .wav                                |
| Cursore del mouse | .cur, .ani                          |
| Icona del desktop | ico                                |
| Logo del marchio   | png                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica degli stili di visualizzazione](visual-styles-overview.md)
</dt> </dl>

