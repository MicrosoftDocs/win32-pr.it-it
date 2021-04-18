---
title: Guida alla programmazione di Windows Media Format SDK
description: Guida alla programmazione di Windows Media Format SDK
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- Windows Media Format SDK, guida per programmatori
- Windows Media Format SDK, Advanced Systems Format (ASF)
- ASF (Advanced Systems Format), Guida alla programmazione
- ASF (Advanced Systems Format), Guida alla programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300842"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="e42b9-107">Guida alla programmazione di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="e42b9-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="e42b9-108">La guida alla programmazione è destinata all'utilizzo di Microsoft Windows Media Format Software Development Kit (SDK) per creare applicazioni che funzionano con i file utilizzando il formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e42b9-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="e42b9-109">È possibile utilizzare Windows Media Format SDK per creare applicazioni in grado di scrivere flussi multimediali digitali e leggere flussi da file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="e42b9-110">Questo SDK supporta anche la modifica dei metadati nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="e42b9-111">Inoltre, è possibile utilizzare questo SDK per leggere e modificare i metadati in file MP3.</span><span class="sxs-lookup"><span data-stu-id="e42b9-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="e42b9-112">Le sezioni seguenti illustrano in dettaglio i passaggi necessari per scrivere, leggere e modificare i file ASF usando questo SDK.</span><span class="sxs-lookup"><span data-stu-id="e42b9-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="e42b9-113">Sezione</span><span class="sxs-lookup"><span data-stu-id="e42b9-113">Section</span></span>                                                                            | <span data-ttu-id="e42b9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e42b9-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e42b9-115">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="e42b9-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="e42b9-116">Fornisce informazioni generali su come prepararsi all'uso di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="e42b9-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="e42b9-117">Utilizzo dei metodi di callback</span><span class="sxs-lookup"><span data-stu-id="e42b9-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="e42b9-118">Vengono descritti i metodi di callback utilizzati in molte attività diverse.</span><span class="sxs-lookup"><span data-stu-id="e42b9-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="e42b9-119">Utilizzo dei profili</span><span class="sxs-lookup"><span data-stu-id="e42b9-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="e42b9-120">Viene descritto come utilizzare, modificare e creare profili.</span><span class="sxs-lookup"><span data-stu-id="e42b9-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="e42b9-121">Scrittura di file ASF</span><span class="sxs-lookup"><span data-stu-id="e42b9-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="e42b9-122">Viene descritto come utilizzare l'oggetto writer per creare file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="e42b9-123">Lettura di file ASF</span><span class="sxs-lookup"><span data-stu-id="e42b9-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="e42b9-124">Viene descritto come ricevere contenuto dai file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="e42b9-125">Utilizzo dei metadati</span><span class="sxs-lookup"><span data-stu-id="e42b9-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="e42b9-126">Viene descritto come gestire il contenuto della sezione di intestazione di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="e42b9-127">Operazioni con gli indici</span><span class="sxs-lookup"><span data-stu-id="e42b9-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="e42b9-128">Viene descritto come utilizzare gli indici.</span><span class="sxs-lookup"><span data-stu-id="e42b9-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="e42b9-129">Utilizzo dei profili</span><span class="sxs-lookup"><span data-stu-id="e42b9-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="e42b9-130">Viene descritto come utilizzare, modificare e creare profili.</span><span class="sxs-lookup"><span data-stu-id="e42b9-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="e42b9-131">Uso di comandi script</span><span class="sxs-lookup"><span data-stu-id="e42b9-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="e42b9-132">Viene descritto come utilizzare i comandi script nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="e42b9-133">Copia di dati da un file a un altro</span><span class="sxs-lookup"><span data-stu-id="e42b9-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="e42b9-134">Viene descritto come copiare i dati da un file ASF a un altro, senza decodifica e codifica.</span><span class="sxs-lookup"><span data-stu-id="e42b9-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="e42b9-135">Abilitazione del supporto DRM</span><span class="sxs-lookup"><span data-stu-id="e42b9-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="e42b9-136">Viene descritto come abilitare il supporto per la riproduzione di file ASF protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="e42b9-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="e42b9-137">Implementazione della funzionalità di rete</span><span class="sxs-lookup"><span data-stu-id="e42b9-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="e42b9-138">Descrive l'uso di questo SDK per eseguire le operazioni di rete essenziali per i flussi multimediali riusciti.</span><span class="sxs-lookup"><span data-stu-id="e42b9-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="e42b9-139">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="e42b9-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="e42b9-140">Viene descritto come utilizzare alcune delle funzionalità avanzate di questo SDK nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e42b9-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="e42b9-141">DirectShow e Windows Media</span><span class="sxs-lookup"><span data-stu-id="e42b9-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="e42b9-142">Viene descritto come è possibile utilizzare Microsoft DirectShow per creare e leggere file ASF.</span><span class="sxs-lookup"><span data-stu-id="e42b9-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="e42b9-143">Considerazioni sui progetti</span><span class="sxs-lookup"><span data-stu-id="e42b9-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="e42b9-144">Fornisce informazioni dettagliate sul completamento e la distribuzione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e42b9-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="e42b9-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e42b9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e42b9-146">**Informazioni su Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="e42b9-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="e42b9-147">**SDK di Windows Media Format 11**</span><span class="sxs-lookup"><span data-stu-id="e42b9-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




