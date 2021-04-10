---
title: Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)
description: Creazione di file ASF in DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, creazione di file ASF in DirectShow
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), creazione in DirectShow
- ASF (formato avanzato dei sistemi), creazione in DirectShow
- DirectShow, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118770"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="68219-110">Creazione di file ASF in DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="68219-110">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="68219-111">È possibile utilizzare DirectShow per creare file ASF direttamente da origini di acquisizione, ad esempio videocamere DV o per la transcodifica di altri file in formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="68219-111">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="68219-112">In entrambi gli scenari, le applicazioni creano grafici di filtro che includono il filtro del [writer ASF WM](wm-asf-writer-filter.md) come renderer.</span><span class="sxs-lookup"><span data-stu-id="68219-112">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="68219-113">Il writer ASF WM fornisce un wrapper parziale per Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="68219-113">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="68219-114">Le applicazioni possono utilizzare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro per passare un profilo di sistema (versioni 4, 7 o 8) oppure utilizzare direttamente Windows Media Format SDK per creare un profilo personalizzato da passare al filtro.</span><span class="sxs-lookup"><span data-stu-id="68219-114">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="68219-115">Per aggiungere metadati e altre informazioni di intestazione, l'applicazione utilizza l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , che può essere ottenuta dal filtro.</span><span class="sxs-lookup"><span data-stu-id="68219-115">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="68219-116">Dopo aver configurato il profilo e i metadati, l'applicazione può semplicemente eseguire il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="68219-116">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="68219-117">Internamente, il filtro usa Windows Media Format SDK per scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="68219-117">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="68219-118">Il filtro gestisce tutti i dettagli della sincronizzazione del video audio, che altrimenti sarebbero la responsabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68219-118">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="68219-119">Questo processo viene illustrato più dettagliatamente nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="68219-119">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="68219-120">Sezione</span><span class="sxs-lookup"><span data-stu-id="68219-120">Section</span></span>                                                                                                           | <span data-ttu-id="68219-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68219-121">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="68219-122">Configurazione del writer ASF WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="68219-122">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="68219-123">Viene descritto come configurare il filtro del writer ASF WM.</span><span class="sxs-lookup"><span data-stu-id="68219-123">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="68219-124">Creazione di grafici di filtro per la scrittura di file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="68219-124">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="68219-125">Viene descritto come creare una transcodifica di file e acquisire grafici.</span><span class="sxs-lookup"><span data-stu-id="68219-125">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="68219-126">Configurazione di profili e altre proprietà di file (QASF)</span><span class="sxs-lookup"><span data-stu-id="68219-126">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="68219-127">Viene descritto come eseguire varie attività di configurazione di file ASF usando il writer ASF WM.</span><span class="sxs-lookup"><span data-stu-id="68219-127">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
