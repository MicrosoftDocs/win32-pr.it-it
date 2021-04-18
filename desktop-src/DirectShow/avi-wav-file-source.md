---
description: Origine file AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Origine file AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304264"
---
# <a name="aviwav-file-source"></a><span data-ttu-id="fcbce-103">Origine file AVI/WAV</span><span class="sxs-lookup"><span data-stu-id="fcbce-103">AVI/WAV File Source</span></span>

<span data-ttu-id="fcbce-104">Operazione deprecata:</span><span class="sxs-lookup"><span data-stu-id="fcbce-104">(Deprecated.</span></span> <span data-ttu-id="fcbce-105">Per i file AVI e WAV, usare il [file di origine (Async)](file-source--async--filter.md) e la [barra di divisione AVI](avi-splitter-filter.md) o il [parser Wave](wave-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="fcbce-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="fcbce-106">Il filtro di origine file AVI/WAV legge i file di origine AVI e WAV e genera i pin di output appropriati per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="fcbce-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="fcbce-107">Per i file WAV, il filtro crea un pin di output audio che produce un flusso audio che può essere connesso a un filtro di rendering audio o a un filtro di trasformazione audio corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fcbce-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="fcbce-108">Per i file AVI, il filtro crea un pin di output video, che produce un flusso AVI compresso adatto per il filtro codec AVI e un pin di output audio, che produce un flusso audio adatto per un filtro per il rendering audio o un filtro di trasformazione audio corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fcbce-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcbce-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fcbce-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcbce-110">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="fcbce-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



