---
title: DirectWrite (DWrite)
description: Le applicazioni attuali devono supportare il rendering del testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo per layout e testo Unicode. DirectWrite, un'API [DirectX,](../directx.md) fornisce queste funzionalità e altro ancora.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587949"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="5273f-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="5273f-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="5273f-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="5273f-105">Purpose</span></span>

<span data-ttu-id="5273f-106">Le applicazioni attuali devono supportare il rendering del testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo per layout e testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="5273f-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="5273f-107">DirectWrite, un'API [DirectX,](../directx.md) fornisce queste funzionalità e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="5273f-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="5273f-108">Sistema di layout di testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5273f-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="5273f-109">Rendering di testo [ClearType Microsoft di](/typography/cleartype/) alta qualità e secondario che può usare [GDI,](interoperating-with-gdi.md) [Direct2D](rendering-by-using-direct2d.md)o una tecnologia di rendering specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5273f-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="5273f-110">Testo con accelerazione hardware, se usato con [Direct2D.](rendering-by-using-direct2d.md)</span><span class="sxs-lookup"><span data-stu-id="5273f-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="5273f-111">Supporto per testo in più formati.</span><span class="sxs-lookup"><span data-stu-id="5273f-111">Support for multi-format text.</span></span>
- <span data-ttu-id="5273f-112">Supporto per le funzionalità tipografiche avanzate dei tipi di carattere OpenType.</span><span class="sxs-lookup"><span data-stu-id="5273f-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="5273f-113">Supporto per il layout e il rendering del testo in tutte le lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="5273f-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="5273f-114">Layout e rendering compatibili con [GDI.](interoperating-with-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="5273f-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="5273f-115">L'API supporta la misurazione, il disegno e l'hit testing di testo in più formati.</span><span class="sxs-lookup"><span data-stu-id="5273f-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="5273f-116">DirectWrite gestisce il testo in tutte le lingue supportate per le applicazioni globali e localizzate, sulla base dell'infrastruttura di lingua chiave disponibile in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5273f-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="5273f-117">DirectWrite fornisce anche un'API di rendering dei glifi di basso livello per gli sviluppatori che vogliono eseguire l'elaborazione da Unicode a glifo e del layout.</span><span class="sxs-lookup"><span data-stu-id="5273f-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="5273f-118">[Windows App SDK](/windows/apps/windows-app-sdk/) introduce una nuova versione di DirectWrite denominata DWriteCore che viene eseguita nelle versioni di Windows fino a Windows 8 e apre la porta per l'uso &mdash; &mdash; multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="5273f-118">[Windows App SDK](/windows/apps/windows-app-sdk/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="5273f-119">Per altri dettagli, vedere [Panoramica di DWriteCore.](dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5273f-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5273f-120">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="5273f-120">Run-time requirements</span></span>

- <span data-ttu-id="5273f-121">Windows 7 o Windows Vista con Service Pack 2 (SP2) e Aggiornamento piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5273f-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="5273f-122">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e Aggiornamento della piattaforma per Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5273f-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5273f-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5273f-123">In this section</span></span>

| <span data-ttu-id="5273f-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="5273f-124">Topic</span></span> | <span data-ttu-id="5273f-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5273f-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="5273f-126">Novità di DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5273f-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="5273f-127">Ecco alcune delle nuove aggiunte a DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5273f-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="5273f-128">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="5273f-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="5273f-129">Gli argomenti seguenti offrono una panoramica dell'API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5273f-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="5273f-130">Riferimento API</span><span class="sxs-lookup"><span data-stu-id="5273f-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="5273f-131">Descrive l'API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5273f-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="5273f-132">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="5273f-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="5273f-133">Questa sezione contiene informazioni sui programmi di esempio per DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5273f-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
