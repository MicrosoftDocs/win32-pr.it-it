---
title: Generazione di un formato non standard
description: Generazione di un formato non standard
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Gestione compressione audio (ACM), formati non standard
- ACM (Gestione compressione audio), formati non standard
- Esempi di ACM, formati non standard
- acmFormatSuggest (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856049"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="b94b6-107">Generazione di un formato non standard</span><span class="sxs-lookup"><span data-stu-id="b94b6-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="b94b6-108">A volte un'applicazione richiede un formato non standard.</span><span class="sxs-lookup"><span data-stu-id="b94b6-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="b94b6-109">Ad esempio, un'applicazione potrebbe avere bisogno di un file in formato ADPCM a 16 kHz.</span><span class="sxs-lookup"><span data-stu-id="b94b6-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="b94b6-110">Poiché 16 kHz non sono standard, le funzioni di enumerazione non genereranno questo formato.</span><span class="sxs-lookup"><span data-stu-id="b94b6-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="b94b6-111">In realtà, a breve della codifica personalizzata degli algoritmi di formato nell'applicazione, non esiste un modo affidabile per generare un formato non standard.</span><span class="sxs-lookup"><span data-stu-id="b94b6-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="b94b6-112">Tuttavia, talvolta è possibile generare un formato analogo impostando un formato PCM valido con tutte le informazioni necessarie e quindi utilizzando la funzione [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) .</span><span class="sxs-lookup"><span data-stu-id="b94b6-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="b94b6-113">Poiché i compressori e i decompressori tentano di suggerire un formato più vicino al formato desiderato, il numero di canali e frequenza viene in genere mantenuto.</span><span class="sxs-lookup"><span data-stu-id="b94b6-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




