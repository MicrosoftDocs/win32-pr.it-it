---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8223ec5e98db3e45b0087073b4eb68baeae81280
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089179"
---
# <a name="direct2d"></a><span data-ttu-id="da3df-103">Direct2D</span><span class="sxs-lookup"><span data-stu-id="da3df-103">Direct2D</span></span>

## <a name="purpose"></a><span data-ttu-id="da3df-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="da3df-104">Purpose</span></span>

<span data-ttu-id="da3df-105">Direct2D è un'API per la grafica 2D in modalità immediata e con accelerazione hardware che offre prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo.</span><span class="sxs-lookup"><span data-stu-id="da3df-105">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="da3df-106">L'API Direct2D è progettata per interagire bene con GDI, GDI+ e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="da3df-106">The Direct2D API is designed to interoperate well with GDI, GDI+, and Direct3D.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="da3df-107">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="da3df-107">Developer audience</span></span>

<span data-ttu-id="da3df-108">Direct2D è progettato principalmente per l'uso da parte delle classi di sviluppatori seguenti:</span><span class="sxs-lookup"><span data-stu-id="da3df-108">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="da3df-109">Sviluppatori di applicazioni native di grandi dimensioni su scala aziendale.</span><span class="sxs-lookup"><span data-stu-id="da3df-109">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="da3df-110">Sviluppatori che creano toolkit e librerie di controllo per l'utilizzo da parte degli sviluppatori downstream.</span><span class="sxs-lookup"><span data-stu-id="da3df-110">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="da3df-111">Sviluppatori che richiedono il rendering lato server di grafica 2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-111">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="da3df-112">Gli sviluppatori che usano grafica Direct3D e necessitano di rendering 2D e testo semplici e ad alte prestazioni per menu, elementi dell'interfaccia utente e hud(HUD).</span><span class="sxs-lookup"><span data-stu-id="da3df-112">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user-interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="da3df-113">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="da3df-113">Run-time requirements</span></span>

-   <span data-ttu-id="da3df-114">Windows 7 o Windows Vista con Service Pack 2 (SP2) e Aggiornamento piattaforma per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="da3df-114">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista and later.</span></span>
-   <span data-ttu-id="da3df-115">Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e Aggiornamento della piattaforma per Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="da3df-115">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008 and later.</span></span>

> [!Note]
>
> <span data-ttu-id="da3df-116">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono un set di librerie di runtime che consente agli sviluppatori di scegliere come destinazione le applicazioni per Windows 7, Windows Vista, Windows Server 2008 R2 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="da3df-116">The Platform Update for Windows Vista and Platform Update for Windows Server 2008 are a set of run-time libraries that enables developers to target applications to Windows 7, Windows Vista, Windows Server 2008 R2, and Windows Server 2008.</span></span> <span data-ttu-id="da3df-117">Questi aggiornamenti saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="da3df-117">These updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="da3df-118">Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono Windows Update se è installato l'aggiornamento richiesto; In caso contrario, Windows Update scaricarlo e installarlo in background.</span><span class="sxs-lookup"><span data-stu-id="da3df-118">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span> <span data-ttu-id="da3df-119">Per altre informazioni su entrambi gli aggiornamenti, vedere [Aggiornamento della piattaforma per Windows Vista.](https://support.microsoft.com/kb/971644)</span><span class="sxs-lookup"><span data-stu-id="da3df-119">For more information about both updates, see [Platform Update for Windows Vista](https://support.microsoft.com/kb/971644).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="da3df-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="da3df-120">In this section</span></span>



| <span data-ttu-id="da3df-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="da3df-121">Topic</span></span>                                                                                          | <span data-ttu-id="da3df-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da3df-122">Description</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da3df-123">Novità di Direct2D</span><span class="sxs-lookup"><span data-stu-id="da3df-123">What's new in Direct2D</span></span>](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="da3df-124">Ecco alcune delle nuove aggiunte a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-124">Here are some of the new additions to Direct2D.</span></span> <br/>                                                                                                                   |
| [<span data-ttu-id="da3df-125">Informazioni su Direct2D</span><span class="sxs-lookup"><span data-stu-id="da3df-125">About Direct2D</span></span>](direct2d-overview.md)<br/>                                             | <span data-ttu-id="da3df-126">Introduce Direct2D, un'API che offre agli sviluppatori Win32 la possibilità di eseguire attività di rendering della grafica 2D con prestazioni e qualità visiva superiori.</span><span class="sxs-lookup"><span data-stu-id="da3df-126">Introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span> <br/> |
| [<span data-ttu-id="da3df-127">Guida introduttiva di Direct2D per Windows 8</span><span class="sxs-lookup"><span data-stu-id="da3df-127">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)<br/>    | <span data-ttu-id="da3df-128">Riepiloga i passaggi necessari per disegnare con Direct2D e fornisce codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="da3df-128">Summarizes the steps required to draw with Direct2D and provides example code.</span></span><br/>                                                                                     |
| [<span data-ttu-id="da3df-129">Attività iniziali con Direct2D</span><span class="sxs-lookup"><span data-stu-id="da3df-129">Getting Started with Direct2D</span></span>](getting-started-with-direct2d-nav.md)<br/>              | <span data-ttu-id="da3df-130">Descrive come iniziare a creare applicazioni Direct2D e fornisce codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="da3df-130">Describes how to get started creating Direct2D applications and provides example code.</span></span><br/>                                                                             |
| [<span data-ttu-id="da3df-131">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="da3df-131">Programming Guide</span></span>](programming-guide.md)<br/>                                          | <span data-ttu-id="da3df-132">Questa sezione contiene argomenti di programmazione concettuali che descrivono come usare l'API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-132">This section contains conceptual programming topics that describe how to use the Direct2D API.</span></span> <br/>                                                                    |
| [<span data-ttu-id="da3df-133">Informazioni di riferimento su Direct2D</span><span class="sxs-lookup"><span data-stu-id="da3df-133">Direct2D reference</span></span>](reference.md)<br/>                                                      | <span data-ttu-id="da3df-134">Descrive in dettaglio l'API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-134">Describes the Direct2D API in detail.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="da3df-135">Strumenti e utilità</span><span class="sxs-lookup"><span data-stu-id="da3df-135">Tools and Utilities</span></span>](tools-and-utilities.md)<br/>                                      | <span data-ttu-id="da3df-136">Strumenti e utilità disponibili per Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-136">Tools and utilities provided for Direct2D.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="da3df-137">Esempi</span><span class="sxs-lookup"><span data-stu-id="da3df-137">Samples</span></span>](d2d-samples.md)<br/>                                                          | <span data-ttu-id="da3df-138">Applicazioni di esempio che illustrano l'API Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-138">Sample applications that demonstrate the Direct2D API.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="da3df-139">Glossario Direct2D</span><span class="sxs-lookup"><span data-stu-id="da3df-139">Direct2D Glossary</span></span>](direct2d-glossary.md)<br/>                                          | <span data-ttu-id="da3df-140">Descrive i termini comunemente usati nella documentazione di Direct2D.</span><span class="sxs-lookup"><span data-stu-id="da3df-140">Describes terms commonly used by the Direct2D documentation.</span></span> <br/>                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="da3df-141">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="da3df-141">Additional resources</span></span>

-   [<span data-ttu-id="da3df-142">**Grafica e giochi DirectX**</span><span class="sxs-lookup"><span data-stu-id="da3df-142">**DirectX Graphics and Gaming**</span></span>](/windows/desktop/directx)
-   [<span data-ttu-id="da3df-143">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="da3df-143">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)

 

