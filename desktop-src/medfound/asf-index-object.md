---
description: Indicizzatore ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indicizzatore ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305524"
---
# <a name="asf-indexer"></a><span data-ttu-id="e6ce3-103">Indicizzatore ASF</span><span class="sxs-lookup"><span data-stu-id="e6ce3-103">ASF Indexer</span></span>

<span data-ttu-id="e6ce3-104">L' *indicizzatore* ASF è un componente di livello WMContainer che viene usato per leggere o scrivere oggetti index in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="e6ce3-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="e6ce3-105">Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e6ce3-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="e6ce3-106">Un'applicazione può utilizzare l'indicizzatore per eseguire la ricerca in base all'ora di presentazione o per generare nuove voci di indice per un file ASF.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="e6ce3-107">L'indicizzatore ASF implementa l'interfaccia [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .</span><span class="sxs-lookup"><span data-stu-id="e6ce3-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6ce3-108">Tipo di indice</span><span class="sxs-lookup"><span data-stu-id="e6ce3-108">Index type</span></span></th>
<th><span data-ttu-id="e6ce3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6ce3-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6ce3-110">Indice basato sul tempo di presentazione</span><span class="sxs-lookup"><span data-stu-id="e6ce3-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="e6ce3-111">Fornisce l'indicizzazione basata sul tempo di presentazione per i flussi audio e video nei blocchi di indice per rendere l'indicizzazione più efficiente dello spazio.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="e6ce3-112">Ogni blocco di indice fa riferimento a voci di indice che contengono un offset di byte.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="e6ce3-113">L'offset è la posizione del pacchetto di dati cercato, relativo all'inizio dell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="e6ce3-114">GUID_NULL deve essere utilizzato come tipo GUID per l'identificatore dell'indice.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="e6ce3-115">Per ulteriori informazioni, vedere <a href="using-the-indexer-to-write-a-new-index.md">uso dell'indicizzatore per scrivere un nuovo indice</a>.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6ce3-116">Indice timecode</span><span class="sxs-lookup"><span data-stu-id="e6ce3-116">Timecode Index</span></span></td>
<td><span data-ttu-id="e6ce3-117">Semplifica la ricerca in base al timecode nei flussi che contengono metadati del timecode.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="e6ce3-118">I timecode sono conformi a un formato SMPTE (<em>ore: minuti: secondi: frame</em>).</span><span class="sxs-lookup"><span data-stu-id="e6ce3-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="e6ce3-119">Ogni blocco di indice fa riferimento a voci di indice che contengono un offset di byte.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="e6ce3-120">L'offset è la posizione del pacchetto di dati cercato, relativo all'inizio dell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e6ce3-121">Gli oggetti indice del codice temporale non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6ce3-122">Indice basato su frame</span><span class="sxs-lookup"><span data-stu-id="e6ce3-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="e6ce3-123">Fornisce l'indicizzazione basata su frame per i flussi video.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="e6ce3-124">Gli indici nell'indice basato su frame sono in termini di numeri di frame, con il primo frame per un flusso nel file ASF corrispondente alla voce 0 nell'oggetto indice basato su frame.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="e6ce3-125">Ogni blocco di indice fa riferimento a voci di indice che contengono un offset di byte.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e6ce3-126">Gli oggetti indice basati su frame non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e6ce3-127">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-127">This section contains the following topics.</span></span>



| <span data-ttu-id="e6ce3-128">Argomento</span><span class="sxs-lookup"><span data-stu-id="e6ce3-128">Topic</span></span>                                                                                | <span data-ttu-id="e6ce3-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6ce3-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6ce3-130">Creazione e configurazione dell'indicizzatore</span><span class="sxs-lookup"><span data-stu-id="e6ce3-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="e6ce3-131">Come creare un oggetto indicizzatore e configurarlo per la lettura di un indice esistente o per la scrittura di un nuovo oggetto indice ASF per un file.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="e6ce3-132">Uso dell'indicizzatore per la ricerca in un file</span><span class="sxs-lookup"><span data-stu-id="e6ce3-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="e6ce3-133">Come utilizzare l'indicizzatore per la ricerca all'interno di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="e6ce3-134">Uso dell'indicizzatore per scrivere un nuovo indice</span><span class="sxs-lookup"><span data-stu-id="e6ce3-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="e6ce3-135">Come utilizzare l'indicizzatore per generare voci di indice e scrivere un nuovo oggetto index per un file ASF.</span><span class="sxs-lookup"><span data-stu-id="e6ce3-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="e6ce3-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6ce3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ce3-137">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="e6ce3-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="e6ce3-138">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6ce3-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




