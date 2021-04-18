---
description: Il sink multimediale ASF è il componente finale della pipeline di codifica che consente a un'applicazione di scrivere un file ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Sink di supporti ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320692"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="ab06b-103">Sink di supporti ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-103">ASF Media Sinks</span></span>

<span data-ttu-id="ab06b-104">Il sink multimediale ASF è il componente finale della pipeline di codifica che consente a un'applicazione di scrivere un file ASF.</span><span class="sxs-lookup"><span data-stu-id="ab06b-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="ab06b-105">Media Foundation fornisce due tipi di sink di supporti ASF:</span><span class="sxs-lookup"><span data-stu-id="ab06b-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="ab06b-106">Il *sink di file ASF* viene usato per archiviare i dati del supporto ASF in un file.</span><span class="sxs-lookup"><span data-stu-id="ab06b-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="ab06b-107">Il *sink di streaming ASF* viene usato per scrivere contenuto ASF in un flusso di byte che può essere trasmesso attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="ab06b-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="ab06b-108">I sink multimediali ASF contengono uno o più sink di flusso, che rappresentano i dati da scrivere per ogni flusso nel file ASF di output.</span><span class="sxs-lookup"><span data-stu-id="ab06b-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="ab06b-109">Per la codifica di applicazioni eseguite in Windows Vista, è necessario configurare manualmente la topologia di codifica tramite la creazione e la configurazione del sink multimediale ASF e quindi l'aggiunta alla topologia.</span><span class="sxs-lookup"><span data-stu-id="ab06b-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="ab06b-110">In Windows 7, se si utilizzano gli oggetti transcode veloci per creare la topologia, non è necessario creare direttamente il sink multimediale e l'applicazione non chiama alcun metodo sul sink multimediale o su uno dei sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="ab06b-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="ab06b-111">Gli oggetti Fast transcode creano un'istanza dei sink multimediali necessari e li aggiungono alla topologia prima di restituire un riferimento all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="ab06b-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="ab06b-112">Per gli oggetti di transcodifica rapida, tuttavia, esistono alcune restrizioni che si applicano a seconda del tipo di codifica.</span><span class="sxs-lookup"><span data-stu-id="ab06b-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="ab06b-113">Modello a oggetti del sink multimediale ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="ab06b-114">Sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="ab06b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab06b-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="ab06b-116">Modello a oggetti del sink multimediale ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="ab06b-117">I sink multimediali ASF implementano l'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ed espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab06b-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="ab06b-118">Un'applicazione può ottenere un riferimento a queste interfacce chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sink multimediale ASF usato per generare esempi di output.</span><span class="sxs-lookup"><span data-stu-id="ab06b-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="ab06b-119">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ab06b-119">Interface</span></span>                                                  | <span data-ttu-id="ab06b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab06b-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab06b-121">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="ab06b-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="ab06b-122">Obbligatorio per tutti i sink di supporto.</span><span class="sxs-lookup"><span data-stu-id="ab06b-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="ab06b-123">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="ab06b-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="ab06b-124">Implementato dal sink di file ASF che scrive il contenuto multimediale generato in un file.</span><span class="sxs-lookup"><span data-stu-id="ab06b-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="ab06b-125">È possibile utilizzare i metodi su questa interfaccia per svuotare i dati e aggiornare l'oggetto intestazione ASF del file di output finale.</span><span class="sxs-lookup"><span data-stu-id="ab06b-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="ab06b-126">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="ab06b-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="ab06b-127">Riceve notifiche di modifica dello stato dal clock della presentazione.</span><span class="sxs-lookup"><span data-stu-id="ab06b-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="ab06b-128">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="ab06b-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="ab06b-129">L'oggetto di un oggetto ContentInfo ASF è un oggetto a livello di WMContainer che archivia principalmente le informazioni sull'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="ab06b-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="ab06b-130">Viene utilizzato per creare i sink di supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="ab06b-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="ab06b-131">**IMFMetadata**</span><span class="sxs-lookup"><span data-stu-id="ab06b-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="ab06b-132">Utilizzato per descrivere i metadati per il file ASF.</span><span class="sxs-lookup"><span data-stu-id="ab06b-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="ab06b-133">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="ab06b-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="ab06b-134">Recupera una raccolta di metadati per un'intera presentazione o per un flusso nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="ab06b-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="ab06b-135">Sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-135">ASF File Sink</span></span>

<span data-ttu-id="ab06b-136">Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file.</span><span class="sxs-lookup"><span data-stu-id="ab06b-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="ab06b-137">È necessario creare, configurare e chiamare metodi sul sink di file o su uno dei relativi sink di flusso se si usano gli oggetti livello pipeline per scrivere un nuovo file ASF.</span><span class="sxs-lookup"><span data-stu-id="ab06b-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="ab06b-138">Dopo aver configurato il sink di file, è possibile aggiungerlo alla pipeline di codifica.</span><span class="sxs-lookup"><span data-stu-id="ab06b-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="ab06b-139">Ecco i passaggi generali per l'uso del sink di file ASF:</span><span class="sxs-lookup"><span data-stu-id="ab06b-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="ab06b-140">Creare il sink di file in-process o out-of-process.</span><span class="sxs-lookup"><span data-stu-id="ab06b-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="ab06b-141">Configurare il sink di file con tutti i flussi, le proprietà di codifica e le informazioni sui metadati.</span><span class="sxs-lookup"><span data-stu-id="ab06b-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="ab06b-142">Associare il sink di file al nodo della topologia di output enumerando i sink del flusso o tenendo traccia dei numeri di flusso con nel sink.</span><span class="sxs-lookup"><span data-stu-id="ab06b-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="ab06b-143">Negli argomenti seguenti sono incluse informazioni dettagliate sull'utilizzo del sink di file ASF:</span><span class="sxs-lookup"><span data-stu-id="ab06b-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="ab06b-144">Creazione del sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="ab06b-145">Aggiunta di informazioni sul flusso al sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="ab06b-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="ab06b-146">Impostazione delle proprietà nel sink di file</span><span class="sxs-lookup"><span data-stu-id="ab06b-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="ab06b-147">Aggiunta di metadati al sink di file</span><span class="sxs-lookup"><span data-stu-id="ab06b-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="ab06b-148">Modello di buffer di bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="ab06b-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="ab06b-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab06b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab06b-150">Componenti ASF a livello pipeline</span><span class="sxs-lookup"><span data-stu-id="ab06b-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="ab06b-151">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab06b-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
