---
title: File di area
description: File di area
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di immagine per le interfacce, i file di area
- Interfacce di Windows Media Player Mobile, file di area
- interfacce, file di area
- File di area in interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332111"
---
# <a name="region-files"></a><span data-ttu-id="758ac-110">File di area</span><span class="sxs-lookup"><span data-stu-id="758ac-110">Region Files</span></span>

<span data-ttu-id="758ac-111">I file di area sono necessari se si usa qualsiasi tipo di pulsante di hit (2PushHit, PushHit o ToggleHit).</span><span class="sxs-lookup"><span data-stu-id="758ac-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="758ac-112">I file di area vengono usati per definire aree che risponderanno a un tocco, noto anche come hit, su un pulsante specifico.</span><span class="sxs-lookup"><span data-stu-id="758ac-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="758ac-113">Per ogni pulsante hit, a un'area nella bitmap dell'area viene assegnato un colore Web specifico, ad esempio \# FF0000, che rappresenta il valore di rosso a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="758ac-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="758ac-114">Il numero di colore viene specificato nella definizione del pulsante Region.</span><span class="sxs-lookup"><span data-stu-id="758ac-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="758ac-115">Quando l'utente Visualizza l'interfaccia, l'immagine del pulsante viene sovrapposta allo sfondo usando le coordinate dell'area nella bitmap della regione.</span><span class="sxs-lookup"><span data-stu-id="758ac-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="758ac-116">Ad esempio, è possibile creare un cerchio rosso in una posizione corrispondente alla posizione del pulsante Avanti e colorarlo a tinta unita rossa ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="758ac-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="758ac-117">Nella definizione del pulsante è quindi possibile assegnare un valore RGB raggiunto di 255, 0, 0, ovvero l'equivalente RGB di \# ff0000.</span><span class="sxs-lookup"><span data-stu-id="758ac-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="758ac-118">In questo caso, il pulsante Avanti risponderà solo ai tocchi (riscontri) all'interno del cerchio rosso.</span><span class="sxs-lookup"><span data-stu-id="758ac-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="758ac-119">I pulsanti hit vengono usati quando si desidera definire forme diverse dai rettangoli.</span><span class="sxs-lookup"><span data-stu-id="758ac-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="758ac-120">È comunque necessario definire le coordinate per ciascun pulsante in modo che le immagini secondarie come push e Disable possano trovarsi correttamente.</span><span class="sxs-lookup"><span data-stu-id="758ac-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="758ac-121">In pratica, ogni pulsante è limitato da un rettangolo e questi rettangoli di limite immaginari non devono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="758ac-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="758ac-122">I file di arte dell'area non sono necessari nelle interfacce Windows Media Player 10 mobile perché i tipi di pulsante non sono supportati in Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="758ac-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="758ac-123">L'immagine seguente è un file di area tipico.</span><span class="sxs-lookup"><span data-stu-id="758ac-123">The following image is a typical Region file.</span></span>

![file Region](images/cesdkreg.png)

<span data-ttu-id="758ac-125">Questo file definisce le parti dell'interfaccia per ogni pulsante di tipo hit.</span><span class="sxs-lookup"><span data-stu-id="758ac-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="758ac-126">Ogni colore verrà identificato in base al relativo numero di colore nella sezione dei pulsanti del file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="758ac-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="758ac-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="758ac-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="758ac-128">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="758ac-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




