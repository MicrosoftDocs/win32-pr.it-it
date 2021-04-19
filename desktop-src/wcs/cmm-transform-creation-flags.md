---
title: Flag di creazione della trasformazione CMM
description: CMM usare i flag di creazione della trasformazione come hint per la creazione di una trasformazione colore. Per determinare il modo migliore di usare questi flag, spetta alla CMM.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "106320183"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="23dac-104">Flag di creazione della trasformazione CMM</span><span class="sxs-lookup"><span data-stu-id="23dac-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="23dac-105">CMM usare i flag di creazione della trasformazione come hint per la creazione di una trasformazione colore.</span><span class="sxs-lookup"><span data-stu-id="23dac-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="23dac-106">Per determinare il modo migliore di usare questi flag, spetta alla CMM.</span><span class="sxs-lookup"><span data-stu-id="23dac-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="23dac-107">Tutte le funzioni che utilizzano questi flag passano o ricevono valori di flag tramite un parametro denominato *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="23dac-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="23dac-108">La **parola** più ordinata di *dwFlags* deve essere impostata su un valore della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="23dac-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="23dac-109">Costante</span><span class="sxs-lookup"><span data-stu-id="23dac-109">Constant</span></span>                    | <span data-ttu-id="23dac-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23dac-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23dac-111">Abilita \_ \_ controllo gamut</span><span class="sxs-lookup"><span data-stu-id="23dac-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="23dac-112">Usare questa trasformazione per il controllo della gamma.</span><span class="sxs-lookup"><span data-stu-id="23dac-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="23dac-113">USA \_ \_ colorimetrico relativo</span><span class="sxs-lookup"><span data-stu-id="23dac-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="23dac-114">Non mantenere il punto bianco.</span><span class="sxs-lookup"><span data-stu-id="23dac-114">Do not preserve the white point.</span></span> <span data-ttu-id="23dac-115">Se la gamma di output non supporta un determinato colore, utilizzare il colore supportato più vicino.</span><span class="sxs-lookup"><span data-stu-id="23dac-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="23dac-116">Vedere rendering di Intent.</span><span class="sxs-lookup"><span data-stu-id="23dac-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="23dac-117">\_conversione veloce</span><span class="sxs-lookup"><span data-stu-id="23dac-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="23dac-118">Cerca solo il colore.</span><span class="sxs-lookup"><span data-stu-id="23dac-118">Look up color only.</span></span> <span data-ttu-id="23dac-119">Non interpolare il colore.</span><span class="sxs-lookup"><span data-stu-id="23dac-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="23dac-120">PRESERVEBLACK</span><span class="sxs-lookup"><span data-stu-id="23dac-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="23dac-121">Inserisce il GMMP di generazione nera appropriato come ultimo GMMP nella sequenza di trasformazione</span><span class="sxs-lookup"><span data-stu-id="23dac-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="23dac-122">WCS \_ Always</span><span class="sxs-lookup"><span data-stu-id="23dac-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="23dac-123">Usare il percorso del codice WCS anche per le trasformazioni ICC.</span><span class="sxs-lookup"><span data-stu-id="23dac-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="23dac-124">trasformazione SEQUENZIAle \_</span><span class="sxs-lookup"><span data-stu-id="23dac-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="23dac-125">Flag di creazione trasformazione per la creazione di una trasformazione colore sequenziale (non ottimizzata).</span><span class="sxs-lookup"><span data-stu-id="23dac-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="23dac-126">La **parola** più bassa può avere uno dei valori costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="23dac-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="23dac-127">Costante</span><span class="sxs-lookup"><span data-stu-id="23dac-127">Constant</span></span>     | <span data-ttu-id="23dac-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23dac-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23dac-129">modalità di prova \_</span><span class="sxs-lookup"><span data-stu-id="23dac-129">PROOF\_MODE</span></span>  | <span data-ttu-id="23dac-130">La trasformazione verrà utilizzata per visualizzare l'anteprima dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="23dac-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="23dac-131">Qualità dell'immagine ridotta.</span><span class="sxs-lookup"><span data-stu-id="23dac-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="23dac-132">\_modalità normale</span><span class="sxs-lookup"><span data-stu-id="23dac-132">NORMAL\_MODE</span></span> | <span data-ttu-id="23dac-133">La trasformazione verrà usata per la visualizzazione dell'immagine normale.</span><span class="sxs-lookup"><span data-stu-id="23dac-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="23dac-134">Qualità media dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="23dac-134">Average image quality.</span></span>                            |
| <span data-ttu-id="23dac-135">\_modalità migliore</span><span class="sxs-lookup"><span data-stu-id="23dac-135">BEST\_MODE</span></span>   | <span data-ttu-id="23dac-136">La trasformazione verrà usata per la visualizzazione dell'immagine di qualità massima possibile sul dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="23dac-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="23dac-137">Passaggio dalla \_ modalità di prova alla \_ modalità migliore, la qualità di output migliora in genere e trasforma la velocità diminuisce.</span><span class="sxs-lookup"><span data-stu-id="23dac-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23dac-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23dac-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23dac-139">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="23dac-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="23dac-140">Costanti ICM</span><span class="sxs-lookup"><span data-stu-id="23dac-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




