---
title: File con privilegi avanzati
description: File con privilegi avanzati
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, file con file con privilegi avanzati
- Windows Media Player Mobile Skins, file con file con privilegi avanzati
- interfacce, file con privilegi avanzati
- File con privilegi avanzati nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298743"
---
# <a name="super-files"></a><span data-ttu-id="d594a-110">File con privilegi avanzati</span><span class="sxs-lookup"><span data-stu-id="d594a-110">Super Files</span></span>

<span data-ttu-id="d594a-111">I file con privilegi avanzati vengono usati per archiviare le immagini disabilitate per trackbars.</span><span class="sxs-lookup"><span data-stu-id="d594a-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="d594a-112">Poiché l'immagine TrackBar principale viene visualizzata nel file in background e l'utente tocca l'immagine Thumb, non l'immagine TrackBar, per trackbars è necessaria solo l'immagine disabilitata.</span><span class="sxs-lookup"><span data-stu-id="d594a-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="d594a-113">Viene archiviato nel file definito da Super nella sezione bitmap del file di definizione dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d594a-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="d594a-114">Un file con privilegi avanzati può archiviare anche le immagini inserite e disabilitate per altri pulsanti, ad esempio mute, che non devono necessariamente essere un pulsante di tipo hit.</span><span class="sxs-lookup"><span data-stu-id="d594a-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="d594a-115">I file Super Art non vengono usati nelle interfacce per Windows Media Player 10 mobile o versioni successive perché le immagini disabilitate per Seek trackbars si trovano nel file seekthumb.</span><span class="sxs-lookup"><span data-stu-id="d594a-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="d594a-116">L'immagine seguente è un file Super tipico.</span><span class="sxs-lookup"><span data-stu-id="d594a-116">The following image is a typical Super file.</span></span>

![file con privilegi avanzati](images/cesdksup.png)

<span data-ttu-id="d594a-118">Consente di archiviare le immagini disabilitate per i TrackBar e il pulsante di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="d594a-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="d594a-119">Queste immagini sono offset in base a quanto definito dalla sezione bitmap.</span><span class="sxs-lookup"><span data-stu-id="d594a-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="d594a-120">L'area di sfondo dell'immagine TrackBar disabilitata corrisponde esattamente all'area corrispondente nel file in background.</span><span class="sxs-lookup"><span data-stu-id="d594a-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="d594a-121">Questo è importante, poiché l'intero rettangolo definito per l'immagine TrackBar disabilitata sostituirà l'area corrispondente nel file in background.</span><span class="sxs-lookup"><span data-stu-id="d594a-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="d594a-122">Ciò garantisce che l'immagine TrackBar disabilitata si mescoli facilmente nell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="d594a-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d594a-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d594a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d594a-124">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="d594a-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




