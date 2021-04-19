---
description: Convertitore da tee a sink a sink
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertitore da tee a sink a sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316295"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="e2fed-103">Convertitore da tee a sink a sink</span><span class="sxs-lookup"><span data-stu-id="e2fed-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="e2fed-104">Il convertitore Tee/Sink-to-sink è un filtro basato su KsProxy in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="e2fed-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="e2fed-105">Viene usato nei grafici di filtri per la televisione video analogici in cui viene eseguito il rendering o l'acquisizione di dati VBI.</span><span class="sxs-lookup"><span data-stu-id="e2fed-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="e2fed-106">Il filtro è connesso upstream al filtro di [acquisizione video WDM](wdm-video-capture-filter.md) e fornisce un modo efficiente per duplicare i flussi di dati in modalità kernel senza le transizioni dispendiose tra il kernel e la modalità utente.</span><span class="sxs-lookup"><span data-stu-id="e2fed-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="e2fed-107">Recapita ogni blocco di dati ricevuti a tutti i pin di output e il codec downstream è responsabile dell'individuazione dei dati VBI specifici da decodificare.</span><span class="sxs-lookup"><span data-stu-id="e2fed-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="e2fed-108">Il convertitore Tee/Sink-to-sink viene visualizzato nella categoria del filtro "dispositivi con splitter o di streaming WDM" (AM \_ KSCATEGORY \_ splitter).</span><span class="sxs-lookup"><span data-stu-id="e2fed-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="e2fed-109">Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente tramite [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e2fed-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="e2fed-110">Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="e2fed-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="e2fed-111">Per ulteriori informazioni, vedere [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e2fed-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2fed-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2fed-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2fed-113">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="e2fed-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
