---
title: Funzioni e strutture di Gestione compressione audio
description: Funzioni e strutture di Gestione compressione audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimediale, funzioni ACM
- audio, funzioni ACM
- Gestione compressione audio (ACM), funzioni
- ACM (Gestione compressione audio), funzioni
- audio multimediale, strutture ACM
- audio, strutture ACM
- Gestione compressione audio (ACM), strutture
- ACM (Gestione compressione audio), strutture
- Strutture di ACM
- Funzioni ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299628"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="4537c-113">Funzioni e strutture di Gestione compressione audio</span><span class="sxs-lookup"><span data-stu-id="4537c-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="4537c-114">Le funzioni ACM rientrano in diverse categorie.</span><span class="sxs-lookup"><span data-stu-id="4537c-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="4537c-115">Le convenzioni di denominazione per le funzioni facilitano l'identificazione di queste categorie.</span><span class="sxs-lookup"><span data-stu-id="4537c-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="4537c-116">I nomi delle funzioni (con due eccezioni) sono nel formato *acmGroupFunction*, dove *Group* designa la categoria ACM (ad esempio "driver", "Format", "FormatTag", "Filter", "FilterTag" o "Stream") e *Function* descrive l'azione eseguita dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="4537c-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="4537c-117">Le funzioni nei gruppi di filtro e di formato sono molto simili.</span><span class="sxs-lookup"><span data-stu-id="4537c-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="4537c-118">Quasi tutte le funzioni che agiscono sui filtri hanno una funzione parallela che agisce sui formati.</span><span class="sxs-lookup"><span data-stu-id="4537c-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="4537c-119">Nel gruppo Format alcune funzioni usano tag di formato Waveform-Audio (il membro **wFormatTag** di una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), mentre altri richiedono formati audio completi per la forma d'onda (la struttura **WAVEFORMATEX** completa).</span><span class="sxs-lookup"><span data-stu-id="4537c-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="4537c-120">Per informazioni di riferimento sulla struttura **WAVEFORMATEX** , vedere [Error](error.md).</span><span class="sxs-lookup"><span data-stu-id="4537c-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="4537c-121">Nel gruppo di filtri alcune funzioni usano i tag del filtro per la forma d'onda-audio (il membro **dwFilterTag** di una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), mentre altri richiedono filtri audio e di forma d'onda completi (la struttura **WAVEFILTER** completa).</span><span class="sxs-lookup"><span data-stu-id="4537c-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="4537c-122">Le funzioni del gruppo Stream rappresentano i molti passaggi necessari per una conversione: l'apertura di un'istanza di conversione, la preparazione per la conversione, la conversione, la pulizia al termine della conversione e la chiusura dell'istanza di conversione.</span><span class="sxs-lookup"><span data-stu-id="4537c-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 