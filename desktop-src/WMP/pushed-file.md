---
title: File con push
description: File con push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, file con push
- Windows Media Player Mobile Skins, file con push
- interfacce, file con push
- Push dei file nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396150"
---
# <a name="pushed-file"></a><span data-ttu-id="5db64-110">File con push</span><span class="sxs-lookup"><span data-stu-id="5db64-110">Pushed File</span></span>

<span data-ttu-id="5db64-111">Il file inserito contiene le immagini che verranno visualizzate quando l'utente tocca un pulsante.</span><span class="sxs-lookup"><span data-stu-id="5db64-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="5db64-112">È anche possibile includere le immagini normale e push per lo stato di sospensione del pulsante come playpause.</span><span class="sxs-lookup"><span data-stu-id="5db64-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="5db64-113">L'immagine seguente è un file di cui è stato eseguito il push tipico.</span><span class="sxs-lookup"><span data-stu-id="5db64-113">The following image is a typical Pushed file.</span></span>

![file con push](images/cesdkpus.png)

<span data-ttu-id="5db64-115">Archivia le immagini che verranno visualizzate quando si toccano i pulsanti di tipo hit.</span><span class="sxs-lookup"><span data-stu-id="5db64-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="5db64-116">Inoltre, archiviate in questo file sono le immagini normali e push per l'immagine sospesa del pulsante come playpause.</span><span class="sxs-lookup"><span data-stu-id="5db64-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="5db64-117">Ad eccezione delle immagini secondarie di come playpause a destra, le altre immagini dei pulsanti si allineano con l'immagine di sfondo, usando l'offset definito nella sezione bitmap del file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="5db64-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="5db64-118">Si noti che lo sfondo dell'immagine del pulsante corrisponde esattamente all'area corrispondente nel file in background.</span><span class="sxs-lookup"><span data-stu-id="5db64-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="5db64-119">Questo è importante perché quando l'utente tocca un pulsante di tipo hit, l'intero rettangolo definito per l'immagine push sostituisce l'area corrispondente nel file in background.</span><span class="sxs-lookup"><span data-stu-id="5db64-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="5db64-120">Mantenere la grafica coerente con l'immagine di sfondo per assicurarsi che solo le parti del pulsante che si desidera visualizzare diverse cambieranno effettivamente.</span><span class="sxs-lookup"><span data-stu-id="5db64-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5db64-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5db64-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5db64-122">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="5db64-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




