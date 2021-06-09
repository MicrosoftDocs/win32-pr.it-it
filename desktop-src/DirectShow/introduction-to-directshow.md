---
description: Introduzione a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introduzione a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827225"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="aa6f7-103">Introduzione a DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa6f7-103">Introduction to DirectShow</span></span>

<span data-ttu-id="aa6f7-104">Microsoft® DirectShow® è un'architettura per lo streaming di contenuti multimediali nella piattaforma Microsoft Windows®.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="aa6f7-105">DirectShow consente l'acquisizione e la riproduzione di flussi multimediali di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="aa6f7-106">Supporta un'ampia gamma di formati, tra cui ASF (Advanced Systems Format), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) e file audio WAV.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="aa6f7-107">Supporta l'acquisizione da dispositivi digitali e analoghi basati su Windows Driver Model (WDM) o Video per Windows.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="aa6f7-108">Rileva e usa automaticamente l'hardware di accelerazione audio e video quando disponibile, ma supporta anche sistemi senza hardware di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="aa6f7-109">DirectShow è basato sul Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="aa6f7-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="aa6f7-110">Per scrivere un'applicazione o un componente DirectShow, è necessario comprendere la programmazione client COM.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="aa6f7-111">Per la maggior parte delle applicazioni, non è necessario implementare oggetti COM personalizzati.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="aa6f7-112">DirectShow fornisce i componenti necessari.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="aa6f7-113">Se tuttavia si vuole estendere DirectShow scrivendo componenti personalizzati, è necessario implementarli come oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="aa6f7-114">DirectShow è progettato per C++.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="aa6f7-115">Microsoft non fornisce un'API gestita per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="aa6f7-116">DirectShow semplifica le attività di riproduzione multimediale, conversione del formato e acquisizione.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="aa6f7-117">Allo stesso tempo, fornisce l'accesso all'architettura di controllo del flusso sottostante per le applicazioni che richiedono soluzioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="aa6f7-118">È anche possibile creare componenti DirectShow personalizzati per supportare nuovi formati o effetti personalizzati.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="aa6f7-119">Esempi di tipi di applicazione che è possibile scrivere con DirectShow includono lettori di file, lettori TV e DVD, applicazioni di modifica video, convertitori di formati di file, applicazioni di acquisizione audio-video, codificatori e decodificatori, processori di segnali digitali e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="aa6f7-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="aa6f7-120">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="aa6f7-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="aa6f7-121">Novità di DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa6f7-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="aa6f7-122">Formati supportati in DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa6f7-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="aa6f7-123">Domande frequenti su DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa6f7-123">DirectShow FAQ</span></span>](directshow-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="aa6f7-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa6f7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa6f7-125">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="aa6f7-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="aa6f7-126">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa6f7-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



