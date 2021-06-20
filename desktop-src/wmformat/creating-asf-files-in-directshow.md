---
title: Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)
description: Informazioni sulla creazione di file ASF in DirectShow con Windows Media Format 11 SDK. ASF è un formato di contenitore che può contenere qualsiasi tipo di dati.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, creazione di file ASF in DirectShow
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format),DirectShow
- Advanced Systems Format (ASF), creazione in DirectShow
- ASF (Advanced Systems Format), creazione in DirectShow
- DirectShow, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406184"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="8e5a7-111">Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="8e5a7-111">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="8e5a7-112">È possibile usare DirectShow per creare file ASF direttamente da origini di acquisizione, ad esempio videocamere DV o per transcodificare altri file in Formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-112">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="8e5a7-113">In entrambi gli scenari, le applicazioni creano grafici di filtro che includono il filtro [WM ASF Writer](wm-asf-writer-filter.md) come renderer.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-113">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="8e5a7-114">WM ASF Writer fornisce un wrapper parziale per Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-114">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="8e5a7-115">Le applicazioni possono usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro per passare un profilo di sistema (versioni 4, 7 o 8) o usare direttamente Windows Media Format SDK per creare un profilo personalizzato da passare al filtro.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-115">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="8e5a7-116">Per aggiungere metadati e altre informazioni sull'intestazione, l'applicazione usa [**l'interfaccia IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) che può essere ottenuta dal filtro.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-116">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="8e5a7-117">Dopo aver configurato il profilo e i metadati, l'applicazione può semplicemente eseguire il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-117">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="8e5a7-118">Internamente, il filtro usa Windows Media Format SDK per scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-118">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="8e5a7-119">Il filtro gestisce tutti i dettagli di sincronizzazione audio-video, che altrimenti sarebbero responsabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-119">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="8e5a7-120">Questo processo è illustrato in modo più dettagliato nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-120">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="8e5a7-121">Sezione</span><span class="sxs-lookup"><span data-stu-id="8e5a7-121">Section</span></span>                                                                                                           | <span data-ttu-id="8e5a7-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e5a7-122">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e5a7-123">Configurazione di WM ASF Writer (QASF)</span><span class="sxs-lookup"><span data-stu-id="8e5a7-123">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="8e5a7-124">Viene descritto come configurare il filtro WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-124">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="8e5a7-125">Compilazione di grafici di filtro per la scrittura di file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="8e5a7-125">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="8e5a7-126">Viene descritto come creare grafici di transcoding e acquisizione di file.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-126">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="8e5a7-127">Configurazione di profili e altre proprietà di file (QASF)</span><span class="sxs-lookup"><span data-stu-id="8e5a7-127">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="8e5a7-128">Viene descritto come eseguire varie attività di configurazione di file ASF usando WM ASF Writer.</span><span class="sxs-lookup"><span data-stu-id="8e5a7-128">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
