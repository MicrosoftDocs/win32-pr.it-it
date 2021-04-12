---
title: Accesso a metadati e attributi nell'app
description: Recupero e impostazione di metadati e attributi nell'applicazione
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Media Gestione dispositivi, metadati
- Gestione dispositivi, metadati
- Guida per programmatori, metadati
- applicazioni desktop, metadati
- creazione di applicazioni Windows Media Gestione dispositivi, metadati
- metadata
- Windows Media Gestione dispositivi, attributi
- Gestione dispositivi, attributi
- Guida per programmatori, attributi
- applicazioni desktop, attributi
- creazione di applicazioni Windows Media Gestione dispositivi, attributi
- attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104335764"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="1fce3-115">Accesso a metadati e attributi nell'app</span><span class="sxs-lookup"><span data-stu-id="1fce3-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="1fce3-116">Una discussione generale sui metadati e sugli attributi è disponibile in [recupero e impostazione di metadati e attributi](getting-and-setting-metadata-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1fce3-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="1fce3-117">In questa sezione vengono illustrate le chiamate al metodo dell'applicazione specifiche per recuperare o impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="1fce3-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="1fce3-118">Le applicazioni possono recuperare gli attributi o i metadati relativi a un'archiviazione specifica chiamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="1fce3-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="1fce3-119">**GetMetadata** recupera una raccolta completa di tutti i metadati associati a una risorsa di archiviazione e l'applicazione può quindi enumerare tutti i valori o richiedere valori specifici dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="1fce3-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="1fce3-120">**GetSpecifiedMetadata** crea un oggetto di metadati per conto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="1fce3-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="1fce3-121">Il chiamante può richiedere un subset dei dati disponibili compilando il parametro *ppwszPropNames* con una matrice delle stringhe di proprietà Windows Media Gestione dispositivi desiderate e il conteggio di tale matrice.</span><span class="sxs-lookup"><span data-stu-id="1fce3-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="1fce3-122">L'oggetto di metadati restituito verrà compilato con le proprietà che possono essere recuperate.</span><span class="sxs-lookup"><span data-stu-id="1fce3-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="1fce3-123">Non è possibile recuperare le proprietà che non possono essere recuperate.</span><span class="sxs-lookup"><span data-stu-id="1fce3-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="1fce3-124">I metadati vengono restituiti in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="1fce3-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="1fce3-125">Un dispositivo può impostare attributi o metadati in un'archiviazione chiamando [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)o [**IWMDMStorage3::**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="1fce3-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="1fce3-126">Si noti che non esiste alcuna garanzia che i valori impostati siano persistenti, perché possono essere archiviati in un archivio di file esterno non persistente, i valori potrebbero non essere supportati o, il dispositivo potrebbe non supportare le proprietà come scrivibili.</span><span class="sxs-lookup"><span data-stu-id="1fce3-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="1fce3-127">È anche possibile ottenere o impostare i metadati relativi a un dispositivo chiamando [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) o [**IWMDMDevice3:: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="1fce3-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="1fce3-128">Alla fine delle [costanti dei metadati](metadata-constants.md)è presente una tabella separata di costanti dei metadati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1fce3-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="1fce3-129">Esempi di utilizzo di questi metodi sono forniti nella documentazione di riferimento di ciascun metodo.</span><span class="sxs-lookup"><span data-stu-id="1fce3-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fce3-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fce3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fce3-131">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="1fce3-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="1fce3-132">**Recupero e impostazione di metadati e attributi**</span><span class="sxs-lookup"><span data-stu-id="1fce3-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




