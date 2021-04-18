---
title: DirectWrite (DWrite)
description: Le applicazioni attuali devono supportare il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione e il testo Unicode completo e il supporto del layout. DirectWrite, un'API [DirectX](../directx.md) , fornisce queste funzionalità e altro ancora.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2020
ms.locfileid: "104475016"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="cb365-104">DirectWrite (DWrite)</span><span class="sxs-lookup"><span data-stu-id="cb365-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="cb365-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="cb365-105">Purpose</span></span>

<span data-ttu-id="cb365-106">Le applicazioni attuali devono supportare il rendering di testo di alta qualità, i tipi di carattere di struttura indipendenti dalla risoluzione e il testo Unicode completo e il supporto del layout.</span><span class="sxs-lookup"><span data-stu-id="cb365-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="cb365-107">DirectWrite, un'API [DirectX](../directx.md) , fornisce queste funzionalità e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="cb365-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="cb365-108">Sistema di layout del testo indipendente dal dispositivo che migliora la leggibilità del testo nei documenti e nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cb365-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="cb365-109">Rendering di testo di alta qualità, sottopixel, [Microsoft ClearType](/typography/cleartype/) che può utilizzare la tecnologia di rendering [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)o specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb365-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="cb365-110">Testo con accelerazione hardware, se usato con [Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="cb365-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="cb365-111">Supporto per il testo in più formati.</span><span class="sxs-lookup"><span data-stu-id="cb365-111">Support for multi-format text.</span></span>
- <span data-ttu-id="cb365-112">Supporto per le funzionalità tipografiche avanzate dei tipi di carattere OpenType.</span><span class="sxs-lookup"><span data-stu-id="cb365-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="cb365-113">Supporto per il layout e il rendering del testo in tutte le lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="cb365-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="cb365-114">Layout e rendering compatibili con [GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="cb365-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="cb365-115">L'API supporta la misurazione, il disegno e l'hit testing del testo in più formati.</span><span class="sxs-lookup"><span data-stu-id="cb365-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="cb365-116">DirectWrite gestisce il testo in tutte le lingue supportate per le applicazioni globali e localizzate, basandosi sull'infrastruttura di linguaggio chiave disponibile in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb365-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="cb365-117">DirectWrite fornisce anche un'API di rendering dei glifi di basso livello per gli sviluppatori che vogliono eseguire l'elaborazione da Unicode a glifo e del layout.</span><span class="sxs-lookup"><span data-stu-id="cb365-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="cb365-118">Il [progetto Reunion](/windows/apps/project-reunion/) introduce una nuova versione di DirectWrite &mdash; denominata DWriteCore &mdash; che viene eseguita nelle versioni di Windows fino a Windows 8 e apre lo sportello per l'uso multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="cb365-118">[Project Reunion](/windows/apps/project-reunion/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="cb365-119">Per altri dettagli, vedere [Panoramica di DWriteCore](dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cb365-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cb365-120">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="cb365-120">Run-time requirements</span></span>

- <span data-ttu-id="cb365-121">Windows 7 o Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb365-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="cb365-122">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb365-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb365-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cb365-123">In this section</span></span>

| <span data-ttu-id="cb365-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="cb365-124">Topic</span></span> | <span data-ttu-id="cb365-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb365-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="cb365-126">Novità di DirectWrite</span><span class="sxs-lookup"><span data-stu-id="cb365-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="cb365-127">Di seguito sono riportate alcune delle nuove aggiunte a DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="cb365-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="cb365-128">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="cb365-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="cb365-129">Negli argomenti seguenti viene fornita una panoramica dell'API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="cb365-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="cb365-130">Riferimento API</span><span class="sxs-lookup"><span data-stu-id="cb365-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="cb365-131">Descrive l'API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="cb365-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="cb365-132">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="cb365-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="cb365-133">Questa sezione contiene informazioni sui programmi di esempio per DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="cb365-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
