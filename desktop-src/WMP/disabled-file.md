---
title: File disabilitato
description: File disabilitato
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di immagine per le interfacce, file disabilitati
- Windows Media Player Mobile Skins, file disabilitati
- interfacce, file disabilitati
- File disabilitati nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044964"
---
# <a name="disabled-file"></a><span data-ttu-id="77cd6-110">File disabilitato</span><span class="sxs-lookup"><span data-stu-id="77cd6-110">Disabled File</span></span>

<span data-ttu-id="77cd6-111">Il file disabilitato contiene le immagini che verranno visualizzate quando non è possibile usare una funzione di pulsante particolare o lo stato di un pulsante è disattivato.</span><span class="sxs-lookup"><span data-stu-id="77cd6-111">The Disabled file contains the images that will be displayed when a particular button function cannot be used or a button state is off.</span></span> <span data-ttu-id="77cd6-112">Se, ad esempio, viene definita una playlist vuota, i pulsanti **Avanti** e **indietro** verranno visualizzati e devono essere visualizzati usando un'immagine disabilitata.</span><span class="sxs-lookup"><span data-stu-id="77cd6-112">For example, if an empty playlist is defined, the **Next** and **Prev** buttons will be displayed, and they should be displayed using a disabled image.</span></span> <span data-ttu-id="77cd6-113">Inoltre, per i pulsanti di attivazione, l'immagine disabilitata viene utilizzata per indicare che lo stato è disattivato.</span><span class="sxs-lookup"><span data-stu-id="77cd6-113">Also, for toggle buttons, the Disabled image is used to indicate that the state is off.</span></span>

<span data-ttu-id="77cd6-114">L'immagine seguente è un file disabilitato tipico.</span><span class="sxs-lookup"><span data-stu-id="77cd6-114">The following image is a typical Disabled file.</span></span>

![file disabilitato](images/cesdkdis.png)

<span data-ttu-id="77cd6-116">Archivia le immagini per i pulsanti di tipo hit che sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="77cd6-116">This stores the images for hit-type buttons that are disabled.</span></span> <span data-ttu-id="77cd6-117">Le immagini sono simili al file in background, ma i colori sono più chiari.</span><span class="sxs-lookup"><span data-stu-id="77cd6-117">The images are similar to the Background file, but the colors are lighter.</span></span> <span data-ttu-id="77cd6-118">Utilizzando l'offset definito nella sezione bitmap del file di definizione della pelle, le immagini dei pulsanti si allineano con l'immagine del file di sfondo.</span><span class="sxs-lookup"><span data-stu-id="77cd6-118">Using the offset defined in the Bitmaps section of the skin definition file, the button images line up with the Background file image.</span></span>

<span data-ttu-id="77cd6-119">Si noti che lo sfondo dell'immagine del pulsante corrisponde esattamente all'area corrispondente nel file in background.</span><span class="sxs-lookup"><span data-stu-id="77cd6-119">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="77cd6-120">Questo è importante, poiché quando un pulsante di tipo hit non è disponibile, l'intero rettangolo definito per l'immagine disabilitata sostituirà l'area corrispondente nel file in background.</span><span class="sxs-lookup"><span data-stu-id="77cd6-120">This is important, because when a hit-type button is unavailable, the entire rectangle defined for the disabled image will replace the matching area in the Background file.</span></span> <span data-ttu-id="77cd6-121">Mantenere la grafica coerente con l'immagine di sfondo per assicurarsi che solo le parti del pulsante che si desidera visualizzare diverse cambieranno effettivamente.</span><span class="sxs-lookup"><span data-stu-id="77cd6-121">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77cd6-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77cd6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77cd6-123">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="77cd6-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




