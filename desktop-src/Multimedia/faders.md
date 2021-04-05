---
title: Fader
description: Fader
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixer audio, controlli
- mixer audio, cursori
- mixer, controlli
- mixer, fader
- fader
- Struttura MIXERCONTROLDETAILS_UNSIGNED
- controllo dissolvenza volume
- controllo Fade volume bass
- controllo Fade volume Treble
- controllo equalizzatore grafico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956393"
---
# <a name="faders"></a><span data-ttu-id="b77b9-113">Fader</span><span class="sxs-lookup"><span data-stu-id="b77b9-113">Faders</span></span>

<span data-ttu-id="b77b9-114">I controlli fader sono in genere controlli verticali che possono essere regolati verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="b77b9-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="b77b9-115">Questi controlli hanno una scala lineare e usano la [**struttura \_ senza segno MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare i dettagli del controllo.</span><span class="sxs-lookup"><span data-stu-id="b77b9-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="b77b9-116">Nella tabella seguente vengono descritti i tipi di fader.</span><span class="sxs-lookup"><span data-stu-id="b77b9-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="b77b9-117">Controllo</span><span class="sxs-lookup"><span data-stu-id="b77b9-117">Control</span></span>   | <span data-ttu-id="b77b9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b77b9-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b77b9-119">Fader</span><span class="sxs-lookup"><span data-stu-id="b77b9-119">Fader</span></span>     | <span data-ttu-id="b77b9-120">Controllo di dissolvenza generale.</span><span class="sxs-lookup"><span data-stu-id="b77b9-120">General fade control.</span></span> <span data-ttu-id="b77b9-121">L'intervallo di valori accettabili è compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="b77b9-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b77b9-122">Volume</span><span class="sxs-lookup"><span data-stu-id="b77b9-122">Volume</span></span>    | <span data-ttu-id="b77b9-123">Controllo di dissolvenza generale del volume.</span><span class="sxs-lookup"><span data-stu-id="b77b9-123">General volume fade control.</span></span> <span data-ttu-id="b77b9-124">L'intervallo di valori accettabili è compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="b77b9-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="b77b9-125">Per informazioni sulla modifica di questo intervallo, vedere la documentazione relativa al dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="b77b9-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="b77b9-126">Basso</span><span class="sxs-lookup"><span data-stu-id="b77b9-126">Bass</span></span>      | <span data-ttu-id="b77b9-127">Controllo dissolvenza volume basso.</span><span class="sxs-lookup"><span data-stu-id="b77b9-127">Bass volume fade control.</span></span> <span data-ttu-id="b77b9-128">L'intervallo di valori accettabili è compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="b77b9-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="b77b9-129">I limiti della banda di frequenza bassi sono specifici dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b77b9-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="b77b9-130">Per informazioni sui limiti delle bande, vedere la documentazione relativa al dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="b77b9-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="b77b9-131">Acuti</span><span class="sxs-lookup"><span data-stu-id="b77b9-131">Treble</span></span>    | <span data-ttu-id="b77b9-132">Controllo Fade volume Treble.</span><span class="sxs-lookup"><span data-stu-id="b77b9-132">Treble volume fade control.</span></span> <span data-ttu-id="b77b9-133">L'intervallo di valori accettabili è compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="b77b9-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="b77b9-134">I limiti della banda di frequenze acute sono specifici dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b77b9-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="b77b9-135">Per informazioni sui limiti della banda, vedere la documentazione relativa al dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="b77b9-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="b77b9-136">Equalizer</span><span class="sxs-lookup"><span data-stu-id="b77b9-136">Equalizer</span></span> | <span data-ttu-id="b77b9-137">Controllo equalizzatore grafico.</span><span class="sxs-lookup"><span data-stu-id="b77b9-137">Graphic equalizer control.</span></span> <span data-ttu-id="b77b9-138">L'intervallo di valori accettabili per una banda dell'equalizzatore è compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="b77b9-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="b77b9-139">Il numero di bande di equalizzatore e i relativi limiti sono specifici dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b77b9-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="b77b9-140">Per informazioni sull'equalizzatore, vedere la documentazione relativa al dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="b77b9-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="b77b9-141">È possibile usare la [**struttura \_ LISTTEXT di MIXERCONTROLDETAILS**](/previous-versions//dd757296(v=vs.85)) per recuperare le etichette di testo per l'equalizzatore.</span><span class="sxs-lookup"><span data-stu-id="b77b9-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 