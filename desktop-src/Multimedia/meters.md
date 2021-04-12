---
title: Metri
description: Metri
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mixer audio, controlli
- mixer audio, contatori
- mixer, controlli
- mixer, contatori
- controlli contatore
- Struttura MIXERCONTROLDETAILS_BOOLEAN
- Struttura MIXERCONTROLDETAILS_SIGNED
- Struttura MIXERCONTROLDETAILS_UNSIGNED
- Controllo booleano
- picco di controllo
- controllo firmato
- controllo senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473115"
---
# <a name="meters"></a><span data-ttu-id="14d89-115">Metri</span><span class="sxs-lookup"><span data-stu-id="14d89-115">Meters</span></span>

<span data-ttu-id="14d89-116">Il contatore controlla i dati delle misure che passano attraverso una linea audio.</span><span class="sxs-lookup"><span data-stu-id="14d89-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="14d89-117">Questi controlli utilizzano le strutture [**MIXERCONTROLDETAILS \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS \_ signed**](/previous-versions//dd757297(v=vs.85))e [**MIXERCONTROLDETAILS \_ senza segno**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="14d89-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="14d89-118">Nella tabella seguente vengono descritti i tipi di contatori.</span><span class="sxs-lookup"><span data-stu-id="14d89-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="14d89-119">Controllo</span><span class="sxs-lookup"><span data-stu-id="14d89-119">Control</span></span>  | <span data-ttu-id="14d89-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14d89-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d89-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="14d89-121">Boolean</span></span>  | <span data-ttu-id="14d89-122">Misura se un valore intero è FALSE/OFF (zero) o TRUE/ON (diverso da zero).</span><span class="sxs-lookup"><span data-stu-id="14d89-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="14d89-123">Peak</span><span class="sxs-lookup"><span data-stu-id="14d89-123">Peak</span></span>     | <span data-ttu-id="14d89-124">Misura la deflessione da 0 in entrambe le direzioni positivo e negativo.</span><span class="sxs-lookup"><span data-stu-id="14d89-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="14d89-125">L'intervallo di valori integer per il contatore massimo è da-32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="14d89-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="14d89-126">Firmato</span><span class="sxs-lookup"><span data-stu-id="14d89-126">Signed</span></span>   | <span data-ttu-id="14d89-127">Misura i valori interi nell'intervallo compreso tra-231 e (231-1).</span><span class="sxs-lookup"><span data-stu-id="14d89-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="14d89-128">Il driver del mixer definisce i limiti di questo contatore.</span><span class="sxs-lookup"><span data-stu-id="14d89-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="14d89-129">Senza segno</span><span class="sxs-lookup"><span data-stu-id="14d89-129">Unsigned</span></span> | <span data-ttu-id="14d89-130">Misura i valori interi nell'intervallo compreso tra 0 e (232-1).</span><span class="sxs-lookup"><span data-stu-id="14d89-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="14d89-131">Il driver del mixer definisce i limiti di questo contatore.</span><span class="sxs-lookup"><span data-stu-id="14d89-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 