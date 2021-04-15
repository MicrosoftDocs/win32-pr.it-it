---
description: Panoramica del sistema DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Panoramica del sistema DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520586"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="35d7d-103">Panoramica del sistema DirectShow</span><span class="sxs-lookup"><span data-stu-id="35d7d-103">DirectShow System Overview</span></span>

<span data-ttu-id="35d7d-104">**Sfida dei contenuti multimediali**</span><span class="sxs-lookup"><span data-stu-id="35d7d-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="35d7d-105">L'uso dei contenuti multimediali presenta diverse principali problemi:</span><span class="sxs-lookup"><span data-stu-id="35d7d-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="35d7d-106">I flussi multimediali contengono grandi quantità di dati, che devono essere elaborati molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="35d7d-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="35d7d-107">Audio e video devono essere sincronizzati in modo che vengano avviati e arrestati allo stesso tempo e riproducano alla stessa velocità.</span><span class="sxs-lookup"><span data-stu-id="35d7d-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="35d7d-108">I dati possono provenire da molte origini, tra cui file locali, reti di computer, trasmissioni televisive e videocamere.</span><span class="sxs-lookup"><span data-stu-id="35d7d-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="35d7d-109">I dati sono disponibili in diversi formati, ad esempio Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) e Digital video (DV).</span><span class="sxs-lookup"><span data-stu-id="35d7d-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="35d7d-110">Il programmatore non sa in anticipo quali dispositivi hardware saranno presenti nel sistema dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="35d7d-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="35d7d-111">**Soluzione DirectShow**</span><span class="sxs-lookup"><span data-stu-id="35d7d-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="35d7d-112">DirectShow è progettato per risolvere ognuno di questi problemi.</span><span class="sxs-lookup"><span data-stu-id="35d7d-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="35d7d-113">Il principale obiettivo di progettazione consiste nel semplificare l'attività di creazione di applicazioni multimediali digitali sulla piattaforma Windows, isolando le applicazioni dalle complessità dei trasporti di dati, le differenze hardware e la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="35d7d-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="35d7d-114">Per ottenere la velocità effettiva necessaria per lo streaming di video e audio, DirectShow utilizza Direct3D e DirectSound laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="35d7d-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="35d7d-115">Queste tecnologie eseguono il rendering dei dati in modo efficiente sulle schede audio e grafiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="35d7d-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="35d7d-116">DirectShow sincronizza la riproduzione incapsulando i dati multimediali in campioni con timestamp.</span><span class="sxs-lookup"><span data-stu-id="35d7d-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="35d7d-117">Per gestire la varietà di origini, formati e dispositivi hardware possibili, DirectShow usa un'architettura modulare, in cui l'applicazione combina e trova la corrispondenza con componenti software diversi, detti *filtri*.</span><span class="sxs-lookup"><span data-stu-id="35d7d-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="35d7d-118">DirectShow fornisce filtri che supportano l'acquisizione e l'ottimizzazione di dispositivi basati sul Windows Driver Model (WDM), oltre a filtri che supportano le schede di acquisizione video for Windows (VfW) precedenti e i codec scritti per le interfacce di Gestione compressione audio (ACM) e video Compression Manager (VCM).</span><span class="sxs-lookup"><span data-stu-id="35d7d-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="35d7d-119">Il diagramma seguente illustra la relazione tra un'applicazione, i componenti DirectShow e alcuni componenti hardware e software supportati da DirectShow.</span><span class="sxs-lookup"><span data-stu-id="35d7d-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![architettura di alto livello](images/arch-oview2.png)

<span data-ttu-id="35d7d-121">Come illustrato qui, i filtri DirectShow comunicano con e controllano un'ampia gamma di dispositivi, tra cui il file system locale, il sintonizzatore TV e le schede di acquisizione video, i codec VfW, la visualizzazione video (tramite DirectDraw o GDI) e la scheda audio (tramite DirectSound).</span><span class="sxs-lookup"><span data-stu-id="35d7d-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="35d7d-122">Quindi, DirectShow isola l'applicazione da molte delle complessità di questi dispositivi.</span><span class="sxs-lookup"><span data-stu-id="35d7d-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="35d7d-123">DirectShow fornisce inoltre filtri nativi per la compressione e la decompressione per determinati formati di file.</span><span class="sxs-lookup"><span data-stu-id="35d7d-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35d7d-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35d7d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35d7d-125">Informazioni su DirectShow</span><span class="sxs-lookup"><span data-stu-id="35d7d-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



