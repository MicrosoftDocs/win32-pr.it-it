---
title: Formato file tema
description: In questo documento viene illustrato il formato dei file tema (con estensione Theme). Un file con estensione Theme è un file di testo con estensione ini suddiviso in sezioni, che specificano gli elementi visivi visualizzati in un desktop di Windows. I nomi delle sezioni sono racchiusi tra parentesi quadre (\ \) nel file ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "103873081"
---
# <a name="theme-file-format"></a>Formato file tema

In questo documento viene illustrato il formato dei file tema (con estensione Theme). Un file con estensione Theme è un file di testo con estensione ini suddiviso in sezioni, che specificano gli elementi visivi visualizzati in un desktop di Windows. I nomi delle sezioni sono racchiusi tra parentesi quadre ( \[ \] ) nel file ini.

Un nuovo formato di file, con estensione themepack, è stato introdotto con Windows 7 per aiutare gli utenti a condividere temi. I temi possono essere selezionati nel pannello di controllo della personalizzazione solo in Windows 7 Home Premium o versione successiva oppure solo in Windows Server 2008 R2 quando il componente desktop è installato.

Gli argomenti seguenti sono trattati in questo articolo.

-   [Creazione di un file di tema](#creating-a-theme-file)
-   [Descrizione di un file di tema](#description-of-a-theme-file)
    -   [\[\]Sezione tema](#theme-section)
    -   [\[Sezione colori del pannello di controllo \\ \]](#control-panelcolors-section)
    -   [\[\\Sezione cursori del pannello di controllo \]](#control-panelcursors-section)
    -   [\[Sezione desktop del pannello di controllo \\ \]](#control-paneldesktop-section)
    -   [\[\]Sezione slideshow](#slideshow-section)
    -   [\[Sezione metrica \]](#metrics-section)
    -   [\[Sezione stili di visualizzazione \]](#visual-styles-section)
    -   [\[\]Sezioni suoni e \[ AppEvents \] (suoni)](#sounds-and-appevents-sections-sounds)
    -   [\[Sezione di avvio \]](#boot-section)
    -   [\[\]Sezione MasterThemeSelector](#masterthemeselector-section)
-   [Esempio di un file di tema](#example-of-a-theme-file)
-   [Installazione dei file di tema](#installing-theme-files)
-   [Pacchetti di tema](#theme-packs)
-   [Argomenti correlati](#related-topics)

## <a name="creating-a-theme-file"></a>Creazione di un file di tema

Un file con estensione Theme consente di modificare l'aspetto di determinati elementi desktop. È possibile creare o modificare un file con estensione Theme in due modi:

-   Modificare le impostazioni di personalizzazione o visualizzazione nel pannello di controllo e salvare le impostazioni come file con estensione Theme. Per istruzioni, vedere la Guida di Windows.
-   Creare manualmente un file con estensione Theme per un livello di controllo maggiore sui dettagli del tema.

Per rendere il tema disponibile ad altri utenti, è necessario fornire il file con estensione Theme, nonché i file immagine di sfondo, screen saver e icone. Questa operazione può essere eseguita con un [pacchetto di tema](#theme-packs).

## <a name="description-of-a-theme-file"></a>Descrizione di un file di tema

I file del tema includono una serie di sezioni obbligatorie e facoltative. Di seguito vengono descritte le sezioni dei file con estensione Theme e vengono forniti esempi di come specificare le modifiche per i diversi elementi.

### <a name="theme-section"></a>\[\]Sezione tema

> [!Note]  
> Questa sezione è facoltativa. Se questa sezione non è inclusa nel file con estensione Theme, il sistema usa le impostazioni predefinite.

 

La \[ sezione del tema \] identifica il nome del tema personalizzato e specifica il logo del marchio e le icone del desktop del tema.

La prima parte della \[ sezione del tema \] contiene i due elementi seguenti:



| Elemento                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName = nome<br/> oppure<br/> DisplayName = @module ,-stringId<br/> esempio: DisplayName = @themeui.dll ,-2013 | DisplayName è il nome del tema che verrà visualizzato nel pannello di controllo della personalizzazione. Può essere una stringa o un riferimento a un nome localizzato.<br/> Questo campo è facoltativo. Se non è presente, viene usato il nome file del tema come nome del tema.<br/>                                                                                                                                                                                                                                         |
| BrandImage = percorso dell'immagine<br/> esempio: BrandImage = c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 e versioni successive** BrandImage specifica il percorso di un file grafico con marchio incorporato nell'anteprima del tema nel pannello di controllo della personalizzazione.<br/> Il grafico icona deve essere un file PNG. Il grafico viene ridimensionato a 80x240 pixel, quindi è consigliabile fornire un'immagine di tale dimensione. La raccolta di temi rispetta le aree trasparenti dell'icona del marchio.<br/> Questo campo è facoltativo. Se non è presente, non viene visualizzato alcun logo come icona del tema.<br/> |



 

Il resto della \[ sezione del tema \] specifica le icone personalizzate per le funzionalità desktop, ad esempio computer, documenti, rete e cestino. Se non si specificano icone desktop personalizzate, il desktop Visualizza le icone desktop predefinite del sistema.

Di seguito sono riportati due esempi di come un file con estensione Theme imposta l'icona del **computer** .


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



Di seguito sono riportati i valori per le icone desktop predefinite in Windows 7.


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



### <a name="control-panelcolors-section"></a>\[Sezione colori del pannello di controllo \\ \]

> [!Note]  
> Questa sezione è facoltativa. Se questa sezione non è inclusa nel file con estensione Theme, il sistema usa le impostazioni predefinite. Se il tema usa lo stile di visualizzazione Aero, è consigliabile evitare di eseguire l'override dei valori predefiniti in questa sezione.

 

Il colore degli elementi, ad esempio barre di scorrimento, testo e pulsanti, è personalizzabile. Il file con estensione Theme specifica i valori RGB da modificare per questi elementi. I valori sostituiscono i valori predefiniti dello stile di visualizzazione e vengono usati quando il tema è basato sui temi Windows classico, Windows 7 Basic o Contrasto elevato.

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



### <a name="control-panelcursors-section"></a>\[\\Sezione cursori del pannello di controllo \]

> [!Note]  
> Questa sezione è facoltativa. Se questa sezione non è inclusa nel file con estensione Theme, il sistema usa i cursori predefiniti.

 

Un tema può anche modificare l'aspetto dei cursori. A tale scopo, è possibile creare file con estensione CUR per sostituire i cursori predefiniti di Windows. L'esempio seguente è da un file con estensione Theme che definisce i cursori per un tema denominato *Sports*.


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



### <a name="control-paneldesktop-section"></a>\[Sezione desktop del pannello di controllo \\ \]

> [!Note]  
> Questa sezione è obbligatoria Se non si include questa sezione nel file con estensione Theme, il sistema ignorerà il tema e non visualizzerà il tema nel pannello di controllo.

 

È possibile creare uno sfondo personalizzato per il desktop e specificare un percorso per il file di immagine. Nell'esempio seguente viene illustrato come modificare l'aspetto del desktop.


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



### <a name="slideshow-section"></a>\[\]Sezione slideshow

**Windows 7 e versioni successive.**

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione Theme, il sistema usa l'immagine di sfondo del desktop specificata nella \[ sezione desktop del pannello di controllo \\ \] . Se si include questa sezione, è necessario specificare qui le impostazioni di presentazione.

 

Lo sfondo del tema può essere una presentazione di immagini archiviate in locale o di immagini gestite da un feed RSS. La \[ \] sezione slideshow del file contiene gli attributi seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Intervallo = numero di millisecondi</td>
<td>Obbligatorio. Interval è un numero che determina la frequenza con cui lo sfondo cambia. Viene misurata in millisecondi.</td>
</tr>
<tr class="even">
<td>Shuffle = 0 o 1</td>
<td>Obbligatorio. Shuffle indica se lo sfondo viene rimescolato.<br/> 0 = Disabilitato<br/> 1 = Abilitato<br/></td>
</tr>
<tr class="odd">
<td>Feed RSS = URL del feed RSS</td>
<td>Obbligatorio se ImagesRootPath non è specificato. Feed RSS specifica un feed RSS da usare come presentazione dello sfondo. Per il funzionamento del feed, è necessario fare riferimento a immagini ad alta risoluzione che rispettano lo &quot; standard Enclosures &quot; usato dalla <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">piattaforma RSS di Windows</a>. A causa di questa limitazione, è necessario creare manualmente i file con estensione Theme che includono un feed RSS. <br/>
<blockquote>
[!Note]<br />
Non è possibile specificare sia feed RSS che ImagesRootPath.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>ImagesRootPath = percorso cartella immagine</td>
<td>Obbligatorio se feed RSS non è specificato. ImagesRootPath specifica il percorso di un set di immagini che si desidera utilizzare come presentazione dello sfondo. Le immagini nelle sottocartelle non sono incluse nella presentazione.<br/> ImagesRootPath supporta le sostituzioni delle variabili di ambiente nel percorso.<br/>
<blockquote>
[!Note]<br />
Non è possibile specificare sia feed RSS che ImagesRootPath.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Elemento<em>N</em>percorso = percorso/i per immagini specifiche</td>
<td>Per l'uso con ImagesRootPath. <br/> Elemento<em>N</em>percorso specifica i percorsi di immagini specifiche, in modo che sia possibile limitare la presentazione a determinate immagini anziché tutte le immagini in una cartella. Se non viene specificato alcun percorso, tutte le immagini nel percorso ImagesRootPath vengono usate nella presentazione, incluse le immagini aggiunte dopo la creazione e l'installazione del tema.<br/> L'elemento<em>N</em>Path supporta le sostituzioni delle variabili di ambiente nel percorso. <em>N</em> è 0, 1, 2 e così via. <br/></td>
</tr>
</tbody>
</table>



 

Negli esempi seguenti viene illustrato il modo in cui un file con estensione Theme specifica la presentazione per includere un set di immagini archiviate localmente.


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



L'esempio seguente è un modello per un file con estensione Theme che crea una presentazione dello sfondo del desktop usando immagini da un feed RSS. Per personalizzare il modello, attenersi alla procedura seguente:

1.  Copiare l'esempio seguente e incollarlo in un editor di testo.
2.  Sostituire {THEMENAME} con il nome che si desidera visualizzare nella raccolta di temi del pannello di controllo della personalizzazione.
3.  Sostituire {rssfeedurl} con il percorso completo di un feed RSS compatibile.
4.  Salvare le modifiche come file con l'estensione ". Theme".


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



### <a name="metrics-section"></a>\[Sezione metrica \]

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione Theme, il sistema utilizza le impostazioni predefinite dello stile di visualizzazione.

 

È possibile specificare le metriche di sistema in un file con estensione Theme. Le metriche di sistema sono le dimensioni dei vari elementi di visualizzazione, ad esempio lo spessore del bordo della finestra, l'altezza dell'icona o la larghezza della barra di scorrimento. I valori NonclientMetrics e IconMetrics sono strutture binarie definite da NONCLIENTMETRICS e ICONMETRICS in winuser. h. Di seguito è riportato un esempio di come modificare le metriche di sistema.


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



### <a name="visual-styles-section"></a>\[Sezione stili di visualizzazione \]

> [!Note]  
> Questa sezione è obbligatoria Se non si include questa sezione nel file con estensione Theme, il sistema ignorerà il tema e non visualizzerà il tema nel pannello di controllo.

 

È possibile fornire informazioni specifiche relative alle dimensioni e al colore degli elementi desktop nei file con estensione MSSTYLES. Le sezioni relative al colore e alle dimensioni dei file con estensione Theme possono essere sostituite dai file con estensione MSSTYLES che consentono di modificare gli elementi del desktop in modo più dettagliato. Questi file sono specificati nella sezione stili di visualizzazione di un file con estensione Theme. Di seguito è riportato un esempio di una sezione degli stili di visualizzazione.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



L'aggiunta di un elemento Path a un file. msstyles è facoltativa. Se si specifica un percorso, è necessario rimuovere le sezioni relative a metriche e colori dal file con estensione Theme. Quando queste sezioni vengono rimosse, i colori, i tipi di carattere e le dimensioni di un tema provengono dal file con estensione MSSTYLES e corrispondono alla finalità dell'autore. msstyles. Se non si riesce a rimuovere la metrica e le sezioni dei colori possono verificarsi problemi di disegno in Windows o nelle applicazioni.

**Windows Vista/Windows 7:** Quando il percorso punta a Aero. msstyles, è possibile specificare il colore del vetro desiderato, come illustrato nell'esempio seguente.

**Windows 7:** Quando il percorso punta a Aero. msstyles, è anche possibile specificare il valore di trasparenza desiderato, come illustrato nell'esempio seguente.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Se i valori ColorizationColor e Transparency corrispondono esattamente a un colore di sistema, nel pannello di controllo della personalizzazione viene visualizzato il nome di sistema per il colore. In caso contrario, il colore è denominato "Custom".

Di seguito è riportata una sezione di VisualStyles per il tema di base di Windows 7.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



Di seguito viene illustrata una sezione di VisualStyles per il tema classico di Windows.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



Di seguito viene illustrata una sezione di VisualStyles per un tema nero Contrasto elevato.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[\]Sezioni suoni e \[ AppEvents \] (suoni)

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione Theme, il sistema utilizza le impostazioni predefinite del suono.

 

L'utente può selezionare l'icona del **suono** nel pannello di controllo per associare i suoni agli eventi che si verificano nelle applicazioni. Un file WAV, ad esempio, può essere riprodotto all'apertura di un'applicazione. Un file con estensione Theme può specificare i file WAV per sostituire quelli predefiniti. L'esempio seguente illustra come farlo.


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



**Windows 7 e versioni successive:** È possibile specificare un nome di schema audio anziché elencare ogni suono separatamente.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



Il valore schemeName specifica il nome dello schema audio o il nome dello schema audio localizzato, come illustrato nell'esempio precedente.

### <a name="boot-section"></a>\[Sezione di avvio \]

> [!Note]  
> **Gli screen saver sono deprecati nell'aggiornamento dell'anniversario di Windows 10 e versioni successive.**

 

> [!Note]  
> Questa sezione è facoltativa. Se non si include questa sezione nel file con estensione Theme, non viene usato alcun screen saver.

 

Nel file con estensione Theme è possibile specificare il screen saver per Windows da usare. Nell'esempio riportato di seguito viene illustrata questa situazione.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[\]Sezione MasterThemeSelector

> [!Note]  
> Questa sezione è obbligatoria Se non si include questa sezione nel file con estensione Theme, il sistema ignorerà il tema e non visualizzerà il tema nel pannello di controllo.

 

La sezione del selettore del tema principale del file. Theme deve essere sempre inclusa come tag che indica che il file è valido. Non è possibile scegliere valori per questo parametro. Di seguito viene illustrato questo.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Esempio di un file di tema

Nell'esempio seguente viene illustrato un file con estensione Theme completo.


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



## <a name="installing-theme-files"></a>Installazione dei file di tema

Quando Windows viene inizializzato, il sistema operativo Enumera le sottodirectory di primo livello delle risorse% WinDir% \\ \\ per identificare i temi disponibili. I file di tema predefiniti del sistema si trovano in% WinDir% \\ \\ temi risorse. I file dei temi utente sono archiviati in% windir% \\ Users \\ <username> \\ AppData \\ Local \\ Microsoft \\ Windows \\ .

Un file con estensione Theme contiene associazioni di file. Pertanto, le applicazioni del programma di installazione del tema possono chiamare [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) in un file con estensione Theme per aprire la finestra di **personalizzazione** nel pannello di controllo sul tema specificato.

## <a name="theme-packs"></a>Pacchetti di tema

**Windows 7 e versioni successive.** Un pacchetto di tema è un file con estensione cab che contiene non solo il file con estensione Theme, ma anche i file necessari per implementare il tema in un altro computer, ad esempio file audio e immagini. Gli utenti possono creare pacchetti di tema tramite il pannello di controllo della personalizzazione.

I tipi di file supportati sono i seguenti:



| Tipo file    | Estensione                           |
|--------------|-------------------------------------|
| Tema        | .theme                              |
| Immagine        | jpg, JPEG, BMP, DIB, TIF, png |
| Suoni        | .wav                                |
| Cursore del mouse | . cur,. ani                          |
| Icona del desktop | ico                                |
| Logo del marchio   | png                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica degli stili di visualizzazione](visual-styles-overview.md)
</dt> </dl>

