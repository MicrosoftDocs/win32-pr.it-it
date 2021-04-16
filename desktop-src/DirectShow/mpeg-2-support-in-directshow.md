---
description: Supporto MPEG-2 in DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Supporto MPEG-2 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522194"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="fa808-103">Supporto MPEG-2 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa808-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="fa808-104">Questa sezione descrive i componenti che è possibile usare per riprodurre contenuto MPEG-2 in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fa808-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="fa808-105">Sebbene il video DVD si basi su MPEG-2, in questa sezione non viene descritta la riproduzione o la navigazione in DVD.</span><span class="sxs-lookup"><span data-stu-id="fa808-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="fa808-106">Per informazioni sui DVD in DirectShow, vedere [applicazioni DVD](dvd-applications.md).</span><span class="sxs-lookup"><span data-stu-id="fa808-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="fa808-107">I dati MPEG-2 possono provenire da un file locale o da un'origine live, ad esempio una trasmissione di rete o un dispositivo D-VHS.</span><span class="sxs-lookup"><span data-stu-id="fa808-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="fa808-108">La riproduzione dei file è detta *modalità pull* , perché il filtro del parser estrae i dati dal file nel grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="fa808-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="fa808-109">Le origini attive sono denominate *modalità push* perché il filtro di origine inserisce i dati nel grafico.</span><span class="sxs-lookup"><span data-stu-id="fa808-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="fa808-110">DirectShow fornisce due filtri che consentono di analizzare i flussi di sistema MPEG-2:</span><span class="sxs-lookup"><span data-stu-id="fa808-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="fa808-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): questo filtro supporta la modalità push per flussi di programma e flussi di trasporto.</span><span class="sxs-lookup"><span data-stu-id="fa808-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="fa808-112">In Windows XP e versioni successive, supporta anche la modalità pull per i flussi di programma.</span><span class="sxs-lookup"><span data-stu-id="fa808-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="fa808-113">[Splitter MPEG-2](mpeg-2-splitter.md): questo filtro supporta la modalità pull per i flussi di programma sulle piattaforme di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="fa808-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="fa808-114">Questo filtro è deprecato in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fa808-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="fa808-115">Per usare il separatore MPEG-2 demux o MPEG-2, è necessario disporre di decodificatori audio e video MPEG-2 compatibili con DirectShow che accettano i flussi elementari (PES).</span><span class="sxs-lookup"><span data-stu-id="fa808-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="fa808-116">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="fa808-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fa808-117">Panoramica dei sistemi MPEG-2</span><span class="sxs-lookup"><span data-stu-id="fa808-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="fa808-118">Uso del Demultiplexer MPEG-2</span><span class="sxs-lookup"><span data-stu-id="fa808-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="fa808-119">Uso della barra di divisione MPEG-2</span><span class="sxs-lookup"><span data-stu-id="fa808-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="fa808-120">Proprietà di esempio MPEG</span><span class="sxs-lookup"><span data-stu-id="fa808-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="fa808-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa808-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa808-122">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="fa808-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



