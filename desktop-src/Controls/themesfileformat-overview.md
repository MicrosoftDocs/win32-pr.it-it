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
# <a name="theme-file-format"></a><span data-ttu-id="80556-105">Formato file tema</span><span class="sxs-lookup"><span data-stu-id="80556-105">Theme File Format</span></span>

<span data-ttu-id="80556-106">In questo documento viene illustrato il formato dei file tema (con estensione Theme).</span><span class="sxs-lookup"><span data-stu-id="80556-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="80556-107">Un file con estensione Theme è un file di testo con estensione ini suddiviso in sezioni, che specificano gli elementi visivi visualizzati in un desktop di Windows.</span><span class="sxs-lookup"><span data-stu-id="80556-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="80556-108">I nomi delle sezioni sono racchiusi tra parentesi quadre ( \[ \] ) nel file ini.</span><span class="sxs-lookup"><span data-stu-id="80556-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="80556-109">Un nuovo formato di file, con estensione themepack, è stato introdotto con Windows 7 per aiutare gli utenti a condividere temi.</span><span class="sxs-lookup"><span data-stu-id="80556-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="80556-110">I temi possono essere selezionati nel pannello di controllo della personalizzazione solo in Windows 7 Home Premium o versione successiva oppure solo in Windows Server 2008 R2 quando il componente desktop è installato.</span><span class="sxs-lookup"><span data-stu-id="80556-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="80556-111">Gli argomenti seguenti sono trattati in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="80556-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="80556-112">Creazione di un file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="80556-113">Descrizione di un file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="80556-114">[\[\]Sezione tema](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="80556-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="80556-115">[\[Sezione colori del pannello di controllo \\ \]](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="80556-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="80556-116">[\[\\Sezione cursori del pannello di controllo \]](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="80556-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="80556-117">[\[Sezione desktop del pannello di controllo \\ \]](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="80556-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="80556-118">[\[\]Sezione slideshow](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="80556-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="80556-119">[\[Sezione metrica \]](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="80556-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="80556-120">[\[Sezione stili di visualizzazione \]](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="80556-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="80556-121">[\[\]Sezioni suoni e \[ AppEvents \] (suoni)](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="80556-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="80556-122">[\[Sezione di avvio \]](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="80556-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="80556-123">[\[\]Sezione MasterThemeSelector](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="80556-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="80556-124">Esempio di un file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="80556-125">Installazione dei file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="80556-126">Pacchetti di tema</span><span class="sxs-lookup"><span data-stu-id="80556-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="80556-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80556-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="80556-128">Creazione di un file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-128">Creating a Theme File</span></span>

<span data-ttu-id="80556-129">Un file con estensione Theme consente di modificare l'aspetto di determinati elementi desktop.</span><span class="sxs-lookup"><span data-stu-id="80556-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="80556-130">È possibile creare o modificare un file con estensione Theme in due modi:</span><span class="sxs-lookup"><span data-stu-id="80556-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="80556-131">Modificare le impostazioni di personalizzazione o visualizzazione nel pannello di controllo e salvare le impostazioni come file con estensione Theme.</span><span class="sxs-lookup"><span data-stu-id="80556-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="80556-132">Per istruzioni, vedere la Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="80556-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="80556-133">Creare manualmente un file con estensione Theme per un livello di controllo maggiore sui dettagli del tema.</span><span class="sxs-lookup"><span data-stu-id="80556-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="80556-134">Per rendere il tema disponibile ad altri utenti, è necessario fornire il file con estensione Theme, nonché i file immagine di sfondo, screen saver e icone.</span><span class="sxs-lookup"><span data-stu-id="80556-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="80556-135">Questa operazione può essere eseguita con un [pacchetto di tema](#theme-packs).</span><span class="sxs-lookup"><span data-stu-id="80556-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="80556-136">Descrizione di un file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-136">Description of a Theme File</span></span>

<span data-ttu-id="80556-137">I file del tema includono una serie di sezioni obbligatorie e facoltative.</span><span class="sxs-lookup"><span data-stu-id="80556-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="80556-138">Di seguito vengono descritte le sezioni dei file con estensione Theme e vengono forniti esempi di come specificare le modifiche per i diversi elementi.</span><span class="sxs-lookup"><span data-stu-id="80556-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="80556-139">\[\]Sezione tema</span><span class="sxs-lookup"><span data-stu-id="80556-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-140">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-140">This section is optional.</span></span> <span data-ttu-id="80556-141">Se questa sezione non è inclusa nel file con estensione Theme, il sistema usa le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="80556-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="80556-142">La \[ sezione del tema \] identifica il nome del tema personalizzato e specifica il logo del marchio e le icone del desktop del tema.</span><span class="sxs-lookup"><span data-stu-id="80556-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="80556-143">La prima parte della \[ sezione del tema \] contiene i due elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="80556-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="80556-144">Elemento</span><span class="sxs-lookup"><span data-stu-id="80556-144">Element</span></span>                                                                                                                    | <span data-ttu-id="80556-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80556-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80556-146">DisplayName = nome</span><span class="sxs-lookup"><span data-stu-id="80556-146">DisplayName=name</span></span><br/> <span data-ttu-id="80556-147">oppure</span><span class="sxs-lookup"><span data-stu-id="80556-147">or</span></span><br/> <span data-ttu-id="80556-148">DisplayName = @module ,-stringId</span><span class="sxs-lookup"><span data-stu-id="80556-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="80556-149">esempio: DisplayName = @themeui.dll ,-2013</span><span class="sxs-lookup"><span data-stu-id="80556-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="80556-150">DisplayName è il nome del tema che verrà visualizzato nel pannello di controllo della personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="80556-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="80556-151">Può essere una stringa o un riferimento a un nome localizzato.</span><span class="sxs-lookup"><span data-stu-id="80556-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="80556-152">Questo campo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80556-152">This field is optional.</span></span> <span data-ttu-id="80556-153">Se non è presente, viene usato il nome file del tema come nome del tema.</span><span class="sxs-lookup"><span data-stu-id="80556-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="80556-154">BrandImage = percorso dell'immagine</span><span class="sxs-lookup"><span data-stu-id="80556-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="80556-155">esempio: BrandImage = c: \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="80556-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="80556-156">**Windows 7 e versioni successive** BrandImage specifica il percorso di un file grafico con marchio incorporato nell'anteprima del tema nel pannello di controllo della personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="80556-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="80556-157">Il grafico icona deve essere un file PNG.</span><span class="sxs-lookup"><span data-stu-id="80556-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="80556-158">Il grafico viene ridimensionato a 80x240 pixel, quindi è consigliabile fornire un'immagine di tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="80556-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="80556-159">La raccolta di temi rispetta le aree trasparenti dell'icona del marchio.</span><span class="sxs-lookup"><span data-stu-id="80556-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="80556-160">Questo campo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="80556-160">This field is optional.</span></span> <span data-ttu-id="80556-161">Se non è presente, non viene visualizzato alcun logo come icona del tema.</span><span class="sxs-lookup"><span data-stu-id="80556-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="80556-162">Il resto della \[ sezione del tema \] specifica le icone personalizzate per le funzionalità desktop, ad esempio computer, documenti, rete e cestino.</span><span class="sxs-lookup"><span data-stu-id="80556-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="80556-163">Se non si specificano icone desktop personalizzate, il desktop Visualizza le icone desktop predefinite del sistema.</span><span class="sxs-lookup"><span data-stu-id="80556-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="80556-164">Di seguito sono riportati due esempi di come un file con estensione Theme imposta l'icona del **computer** .</span><span class="sxs-lookup"><span data-stu-id="80556-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="80556-165">Di seguito sono riportati i valori per le icone desktop predefinite in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80556-165">The following are values for the default desktop icons in Windows 7.</span></span>


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



### <a name="control-panelcolors-section"></a><span data-ttu-id="80556-166">\[Sezione colori del pannello di controllo \\ \]</span><span class="sxs-lookup"><span data-stu-id="80556-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-167">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-167">This section is optional.</span></span> <span data-ttu-id="80556-168">Se questa sezione non è inclusa nel file con estensione Theme, il sistema usa le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="80556-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="80556-169">Se il tema usa lo stile di visualizzazione Aero, è consigliabile evitare di eseguire l'override dei valori predefiniti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="80556-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="80556-170">Il colore degli elementi, ad esempio barre di scorrimento, testo e pulsanti, è personalizzabile.</span><span class="sxs-lookup"><span data-stu-id="80556-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="80556-171">Il file con estensione Theme specifica i valori RGB da modificare per questi elementi.</span><span class="sxs-lookup"><span data-stu-id="80556-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="80556-172">I valori sostituiscono i valori predefiniti dello stile di visualizzazione e vengono usati quando il tema è basato sui temi Windows classico, Windows 7 Basic o Contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="80556-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="80556-173">Di seguito è riportato un esempio di come vengono impostati i colori.</span><span class="sxs-lookup"><span data-stu-id="80556-173">Following is an example of how colors are set.</span></span>


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



### <a name="control-panelcursors-section"></a><span data-ttu-id="80556-174">\[\\Sezione cursori del pannello di controllo \]</span><span class="sxs-lookup"><span data-stu-id="80556-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-175">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-175">This section is optional.</span></span> <span data-ttu-id="80556-176">Se questa sezione non è inclusa nel file con estensione Theme, il sistema usa i cursori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="80556-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="80556-177">Un tema può anche modificare l'aspetto dei cursori.</span><span class="sxs-lookup"><span data-stu-id="80556-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="80556-178">A tale scopo, è possibile creare file con estensione CUR per sostituire i cursori predefiniti di Windows.</span><span class="sxs-lookup"><span data-stu-id="80556-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="80556-179">L'esempio seguente è da un file con estensione Theme che definisce i cursori per un tema denominato *Sports*.</span><span class="sxs-lookup"><span data-stu-id="80556-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


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



### <a name="control-paneldesktop-section"></a><span data-ttu-id="80556-180">\[Sezione desktop del pannello di controllo \\ \]</span><span class="sxs-lookup"><span data-stu-id="80556-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-181">Questa sezione è obbligatoria</span><span class="sxs-lookup"><span data-stu-id="80556-181">This section is required.</span></span> <span data-ttu-id="80556-182">Se non si include questa sezione nel file con estensione Theme, il sistema ignorerà il tema e non visualizzerà il tema nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="80556-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="80556-183">È possibile creare uno sfondo personalizzato per il desktop e specificare un percorso per il file di immagine.</span><span class="sxs-lookup"><span data-stu-id="80556-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="80556-184">Nell'esempio seguente viene illustrato come modificare l'aspetto del desktop.</span><span class="sxs-lookup"><span data-stu-id="80556-184">The following example shows how to modify the desktop appearance.</span></span>


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



### <a name="slideshow-section"></a><span data-ttu-id="80556-185">\[\]Sezione slideshow</span><span class="sxs-lookup"><span data-stu-id="80556-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="80556-186">**Windows 7 e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="80556-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="80556-187">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-187">This section is optional.</span></span> <span data-ttu-id="80556-188">Se non si include questa sezione nel file con estensione Theme, il sistema usa l'immagine di sfondo del desktop specificata nella \[ sezione desktop del pannello di controllo \\ \] .</span><span class="sxs-lookup"><span data-stu-id="80556-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="80556-189">Se si include questa sezione, è necessario specificare qui le impostazioni di presentazione.</span><span class="sxs-lookup"><span data-stu-id="80556-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="80556-190">Lo sfondo del tema può essere una presentazione di immagini archiviate in locale o di immagini gestite da un feed RSS.</span><span class="sxs-lookup"><span data-stu-id="80556-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="80556-191">La \[ \] sezione slideshow del file contiene gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="80556-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80556-192">Attributo</span><span class="sxs-lookup"><span data-stu-id="80556-192">Attribute</span></span></th>
<th><span data-ttu-id="80556-193">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80556-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80556-194">Intervallo = numero di millisecondi</span><span class="sxs-lookup"><span data-stu-id="80556-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="80556-195">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="80556-195">Required.</span></span> <span data-ttu-id="80556-196">Interval è un numero che determina la frequenza con cui lo sfondo cambia.</span><span class="sxs-lookup"><span data-stu-id="80556-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="80556-197">Viene misurata in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="80556-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80556-198">Shuffle = 0 o 1</span><span class="sxs-lookup"><span data-stu-id="80556-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="80556-199">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="80556-199">Required.</span></span> <span data-ttu-id="80556-200">Shuffle indica se lo sfondo viene rimescolato.</span><span class="sxs-lookup"><span data-stu-id="80556-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="80556-201">0 = Disabilitato</span><span class="sxs-lookup"><span data-stu-id="80556-201">0 = Disabled</span></span><br/> <span data-ttu-id="80556-202">1 = Abilitato</span><span class="sxs-lookup"><span data-stu-id="80556-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80556-203">Feed RSS = URL del feed RSS</span><span class="sxs-lookup"><span data-stu-id="80556-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="80556-204">Obbligatorio se ImagesRootPath non è specificato.</span><span class="sxs-lookup"><span data-stu-id="80556-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="80556-205">Feed RSS specifica un feed RSS da usare come presentazione dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="80556-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="80556-206">Per il funzionamento del feed, è necessario fare riferimento a immagini ad alta risoluzione che rispettano lo &quot; standard Enclosures &quot; usato dalla <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">piattaforma RSS di Windows</a>.</span><span class="sxs-lookup"><span data-stu-id="80556-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="80556-207">A causa di questa limitazione, è necessario creare manualmente i file con estensione Theme che includono un feed RSS.</span><span class="sxs-lookup"><span data-stu-id="80556-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="80556-208">Non è possibile specificare sia feed RSS che ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="80556-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80556-209">ImagesRootPath = percorso cartella immagine</span><span class="sxs-lookup"><span data-stu-id="80556-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="80556-210">Obbligatorio se feed RSS non è specificato.</span><span class="sxs-lookup"><span data-stu-id="80556-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="80556-211">ImagesRootPath specifica il percorso di un set di immagini che si desidera utilizzare come presentazione dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="80556-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="80556-212">Le immagini nelle sottocartelle non sono incluse nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="80556-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="80556-213">ImagesRootPath supporta le sostituzioni delle variabili di ambiente nel percorso.</span><span class="sxs-lookup"><span data-stu-id="80556-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="80556-214">Non è possibile specificare sia feed RSS che ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="80556-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80556-215">Elemento<em>N</em>percorso = percorso/i per immagini specifiche</span><span class="sxs-lookup"><span data-stu-id="80556-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="80556-216">Per l'uso con ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="80556-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="80556-217">Elemento<em>N</em>percorso specifica i percorsi di immagini specifiche, in modo che sia possibile limitare la presentazione a determinate immagini anziché tutte le immagini in una cartella.</span><span class="sxs-lookup"><span data-stu-id="80556-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="80556-218">Se non viene specificato alcun percorso, tutte le immagini nel percorso ImagesRootPath vengono usate nella presentazione, incluse le immagini aggiunte dopo la creazione e l'installazione del tema.</span><span class="sxs-lookup"><span data-stu-id="80556-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="80556-219">L'elemento<em>N</em>Path supporta le sostituzioni delle variabili di ambiente nel percorso.</span><span class="sxs-lookup"><span data-stu-id="80556-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="80556-220"><em>N</em> è 0, 1, 2 e così via.</span><span class="sxs-lookup"><span data-stu-id="80556-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="80556-221">Negli esempi seguenti viene illustrato il modo in cui un file con estensione Theme specifica la presentazione per includere un set di immagini archiviate localmente.</span><span class="sxs-lookup"><span data-stu-id="80556-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


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



<span data-ttu-id="80556-222">L'esempio seguente è un modello per un file con estensione Theme che crea una presentazione dello sfondo del desktop usando immagini da un feed RSS.</span><span class="sxs-lookup"><span data-stu-id="80556-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="80556-223">Per personalizzare il modello, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="80556-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="80556-224">Copiare l'esempio seguente e incollarlo in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="80556-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="80556-225">Sostituire {THEMENAME} con il nome che si desidera visualizzare nella raccolta di temi del pannello di controllo della personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="80556-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="80556-226">Sostituire {rssfeedurl} con il percorso completo di un feed RSS compatibile.</span><span class="sxs-lookup"><span data-stu-id="80556-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="80556-227">Salvare le modifiche come file con l'estensione ". Theme".</span><span class="sxs-lookup"><span data-stu-id="80556-227">Save the changes as a file with the ".theme" extension.</span></span>


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



### <a name="metrics-section"></a><span data-ttu-id="80556-228">\[Sezione metrica \]</span><span class="sxs-lookup"><span data-stu-id="80556-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-229">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-229">This section is optional.</span></span> <span data-ttu-id="80556-230">Se non si include questa sezione nel file con estensione Theme, il sistema utilizza le impostazioni predefinite dello stile di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="80556-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="80556-231">È possibile specificare le metriche di sistema in un file con estensione Theme.</span><span class="sxs-lookup"><span data-stu-id="80556-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="80556-232">Le metriche di sistema sono le dimensioni dei vari elementi di visualizzazione, ad esempio lo spessore del bordo della finestra, l'altezza dell'icona o la larghezza della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="80556-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="80556-233">I valori NonclientMetrics e IconMetrics sono strutture binarie definite da NONCLIENTMETRICS e ICONMETRICS in winuser. h.</span><span class="sxs-lookup"><span data-stu-id="80556-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="80556-234">Di seguito è riportato un esempio di come modificare le metriche di sistema.</span><span class="sxs-lookup"><span data-stu-id="80556-234">Following is an example of how to change system metrics.</span></span>


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



### <a name="visual-styles-section"></a><span data-ttu-id="80556-235">\[Sezione stili di visualizzazione \]</span><span class="sxs-lookup"><span data-stu-id="80556-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-236">Questa sezione è obbligatoria</span><span class="sxs-lookup"><span data-stu-id="80556-236">This section is required.</span></span> <span data-ttu-id="80556-237">Se non si include questa sezione nel file con estensione Theme, il sistema ignorerà il tema e non visualizzerà il tema nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="80556-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="80556-238">È possibile fornire informazioni specifiche relative alle dimensioni e al colore degli elementi desktop nei file con estensione MSSTYLES.</span><span class="sxs-lookup"><span data-stu-id="80556-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="80556-239">Le sezioni relative al colore e alle dimensioni dei file con estensione Theme possono essere sostituite dai file con estensione MSSTYLES che consentono di modificare gli elementi del desktop in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="80556-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="80556-240">Questi file sono specificati nella sezione stili di visualizzazione di un file con estensione Theme.</span><span class="sxs-lookup"><span data-stu-id="80556-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="80556-241">Di seguito è riportato un esempio di una sezione degli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="80556-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="80556-242">L'aggiunta di un elemento Path a un file. msstyles è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="80556-243">Se si specifica un percorso, è necessario rimuovere le sezioni relative a metriche e colori dal file con estensione Theme.</span><span class="sxs-lookup"><span data-stu-id="80556-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="80556-244">Quando queste sezioni vengono rimosse, i colori, i tipi di carattere e le dimensioni di un tema provengono dal file con estensione MSSTYLES e corrispondono alla finalità dell'autore. msstyles.</span><span class="sxs-lookup"><span data-stu-id="80556-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="80556-245">Se non si riesce a rimuovere la metrica e le sezioni dei colori possono verificarsi problemi di disegno in Windows o nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="80556-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="80556-246">**Windows Vista/Windows 7:** Quando il percorso punta a Aero. msstyles, è possibile specificare il colore del vetro desiderato, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="80556-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="80556-247">**Windows 7:** Quando il percorso punta a Aero. msstyles, è anche possibile specificare il valore di trasparenza desiderato, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="80556-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="80556-248">Se i valori ColorizationColor e Transparency corrispondono esattamente a un colore di sistema, nel pannello di controllo della personalizzazione viene visualizzato il nome di sistema per il colore.</span><span class="sxs-lookup"><span data-stu-id="80556-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="80556-249">In caso contrario, il colore è denominato "Custom".</span><span class="sxs-lookup"><span data-stu-id="80556-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="80556-250">Di seguito è riportata una sezione di VisualStyles per il tema di base di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80556-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="80556-251">Di seguito viene illustrata una sezione di VisualStyles per il tema classico di Windows.</span><span class="sxs-lookup"><span data-stu-id="80556-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="80556-252">Di seguito viene illustrata una sezione di VisualStyles per un tema nero Contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="80556-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="80556-253">\[\]Sezioni suoni e \[ AppEvents \] (suoni)</span><span class="sxs-lookup"><span data-stu-id="80556-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="80556-254">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-254">This section is optional.</span></span> <span data-ttu-id="80556-255">Se non si include questa sezione nel file con estensione Theme, il sistema utilizza le impostazioni predefinite del suono.</span><span class="sxs-lookup"><span data-stu-id="80556-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="80556-256">L'utente può selezionare l'icona del **suono** nel pannello di controllo per associare i suoni agli eventi che si verificano nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="80556-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="80556-257">Un file WAV, ad esempio, può essere riprodotto all'apertura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80556-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="80556-258">Un file con estensione Theme può specificare i file WAV per sostituire quelli predefiniti.</span><span class="sxs-lookup"><span data-stu-id="80556-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="80556-259">L'esempio seguente illustra come farlo.</span><span class="sxs-lookup"><span data-stu-id="80556-259">The following example shows how to do this.</span></span>


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



<span data-ttu-id="80556-260">**Windows 7 e versioni successive:** È possibile specificare un nome di schema audio anziché elencare ogni suono separatamente.</span><span class="sxs-lookup"><span data-stu-id="80556-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="80556-261">Il valore schemeName specifica il nome dello schema audio o il nome dello schema audio localizzato, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="80556-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="80556-262">\[Sezione di avvio \]</span><span class="sxs-lookup"><span data-stu-id="80556-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-263">**Gli screen saver sono deprecati nell'aggiornamento dell'anniversario di Windows 10 e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="80556-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="80556-264">Questa sezione è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="80556-264">This section is optional.</span></span> <span data-ttu-id="80556-265">Se non si include questa sezione nel file con estensione Theme, non viene usato alcun screen saver.</span><span class="sxs-lookup"><span data-stu-id="80556-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="80556-266">Nel file con estensione Theme è possibile specificare il screen saver per Windows da usare.</span><span class="sxs-lookup"><span data-stu-id="80556-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="80556-267">Nell'esempio riportato di seguito viene illustrata questa situazione.</span><span class="sxs-lookup"><span data-stu-id="80556-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="80556-268">\[\]Sezione MasterThemeSelector</span><span class="sxs-lookup"><span data-stu-id="80556-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="80556-269">Questa sezione è obbligatoria</span><span class="sxs-lookup"><span data-stu-id="80556-269">This section is required.</span></span> <span data-ttu-id="80556-270">Se non si include questa sezione nel file con estensione Theme, il sistema ignorerà il tema e non visualizzerà il tema nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="80556-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="80556-271">La sezione del selettore del tema principale del file. Theme deve essere sempre inclusa come tag che indica che il file è valido.</span><span class="sxs-lookup"><span data-stu-id="80556-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="80556-272">Non è possibile scegliere valori per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="80556-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="80556-273">Di seguito viene illustrato questo.</span><span class="sxs-lookup"><span data-stu-id="80556-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="80556-274">Esempio di un file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-274">Example of a Theme File</span></span>

<span data-ttu-id="80556-275">Nell'esempio seguente viene illustrato un file con estensione Theme completo.</span><span class="sxs-lookup"><span data-stu-id="80556-275">The following example shows a complete .theme file.</span></span>


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



## <a name="installing-theme-files"></a><span data-ttu-id="80556-276">Installazione dei file di tema</span><span class="sxs-lookup"><span data-stu-id="80556-276">Installing Theme Files</span></span>

<span data-ttu-id="80556-277">Quando Windows viene inizializzato, il sistema operativo Enumera le sottodirectory di primo livello delle risorse% WinDir% \\ \\ per identificare i temi disponibili.</span><span class="sxs-lookup"><span data-stu-id="80556-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="80556-278">I file di tema predefiniti del sistema si trovano in% WinDir% \\ \\ temi risorse.</span><span class="sxs-lookup"><span data-stu-id="80556-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="80556-279">I file dei temi utente sono archiviati in% windir% \\ Users \\ <username> \\ AppData \\ Local \\ Microsoft \\ Windows \\ .</span><span class="sxs-lookup"><span data-stu-id="80556-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="80556-280">Un file con estensione Theme contiene associazioni di file. Pertanto, le applicazioni del programma di installazione del tema possono chiamare [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) in un file con estensione Theme per aprire la finestra di **personalizzazione** nel pannello di controllo sul tema specificato.</span><span class="sxs-lookup"><span data-stu-id="80556-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="80556-281">Pacchetti di tema</span><span class="sxs-lookup"><span data-stu-id="80556-281">Theme Packs</span></span>

<span data-ttu-id="80556-282">**Windows 7 e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="80556-282">**Windows 7 and later.**</span></span> <span data-ttu-id="80556-283">Un pacchetto di tema è un file con estensione cab che contiene non solo il file con estensione Theme, ma anche i file necessari per implementare il tema in un altro computer, ad esempio file audio e immagini.</span><span class="sxs-lookup"><span data-stu-id="80556-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="80556-284">Gli utenti possono creare pacchetti di tema tramite il pannello di controllo della personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="80556-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="80556-285">I tipi di file supportati sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="80556-285">Supported file types include the following:</span></span>



| <span data-ttu-id="80556-286">Tipo file</span><span class="sxs-lookup"><span data-stu-id="80556-286">File type</span></span>    | <span data-ttu-id="80556-287">Estensione</span><span class="sxs-lookup"><span data-stu-id="80556-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="80556-288">Tema</span><span class="sxs-lookup"><span data-stu-id="80556-288">Theme</span></span>        | <span data-ttu-id="80556-289">.theme</span><span class="sxs-lookup"><span data-stu-id="80556-289">.theme</span></span>                              |
| <span data-ttu-id="80556-290">Immagine</span><span class="sxs-lookup"><span data-stu-id="80556-290">Image</span></span>        | <span data-ttu-id="80556-291">jpg, JPEG, BMP, DIB, TIF, png</span><span class="sxs-lookup"><span data-stu-id="80556-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="80556-292">Suoni</span><span class="sxs-lookup"><span data-stu-id="80556-292">Sound</span></span>        | <span data-ttu-id="80556-293">.wav</span><span class="sxs-lookup"><span data-stu-id="80556-293">.wav</span></span>                                |
| <span data-ttu-id="80556-294">Cursore del mouse</span><span class="sxs-lookup"><span data-stu-id="80556-294">Mouse cursor</span></span> | <span data-ttu-id="80556-295">. cur,. ani</span><span class="sxs-lookup"><span data-stu-id="80556-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="80556-296">Icona del desktop</span><span class="sxs-lookup"><span data-stu-id="80556-296">Desktop icon</span></span> | <span data-ttu-id="80556-297">ico</span><span class="sxs-lookup"><span data-stu-id="80556-297">.ico</span></span>                                |
| <span data-ttu-id="80556-298">Logo del marchio</span><span class="sxs-lookup"><span data-stu-id="80556-298">Brand logo</span></span>   | <span data-ttu-id="80556-299">png</span><span class="sxs-lookup"><span data-stu-id="80556-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="80556-300">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80556-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80556-301">Panoramica degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="80556-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

