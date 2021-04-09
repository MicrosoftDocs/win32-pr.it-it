---
description: Introduzione a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introduzione a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124353"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="d7d88-103">Introduzione a DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7d88-103">Introduction to DirectShow</span></span>

<span data-ttu-id="d7d88-104">Microsoft® DirectShow® è un'architettura per lo streaming di contenuti multimediali sulla piattaforma® di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d88-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="d7d88-105">DirectShow fornisce l'acquisizione e la riproduzione di alta qualità dei flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="d7d88-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="d7d88-106">Supporta un'ampia gamma di formati, tra cui il formato ASF (Advanced Systems Format), MPEG (Motion Picture Experts Group), Audio-Video file con interfoliazione (AVI), MPEG Audio Layer-3 (MP3) e WAV audio.</span><span class="sxs-lookup"><span data-stu-id="d7d88-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="d7d88-107">Supporta l'acquisizione da dispositivi digitali e analoghi basati sul Windows Driver Model (WDM) o sul video per Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d88-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="d7d88-108">Rileva automaticamente e utilizza hardware di accelerazione video e audio, se disponibile, ma supporta anche sistemi senza hardware di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="d7d88-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="d7d88-109">DirectShow si basa sul Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="d7d88-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="d7d88-110">Per scrivere un'applicazione o un componente DirectShow, è necessario comprendere la programmazione client COM.</span><span class="sxs-lookup"><span data-stu-id="d7d88-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="d7d88-111">Per la maggior parte delle applicazioni, non è necessario implementare oggetti COM personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d7d88-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="d7d88-112">DirectShow fornisce i componenti necessari.</span><span class="sxs-lookup"><span data-stu-id="d7d88-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="d7d88-113">Se si desidera estendere DirectShow scrivendo i propri componenti, è tuttavia necessario implementarli come oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="d7d88-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="d7d88-114">DirectShow è progettato per C++.</span><span class="sxs-lookup"><span data-stu-id="d7d88-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="d7d88-115">Microsoft non fornisce un'API gestita per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d7d88-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="d7d88-116">DirectShow semplifica la riproduzione dei contenuti multimediali, la conversione del formato e le attività di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d7d88-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="d7d88-117">Allo stesso tempo, fornisce l'accesso all'architettura di controllo del flusso sottostante per le applicazioni che richiedono soluzioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="d7d88-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="d7d88-118">È anche possibile creare componenti DirectShow personalizzati per supportare nuovi formati o effetti personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d7d88-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="d7d88-119">Esempi di tipi di applicazione che è possibile scrivere con DirectShow includono lettori di file, lettori TV e DVD, applicazioni di modifica video, convertitori di formati di file, applicazioni di acquisizione video audio, codificatori e decodificatori, processori di segnali digitali e molto altro.</span><span class="sxs-lookup"><span data-stu-id="d7d88-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="d7d88-120">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="d7d88-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d7d88-121">Novità di DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7d88-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="d7d88-122">Formati supportati in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7d88-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="d7d88-123">Domande frequenti su DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7d88-123">DirectShow FAQ</span></span>](directshow-faq.md)

## <a name="related-topics"></a><span data-ttu-id="d7d88-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7d88-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7d88-125">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="d7d88-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="d7d88-126">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7d88-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



