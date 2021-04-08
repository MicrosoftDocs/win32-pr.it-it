---
title: Recupero e impostazione di metadati e attributi
description: Recupero e impostazione di metadati e attributi
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media Gestione dispositivi, attributi
- Gestione dispositivi, attributi
- applicazioni desktop, attributi
- provider di servizi, attributi
- Guida per programmatori, attributi
- attributes
- Windows Media Gestione dispositivi, metadati
- Gestione dispositivi, metadati
- applicazioni desktop, metadati
- provider di servizi, metadati
- Guida per programmatori, metadati
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856350"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="a8ef7-115">Recupero e impostazione di metadati e attributi</span><span class="sxs-lookup"><span data-stu-id="a8ef7-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="a8ef7-116">Un'applicazione può ottenere due tipi di informazioni su uno spazio di archiviazione o un dispositivo: attributi e metadati.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="a8ef7-117">Gli attributi sono valori booleani più semplici che in genere descrivono file system informazioni, ad esempio se una risorsa di archiviazione dispone di oggetti figlio, se può essere rinominata, letta o eliminata e così via.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="a8ef7-118">Gli attributi vengono recuperati come valori di flag chiamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span><span class="sxs-lookup"><span data-stu-id="a8ef7-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="a8ef7-119">Gli attributi vengono impostati chiamando [**IWMDMStorage3:: tometadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="a8ef7-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="a8ef7-120">Un'applicazione può anche richiedere dati più complessi (numerici, stringa o altri tipi di dati) come *metadati*.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="a8ef7-121">I valori dei metadati sono identificati da nomi di stringa univoci.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="a8ef7-122">Windows Media Gestione dispositivi definisce un elenco di costanti stringa che è possibile utilizzare per richiedere valori; questi valori definiti sono elencati nelle [costanti dei metadati](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a8ef7-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="a8ef7-123">Un provider di servizi può definire le proprie costanti, ma un'applicazione chiamante deve tenere conto di tali definizioni per richiedere o impostare questi valori di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="a8ef7-124">L'applicazione richiede i metadati chiamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="a8ef7-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="a8ef7-125">Un aspetto importante del recupero e dell'impostazione di metadati e attributi consiste nel comprendere la provenienza dei valori recuperati.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="a8ef7-126">Il provider di servizi o il dispositivo può ottenere questi valori da diverse posizioni, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8ef7-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="a8ef7-127">Dall'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-127">From the file header.</span></span> <span data-ttu-id="a8ef7-128">Ad esempio, in un file ASF la velocità in bit viene archiviata nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="a8ef7-129">Da valori impostati in modo esplicito dall'applicazione quando si chiama un metodo.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="a8ef7-130">Questi valori possono essere salvati in un archivio di metadati esterno nel provider di servizi o nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="a8ef7-131">Questo archivio può essere mantenuto o meno quando il dispositivo si disconnette o si spegne.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="a8ef7-132">Ad esempio, il numero di Play e le classificazioni a stelle utente vengono in genere archiviati in archivi esterni del computer o del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="a8ef7-133">Esaminando le informazioni fornite dal file system.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-133">By examining information provided by the file system.</span></span> <span data-ttu-id="a8ef7-134">Ad esempio, se un file è di sola lettura o se una cartella contiene elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="a8ef7-135">Aprendo e analizzando i dati del file.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="a8ef7-136">È importante tenere presente che una proprietà può essere archiviata in più di una posizione (all'interno dell'intestazione del file e anche in un archivio locale) e che può essere o meno modificabile.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="a8ef7-137">Ad esempio, la modifica di una descrizione di file può essere persistente; Se il provider di servizi archivia la descrizione localmente, non verrà mantenute nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="a8ef7-138">Analogamente, se la descrizione del file viene ricavata dall'intestazione del file, la modifica di questa operazione sarà permanente solo se il provider di servizi o il dispositivo viene aperto e modifica i dati dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="a8ef7-139">La maggior parte delle applicazioni esegue un tentativo migliore modificando i valori desiderati, ma non dipende da alcuna proprietà che venga modificata in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="a8ef7-140">Ulteriori informazioni su come ottenere e impostare i valori sono fornite nelle sezioni appropriate per gli sviluppatori di applicazioni e gli sviluppatori di provider di servizi più avanti nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="a8ef7-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8ef7-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8ef7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ef7-142">**Attività comuni per le applicazioni e i provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="a8ef7-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




