---
title: Utilizzo dei sink di writer
description: Utilizzo dei sink di writer
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), sink writer
- ASF (formato avanzato dei sistemi), sink writer
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, sink di writer
- sink writer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723367"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="9d4de-109">Utilizzo dei sink di writer</span><span class="sxs-lookup"><span data-stu-id="9d4de-109">Working with Writer Sinks</span></span>

<span data-ttu-id="9d4de-110">L'oggetto writer di Windows Media Format SDK elabora i dati multimediali di input in un flusso di bit.</span><span class="sxs-lookup"><span data-stu-id="9d4de-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="9d4de-111">Tuttavia, l'oggetto writer non distribuisce il flusso di bit alla destinazione finale, ovvero in un file o in un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="9d4de-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="9d4de-112">Per scrivere il contenuto ASF in un formato utilizzabile, è necessario utilizzare i sink del writer.</span><span class="sxs-lookup"><span data-stu-id="9d4de-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="9d4de-113">L'oggetto Writer supporta tre tipi di sink: sink di file, sink di rete e sink di push.</span><span class="sxs-lookup"><span data-stu-id="9d4de-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="9d4de-114">Un sink di file scrive il contenuto ASF in un file ASF su disco.</span><span class="sxs-lookup"><span data-stu-id="9d4de-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="9d4de-115">Un sink di rete trasmette contenuto ASF da un indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="9d4de-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="9d4de-116">Un sink di push recapita i dati a un server che esegue Servizi Windows Media, in modo che il server possa rendere il contenuto disponibile ai destinatari desiderati.</span><span class="sxs-lookup"><span data-stu-id="9d4de-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="9d4de-117">È anche possibile creare sink personalizzati per distribuire i dati ASF nel modo desiderato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d4de-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="9d4de-118">Per informazioni sui sink di rete e sui sink di push, vedere [invio di dati ASF in una rete](sending-asf-data-over-a-network.md).</span><span class="sxs-lookup"><span data-stu-id="9d4de-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="9d4de-119">Nella parte restante di questa sezione vengono illustrati i sink di writer.</span><span class="sxs-lookup"><span data-stu-id="9d4de-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="9d4de-120">È possibile configurare uno o più sink per ogni istanza del writer usato.</span><span class="sxs-lookup"><span data-stu-id="9d4de-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="9d4de-121">Ogni sink gestisce solo una singola destinazione.</span><span class="sxs-lookup"><span data-stu-id="9d4de-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="9d4de-122">Se ad esempio si desidera scrivere tre file in una sola volta, è necessario creare e configurare un sink di file separato per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="9d4de-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="9d4de-123">Le sezioni seguenti descrivono l'uso di sink di writer.</span><span class="sxs-lookup"><span data-stu-id="9d4de-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="9d4de-124">Sezione</span><span class="sxs-lookup"><span data-stu-id="9d4de-124">Section</span></span>                                                                      | <span data-ttu-id="9d4de-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d4de-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9d4de-126">Aggiunta di sink al writer</span><span class="sxs-lookup"><span data-stu-id="9d4de-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="9d4de-127">Viene descritto come aggiungere sink al writer.</span><span class="sxs-lookup"><span data-stu-id="9d4de-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="9d4de-128">Enumerazione dei sink</span><span class="sxs-lookup"><span data-stu-id="9d4de-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="9d4de-129">Viene descritto come enumerare i sink aggiunti al writer.</span><span class="sxs-lookup"><span data-stu-id="9d4de-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="9d4de-130">Recupero di messaggi di errore da un sink</span><span class="sxs-lookup"><span data-stu-id="9d4de-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="9d4de-131">Viene descritto come configurare i sink per inviare messaggi di stato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d4de-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="9d4de-132">Uso di file sink</span><span class="sxs-lookup"><span data-stu-id="9d4de-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="9d4de-133">Viene descritto come utilizzare un sink di file del writer per creare un file ASF su disco.</span><span class="sxs-lookup"><span data-stu-id="9d4de-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="9d4de-134">Uso di sink personalizzati</span><span class="sxs-lookup"><span data-stu-id="9d4de-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="9d4de-135">Viene descritto come creare e utilizzare i sink personalizzati per fornire dati ASF.</span><span class="sxs-lookup"><span data-stu-id="9d4de-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="9d4de-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d4de-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d4de-137">**Interfaccia IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="9d4de-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="9d4de-138">**Interfaccia IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="9d4de-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="9d4de-139">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="9d4de-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




