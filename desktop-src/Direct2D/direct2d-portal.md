---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047029"
---
# <a name="direct2d"></a><span data-ttu-id="62217-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="62217-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="62217-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="62217-104">Purpose</span></span>

<span data-ttu-id="62217-105">Direct2D è un'API per la grafica 2D in modalità immediata e con accelerazione hardware che offre prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo.</span><span class="sxs-lookup"><span data-stu-id="62217-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="62217-106">L'API Direct2D è progettata per interagire correttamente con GDI, GDI+ e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="62217-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="62217-107">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="62217-107">Developer audience</span></span>

<span data-ttu-id="62217-108">Direct2D è progettato principalmente per l'uso da parte delle classi di sviluppatori seguenti:</span><span class="sxs-lookup"><span data-stu-id="62217-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="62217-109">Sviluppatori di applicazioni native di grandi dimensioni e di livello aziendale.</span><span class="sxs-lookup"><span data-stu-id="62217-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="62217-110">Sviluppatori che creano Toolkit e librerie di controllo per l'uso da parte degli sviluppatori downstream.</span><span class="sxs-lookup"><span data-stu-id="62217-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="62217-111">Sviluppatori che richiedono il rendering lato server della grafica 2D.</span><span class="sxs-lookup"><span data-stu-id="62217-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="62217-112">Gli sviluppatori che utilizzano la grafica Direct3D e necessitano di rendering semplice e a prestazioni elevate 2D e di testo per menu, elementi dell'interfaccia utente (UI) e visualizzazioni Heads-up (HUDs).</span><span class="sxs-lookup"><span data-stu-id="62217-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="62217-113">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="62217-113">Run-time requirements</span></span>

-   <span data-ttu-id="62217-114">Windows 7 o Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="62217-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="62217-115">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="62217-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="62217-116">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono un set di librerie di runtime che consente agli sviluppatori di utilizzare applicazioni per Windows 7, Windows Vista, Windows Server 2008 R2 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="62217-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="62217-117">Questi aggiornamenti saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="62217-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="62217-118">Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.</span><span class="sxs-lookup"><span data-stu-id="62217-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="62217-119">Per ulteriori informazioni su entrambi gli aggiornamenti, vedere [aggiornamento della piattaforma per Windows Vista](https://support.microsoft.com/kb/971644).</span><span class="sxs-lookup"><span data-stu-id="62217-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="62217-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="62217-120">In this section</span></span>



| <span data-ttu-id="62217-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="62217-121">Topic</span></span>                                                                                          | <span data-ttu-id="62217-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62217-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62217-123">Novità di Direct2D</span><span class="sxs-lookup"><span data-stu-id="62217-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="62217-124">Di seguito sono riportate alcune delle nuove aggiunte a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="62217-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="62217-125">Informazioni su Direct2D</span><span class="sxs-lookup"><span data-stu-id="62217-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="62217-126">Introduce Direct2D, un'API che fornisce agli sviluppatori Win32 la possibilità di eseguire attività di rendering grafiche 2D con prestazioni e qualità visive superiori.</span><span class="sxs-lookup"><span data-stu-id="62217-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="62217-127">Guida introduttiva di Direct2D per Windows 8</span><span class="sxs-lookup"><span data-stu-id="62217-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="62217-128">Vengono riepilogati i passaggi necessari per creare con Direct2D e viene fornito codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="62217-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="62217-129">Introduzione con Direct2D</span><span class="sxs-lookup"><span data-stu-id="62217-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="62217-130">Viene descritto come iniziare a creare applicazioni Direct2D e viene fornito codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="62217-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="62217-131">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="62217-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="62217-132">Questa sezione contiene argomenti sulla programmazione concettuale che descrivono come usare l'API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="62217-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="62217-133">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="62217-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="62217-134">Descrive in modo dettagliato l'API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="62217-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="62217-135">Strumenti e utilità</span><span class="sxs-lookup"><span data-stu-id="62217-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="62217-136">Strumenti e utilità forniti per Direct2D.</span><span class="sxs-lookup"><span data-stu-id="62217-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="62217-137">Esempi</span><span class="sxs-lookup"><span data-stu-id="62217-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="62217-138">Applicazioni di esempio che illustrano l'API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="62217-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="62217-139">Glossario Direct2D</span><span class="sxs-lookup"><span data-stu-id="62217-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="62217-140">Vengono descritti i termini comunemente utilizzati dalla documentazione di Direct2D.</span><span class="sxs-lookup"><span data-stu-id="62217-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="62217-141">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="62217-141">Additional resources</span></span>

-   [<span data-ttu-id="62217-142">**Grafica e giochi DirectX**</span><span class="sxs-lookup"><span data-stu-id="62217-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="62217-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="62217-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

