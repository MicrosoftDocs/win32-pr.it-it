---
title: Macro per i valori e i colori CMYK
description: Le macro seguenti sono utili per modificare i valori CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS), macro CMYK
- WCS (Windows Color System), macro CMYK
- Gestione colori immagine, macro CMYK
- gestione dei colori, macro CMYK
- colori, macro CMYK
- Riferimento a WCS, macro CMYK
- informazioni di riferimento sul WCS, le macro CMYK
- Macro CMYK
- cyan magenta giallo nero (CMYK)
- CMYK (cyan magenta giallo nero)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320166"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="7c620-113">Macro per i valori e i colori CMYK</span><span class="sxs-lookup"><span data-stu-id="7c620-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="7c620-114">Le macro seguenti sono utili per modificare i valori CMYK.</span><span class="sxs-lookup"><span data-stu-id="7c620-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="7c620-115">Macro</span><span class="sxs-lookup"><span data-stu-id="7c620-115">Macro</span></span>                          | <span data-ttu-id="7c620-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c620-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="7c620-117">**CMYK**</span><span class="sxs-lookup"><span data-stu-id="7c620-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="7c620-118">Compila un valore CMYK dai singoli valori ciano, magenta, giallo e nero.</span><span class="sxs-lookup"><span data-stu-id="7c620-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="7c620-119">**GetCValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="7c620-120">Recupera il valore del colore ciano da un valore di colore CMYK.</span><span class="sxs-lookup"><span data-stu-id="7c620-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="7c620-121">**GetKValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="7c620-122">Recupera il valore del colore nero da un valore di colore CMYK.</span><span class="sxs-lookup"><span data-stu-id="7c620-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="7c620-123">**GetMValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="7c620-124">Recupera il valore magenta da un valore di colore CMYK.</span><span class="sxs-lookup"><span data-stu-id="7c620-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="7c620-125">**GetYValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="7c620-126">Recupera il valore di colore giallo da un valore di colore CMYK.</span><span class="sxs-lookup"><span data-stu-id="7c620-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="7c620-127">Le macro seguenti vengono usate con il colore.</span><span class="sxs-lookup"><span data-stu-id="7c620-127">The following macros are used with color.</span></span>



| <span data-ttu-id="7c620-128">Macro</span><span class="sxs-lookup"><span data-stu-id="7c620-128">Macro</span></span>                                | <span data-ttu-id="7c620-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c620-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c620-130">**GetBValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="7c620-131">Ottiene un valore blu RGB.</span><span class="sxs-lookup"><span data-stu-id="7c620-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="7c620-132">**GetGValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="7c620-133">Ottiene un valore verde RGB.</span><span class="sxs-lookup"><span data-stu-id="7c620-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="7c620-134">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="7c620-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="7c620-135">Ottiene un valore rosso RGB.</span><span class="sxs-lookup"><span data-stu-id="7c620-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="7c620-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c620-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="7c620-137">Accetta un indice in una voce della tavolozza dei colori logici e restituisce un identificatore di voce della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="7c620-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="7c620-138">**PALETTERGB**</span><span class="sxs-lookup"><span data-stu-id="7c620-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="7c620-139">Accetta tre valori che rappresentano le intensità relative di rosso, verde e blu e restituisce un identificatore rosso, verde, blu (RGB) relativo alla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="7c620-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="7c620-140">RGB</span><span class="sxs-lookup"><span data-stu-id="7c620-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="7c620-141">Seleziona un colore rosso, verde, blu (RGB) basato sugli argomenti forniti e sulle funzionalità di colore del dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="7c620-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 