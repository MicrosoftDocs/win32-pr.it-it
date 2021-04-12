---
title: Bordi per Windows Media Player (deprecato)
description: Bordi per Windows Media Player (deprecato)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Media Player di Windows, bordi
- Interfacce di Media Player Windows, bordi
- interfacce, bordi
- bordi, rispetto alle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329884"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="6bbff-107">Bordi per Windows Media Player (deprecato)</span><span class="sxs-lookup"><span data-stu-id="6bbff-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="6bbff-108">Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="6bbff-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="6bbff-109">Un bordo è simile a un oggetto Skin, ma invece di sostituire l'interfaccia utente per la modalità Compact di Windows Media Player, un bordo è incorporato nel riquadro Now Playing del Media Player Windows in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="6bbff-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="6bbff-110">Utilizzando un pacchetto di download di Windows Media, è possibile includere contenuto con un bordo, aprendo il percorso alle applicazioni multimediali.</span><span class="sxs-lookup"><span data-stu-id="6bbff-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="6bbff-111">Nella directory degli esempi di questo SDK è incluso un pacchetto di download di esempio Windows Media che include un bordo e contenuto incorporato.</span><span class="sxs-lookup"><span data-stu-id="6bbff-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="6bbff-112">Creazione di un bordo</span><span class="sxs-lookup"><span data-stu-id="6bbff-112">Creating a Border</span></span>

<span data-ttu-id="6bbff-113">Un bordo viene creato allo stesso modo di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6bbff-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="6bbff-114">L'unica differenza è che l'interfaccia è incorporata all'interno del riquadro **Now Play** .</span><span class="sxs-lookup"><span data-stu-id="6bbff-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="6bbff-115">Ciò significa che le dimensioni dell'interfaccia non possono essere calcolate e che tutti gli elementi dell'interfaccia devono essere relativi.</span><span class="sxs-lookup"><span data-stu-id="6bbff-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="6bbff-116">Se l'utente ridimensiona Windows Media Player, le parti del bordo potrebbero essere ritagliate e non visualizzate.</span><span class="sxs-lookup"><span data-stu-id="6bbff-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="6bbff-117">Caricamento di un bordo</span><span class="sxs-lookup"><span data-stu-id="6bbff-117">Loading a Border</span></span>

<span data-ttu-id="6bbff-118">Quando viene caricato un metafile di Windows Media che usa l'elemento **Skin** , viene caricato un bordo.</span><span class="sxs-lookup"><span data-stu-id="6bbff-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="6bbff-119">L'attributo **href** dell'elemento **Skin** deve fare riferimento a un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6bbff-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="6bbff-120">Un tipico elemento **Skin** avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="6bbff-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="6bbff-121">Per ulteriori informazioni, vedere [elemento Skin (deprecato)](skin-element--deprecated.md).</span><span class="sxs-lookup"><span data-stu-id="6bbff-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="6bbff-122">Inclusione di contenuto con un bordo</span><span class="sxs-lookup"><span data-stu-id="6bbff-122">Including Content with a Border</span></span>

<span data-ttu-id="6bbff-123">È possibile includere contenuto con un bordo utilizzando un file di download di Windows Media (con estensione di file WMD).</span><span class="sxs-lookup"><span data-stu-id="6bbff-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="6bbff-124">A tale scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="6bbff-124">Follow these steps:</span></span>

1.  <span data-ttu-id="6bbff-125">Creare il bordo.</span><span class="sxs-lookup"><span data-stu-id="6bbff-125">Create the border.</span></span> <span data-ttu-id="6bbff-126">Prestare attenzione a crearlo in modo tale che il ridimensionamento non rovini la composizione del bordo.</span><span class="sxs-lookup"><span data-stu-id="6bbff-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="6bbff-127">Ad esempio, non includere un file in background; rendere trasparente lo sfondo in modo da consentire l'esecuzione di una visualizzazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="6bbff-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="6bbff-128">Comprimere il contenuto dell'interfaccia (file di immagine, file JScript e definizione di interfaccia personalizzata) in un file con estensione WMZ.</span><span class="sxs-lookup"><span data-stu-id="6bbff-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="6bbff-129">Creare un metafile di Windows Media (con estensione asx) che fa riferimento al file di bordo compresso (con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="6bbff-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="6bbff-130">Il metafile può includere le informazioni sulla playlist con metadati per l'arte e gli URL per contenuto specifico.</span><span class="sxs-lookup"><span data-stu-id="6bbff-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="6bbff-131">Assemblare il contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="6bbff-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="6bbff-132">Comprimere il bordo, il metafile e il contenuto in un file e assegnargli un'estensione del nome di file. WMD.</span><span class="sxs-lookup"><span data-stu-id="6bbff-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="6bbff-133">Uso di un bordo</span><span class="sxs-lookup"><span data-stu-id="6bbff-133">Using a Border</span></span>

<span data-ttu-id="6bbff-134">Dopo aver creato il file di download di Windows Media, è sufficiente fare doppio clic su di esso.</span><span class="sxs-lookup"><span data-stu-id="6bbff-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="6bbff-135">Il file verrà scaricato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6bbff-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="6bbff-136">I file all'interno del pacchetto verranno decompressi, la playlist verrà aggiunta alle playlist, il bordo verrà visualizzato nel riquadro **ora riproduzione** del Media Player di Windows in modalità completa e il primo elemento della nuova playlist inizierà a essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="6bbff-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bbff-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bbff-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bbff-138">**Informazioni sulle interfacce**</span><span class="sxs-lookup"><span data-stu-id="6bbff-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="6bbff-139">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="6bbff-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="6bbff-140">**Pacchetti di download di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="6bbff-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




