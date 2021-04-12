---
title: Numeri (Windows Multimedia)
description: Numeri
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixer audio, controlli
- mixer audio, numeri
- mixer, controlli
- mixer, numeri
- controlli numero
- Struttura MIXERCONTROLDETAILS_SIGNED
- Struttura MIXERCONTROLDETAILS_UNSIGNED
- controllo decibel
- Percentuale controllo
- controllo firmato
- controllo senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118778"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="afdd8-114">Numeri (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="afdd8-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="afdd8-115">I controlli numero consentono all'utente di immettere dati numerici associati a una riga.</span><span class="sxs-lookup"><span data-stu-id="afdd8-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="afdd8-116">I dati numerici sono espressi come interi con segno, interi senza segno o valori di decibel interi.</span><span class="sxs-lookup"><span data-stu-id="afdd8-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="afdd8-117">Questi controlli utilizzano le strutture [**MIXERCONTROLDETAILS \_ firmate**](/previous-versions//dd757297(v=vs.85)) e [**MIXERCONTROLDETAILS \_ senza segno**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="afdd8-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="afdd8-118">Nella tabella seguente vengono descritti i tipi di controlli numerici.</span><span class="sxs-lookup"><span data-stu-id="afdd8-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="afdd8-119">Controllo</span><span class="sxs-lookup"><span data-stu-id="afdd8-119">Control</span></span>  | <span data-ttu-id="afdd8-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afdd8-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afdd8-121">Firmato</span><span class="sxs-lookup"><span data-stu-id="afdd8-121">Signed</span></span>   | <span data-ttu-id="afdd8-122">Consente valori interi immessi nell'intervallo compreso tra-231 e (231-1).</span><span class="sxs-lookup"><span data-stu-id="afdd8-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="afdd8-123">Senza segno</span><span class="sxs-lookup"><span data-stu-id="afdd8-123">Unsigned</span></span> | <span data-ttu-id="afdd8-124">Consente valori interi immessi nell'intervallo compreso tra 0 e (232-1).</span><span class="sxs-lookup"><span data-stu-id="afdd8-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="afdd8-125">Decibel</span><span class="sxs-lookup"><span data-stu-id="afdd8-125">Decibel</span></span>  | <span data-ttu-id="afdd8-126">Consente l'immissione di valori integer in decibel, in decimi di decibel.</span><span class="sxs-lookup"><span data-stu-id="afdd8-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="afdd8-127">L'intervallo di valori per questo controllo è compreso tra-32.768 e 32.767.</span><span class="sxs-lookup"><span data-stu-id="afdd8-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="afdd8-128">Percentuale</span><span class="sxs-lookup"><span data-stu-id="afdd8-128">Percent</span></span>  | <span data-ttu-id="afdd8-129">Consente di immettere valori come percentuali.</span><span class="sxs-lookup"><span data-stu-id="afdd8-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
