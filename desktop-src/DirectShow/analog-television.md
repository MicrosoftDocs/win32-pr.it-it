---
description: Televisione analoga
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisione analoga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124251"
---
# <a name="analog-television"></a><span data-ttu-id="52cf3-103">Televisione analoga</span><span class="sxs-lookup"><span data-stu-id="52cf3-103">Analog Television</span></span>

<span data-ttu-id="52cf3-104">La televisione analogica differisce da altri scenari di acquisizione video in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="52cf3-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="52cf3-105">La scheda Tuner viene sintonizzata su un segnale analogico, che viene quindi digitato.</span><span class="sxs-lookup"><span data-stu-id="52cf3-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="52cf3-106">L'audio viene portato nel segnale analogico.</span><span class="sxs-lookup"><span data-stu-id="52cf3-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="52cf3-107">Il modo in cui l'audio raggiunge la scheda audio varia a seconda dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="52cf3-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="52cf3-108">Il segnale può contenere dati aggiuntivi nell'intervallo di spaziatura verticale (VBI), ad esempio sottotitoli (CC), World Standard Teletext (WST) e Extended Data Services (XDS).</span><span class="sxs-lookup"><span data-stu-id="52cf3-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="52cf3-109">Il diagramma seguente illustra un tipico grafico di filtro per l'anteprima della televisione.</span><span class="sxs-lookup"><span data-stu-id="52cf3-109">The following diagram shows a typical filter graph for television preview.</span></span>

![grafico analogico TV](images/vidcap06.png)

-   <span data-ttu-id="52cf3-111">Il filtro del [sintonizzatore TV](tv-tuner-filter.md) controlla l'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="52cf3-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="52cf3-112">Il filtro [audio TV](tv-audio-filter.md) controlla la decodifica audio.</span><span class="sxs-lookup"><span data-stu-id="52cf3-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="52cf3-113">Se la scheda Tuner contiene più di un input fisico, il filtro per la barra del [video analogo](analog-video-crossbar-filter.md) consente all'applicazione di selezionare l'input da decodificare e di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="52cf3-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="52cf3-114">Il filtro di [acquisizione video WDM](wdm-video-capture-filter.md) recapita il flusso video digitato.</span><span class="sxs-lookup"><span data-stu-id="52cf3-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="52cf3-115">Il generatore di grafici di acquisizione inserisce automaticamente tutti i filtri necessari a Monte dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="52cf3-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="52cf3-116">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="52cf3-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="52cf3-117">Ottimizzazione della televisione analoga</span><span class="sxs-lookup"><span data-stu-id="52cf3-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="52cf3-118">Audio TV analogico</span><span class="sxs-lookup"><span data-stu-id="52cf3-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="52cf3-119">Didascalie e televideo chiusi</span><span class="sxs-lookup"><span data-stu-id="52cf3-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="52cf3-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52cf3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52cf3-121">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="52cf3-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



