---
title: Conversione dello spazio colore
description: Conversione dello spazio colore
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK, conversione dello spazio colore
- ASF (Advanced Systems Format), conversione dello spazio colore
- ASF (formato avanzato dei sistemi), conversione dello spazio colore
- conversione dello spazio colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221420"
---
# <a name="color-space-conversion"></a><span data-ttu-id="63039-107">Conversione dello spazio colore</span><span class="sxs-lookup"><span data-stu-id="63039-107">Color Space Conversion</span></span>

<span data-ttu-id="63039-108">Spesso esiste una differenza tra la profondità di colore del formato video compresso nel profilo e il formato di input.</span><span class="sxs-lookup"><span data-stu-id="63039-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="63039-109">Quando si verifica questo problema, il video di origine deve essere convertito per essere conforme allo spazio dei colori della destinazione.</span><span class="sxs-lookup"><span data-stu-id="63039-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="63039-110">Il writer gestisce questo processo, comunicando con un convertitore di spazi colore interno.</span><span class="sxs-lookup"><span data-stu-id="63039-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="63039-111">Il lettore comunica anche con il convertitore di spazi dei colori per risolvere le differenze tra il formato compresso e il formato di output.</span><span class="sxs-lookup"><span data-stu-id="63039-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="63039-112">Come per tutte le trasformazioni eseguite sui dati, la conversione tra le profondità dei colori può ridurre la qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="63039-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="63039-113">Quando possibile, è consigliabile usare i formati di input e di output con la stessa profondità di colore del formato compresso.</span><span class="sxs-lookup"><span data-stu-id="63039-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63039-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63039-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63039-115">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="63039-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="63039-116">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="63039-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="63039-117">**Uso degli output**</span><span class="sxs-lookup"><span data-stu-id="63039-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




