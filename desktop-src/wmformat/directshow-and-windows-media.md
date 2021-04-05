---
title: DirectShow e Windows Media
description: DirectShow e Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714215"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="e56dc-107">DirectShow e Windows Media</span><span class="sxs-lookup"><span data-stu-id="e56dc-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="e56dc-108">In alternativa all'uso esclusivo di Windows Media Format SDK, le applicazioni possono anche leggere e scrivere contenuto basato su Windows Media usando l'architettura di streaming Microsoft® DirectShow®, come descritto nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e56dc-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="e56dc-109">Sezione</span><span class="sxs-lookup"><span data-stu-id="e56dc-109">Section</span></span>                                                                                   | <span data-ttu-id="e56dc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e56dc-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e56dc-111">Informazioni su DirectShow</span><span class="sxs-lookup"><span data-stu-id="e56dc-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="e56dc-112">Descrive DirectShow in termini generali e indica dove ottenere ulteriori informazioni su di esso.</span><span class="sxs-lookup"><span data-stu-id="e56dc-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="e56dc-113">Perché usare DirectShow?</span><span class="sxs-lookup"><span data-stu-id="e56dc-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="e56dc-114">Viene descritto il modo in cui DirectShow semplifica determinate attività nella creazione e nella riproduzione di contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e56dc-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="e56dc-115">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e56dc-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="e56dc-116">Viene descritto come riprodurre file ASF con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e56dc-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="e56dc-117">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e56dc-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="e56dc-118">Viene descritto come creare file ASF usando DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e56dc-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="e56dc-119">\_Notifica degli eventi dello stato WMT in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e56dc-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="e56dc-120">Vengono descritti gli eventi di **\_ stato WMT** gestiti dai filtri ASF Reader e writer ASF e il modo in cui le applicazioni possono ricevere questi eventi.</span><span class="sxs-lookup"><span data-stu-id="e56dc-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="e56dc-121">Supporto DRM in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e56dc-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="e56dc-122">Viene descritto come leggere e scrivere file protetti da DRM tramite DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e56dc-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="e56dc-123">Informazioni di riferimento su DirectShow QASF</span><span class="sxs-lookup"><span data-stu-id="e56dc-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="e56dc-124">Contiene la documentazione di riferimento per i componenti DirectShow che supportano Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e56dc-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="e56dc-125">Tre applicazioni di esempio nell'SDK illustrano l'uso di DirectShow: DSCopy, DSPlay e DSSeekFM.</span><span class="sxs-lookup"><span data-stu-id="e56dc-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="e56dc-126">Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="e56dc-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="e56dc-127">Per le applicazioni che usano i componenti di QASF inclusi in questo SDK è necessario che sia installato Microsoft DirectX® 8,1 o versione successiva del Runtime SDK nei sistemi Windows® 2000, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="e56dc-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="e56dc-128">In particolare, questo runtime è richiesto dal filtro wrapper DMO che ospita i codec Windows Media in un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e56dc-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 




