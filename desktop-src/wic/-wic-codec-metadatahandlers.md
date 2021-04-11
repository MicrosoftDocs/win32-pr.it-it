---
description: In questo argomento vengono introdotti i requisiti per la creazione di gestori di metadati personalizzati per il componente di imaging Windows (WIC), inclusi i reader di metadati e i writer.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Panoramica dell'estendibilità dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232323"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="35818-103">Panoramica dell'estendibilità dei metadati</span><span class="sxs-lookup"><span data-stu-id="35818-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="35818-104">In questo argomento vengono introdotti i requisiti per la creazione di gestori di metadati personalizzati per il componente di imaging Windows (WIC), inclusi i reader di metadati e i writer.</span><span class="sxs-lookup"><span data-stu-id="35818-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="35818-105">Vengono inoltre illustrati i requisiti per estendere l'individuazione dei componenti in fase di esecuzione di WIC per includere i gestori di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="35818-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="35818-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="35818-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="35818-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="35818-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="35818-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="35818-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="35818-109">Creazione di un lettore di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="35818-110">Interfaccia IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="35818-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="35818-111">Interfaccia IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="35818-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="35818-112">Interfaccia IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="35818-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="35818-113">Creazione di un writer di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="35818-114">Interfaccia IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="35818-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="35818-115">Interfaccia IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="35818-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="35818-116">Interfaccia IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="35818-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="35818-117">Installazione e registrazione di un gestore di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="35818-118">Chiavi del registro di sistema del gestore dei metadati</span><span class="sxs-lookup"><span data-stu-id="35818-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="35818-119">Lettori di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="35818-120">Writer di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="35818-121">Firma di un gestore di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="35818-122">Considerazioni speciali</span><span class="sxs-lookup"><span data-stu-id="35818-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="35818-123">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="35818-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="35818-124">Gestori 8BIM</span><span class="sxs-lookup"><span data-stu-id="35818-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="35818-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35818-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="35818-126">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="35818-126">Prerequisites</span></span>

<span data-ttu-id="35818-127">Per comprendere questo argomento, è necessario avere una conoscenza approfondita di WIC, dei relativi componenti e dei metadati per le immagini.</span><span class="sxs-lookup"><span data-stu-id="35818-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="35818-128">Per ulteriori informazioni sui metadati WIC, vedere [Cenni preliminari sui metadati WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="35818-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="35818-129">Per ulteriori informazioni sui componenti WIC, vedere [Cenni preliminari sul componente Windows Imaging](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="35818-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="35818-130">Introduzione</span><span class="sxs-lookup"><span data-stu-id="35818-130">Introduction</span></span>

<span data-ttu-id="35818-131">Come illustrato nella [Panoramica dei metadati di WIC](-wic-about-metadata.md), spesso sono presenti più blocchi di metadati all'interno di un'immagine, ognuno dei quali espone tipi diversi di informazioni in formati di metadati diversi.</span><span class="sxs-lookup"><span data-stu-id="35818-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="35818-132">Per interagire con un formato di metadati incorporato in un'immagine, un'applicazione deve usare un gestore di metadati appropriato.</span><span class="sxs-lookup"><span data-stu-id="35818-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="35818-133">WIC fornisce diversi gestori di metadati (Reader di metadati e writer) che consentono di leggere e scrivere tipi specifici di metadati, ad esempio EXIF o XMP.</span><span class="sxs-lookup"><span data-stu-id="35818-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="35818-134">Oltre ai gestori nativi forniti, WIC fornisce le API che consentono di creare nuovi gestori di metadati che fanno parte dell'individuazione del componente runtime di WIC.</span><span class="sxs-lookup"><span data-stu-id="35818-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="35818-135">Ciò consente alle applicazioni che utilizzano WIC di leggere e scrivere formati di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="35818-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="35818-136">I passaggi seguenti consentono ai gestori di metadati di partecipare all'individuazione dei metadati di run-time di WIC.</span><span class="sxs-lookup"><span data-stu-id="35818-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="35818-137">Implementare una classe del gestore di lettura dei metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) che espone le interfacce WIC necessarie per la lettura del formato di metadati personalizzato.</span><span class="sxs-lookup"><span data-stu-id="35818-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="35818-138">Ciò consente alle applicazioni basate su WIC di leggere il formato dei metadati nello stesso modo in cui leggono i formati di metadati nativi.</span><span class="sxs-lookup"><span data-stu-id="35818-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="35818-139">Implementare una classe di gestori di writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) che espone le interfacce WIC necessarie per la codifica del formato di metadati personalizzato.</span><span class="sxs-lookup"><span data-stu-id="35818-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="35818-140">Ciò consente alle applicazioni basate su WIC di serializzare il formato dei metadati in formati di immagine supportati.</span><span class="sxs-lookup"><span data-stu-id="35818-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="35818-141">Firmare digitalmente e registrare i gestori di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="35818-142">In questo modo i gestori dei metadati possono essere individuati in fase di esecuzione associando il modello di identificazione nel registro di sistema al modello incorporato nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="35818-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="35818-143">Creazione di un lettore di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="35818-144">L'accesso principale ai blocchi di metadati all'interno di un codec è tramite l'interfaccia [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementata da ciascun codec WIC.</span><span class="sxs-lookup"><span data-stu-id="35818-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="35818-145">Questa interfaccia enumera tutti i blocchi di metadati incorporati in un formato di immagine in modo che sia possibile individuare e creare un'istanza del gestore di metadati appropriato per ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="35818-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="35818-146">I blocchi di metadati non riconosciuti da WIC sono considerati sconosciuti e sono definiti come CLSID GUID \_ WICUnknownMetadataReader.</span><span class="sxs-lookup"><span data-stu-id="35818-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="35818-147">Per fare in modo che il formato dei metadati venga riconosciuto da WIC, è necessario creare una classe che implementi tre interfacce: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="35818-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="35818-148">Se il formato dei metadati presenta restrizioni che eseguono il rendering di alcuni metodi delle interfacce richieste inappropriate, tali metodi devono restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="35818-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="35818-149">Interfaccia IWICMetadataReader</span><span class="sxs-lookup"><span data-stu-id="35818-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="35818-150">L'interfaccia [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) deve essere implementata quando si crea un lettore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="35818-151">Questa interfaccia fornisce l'accesso agli elementi di metadati sottoposti all'interno del flusso di dati di un formato di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="35818-152">Nel codice seguente viene illustrata la definizione dell'interfaccia del lettore di metadati come definito nel file wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="35818-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="35818-153">Il metodo **GetMetadataFormat** restituisce il GUID del formato dei metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="35818-154">Il metodo **GetMetadataHandlerInfo** restituisce un'interfaccia [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) che fornisce informazioni sul gestore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="35818-155">Sono incluse informazioni quali i formati di immagine che supportano il formato dei metadati e il fatto che il lettore di metadati debba accedere al flusso di metadati completo.</span><span class="sxs-lookup"><span data-stu-id="35818-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="35818-156">Il metodo **GetCount** restituisce il numero di singoli elementi di metadati (compresi i blocchi di metadati incorporati) trovati all'interno del flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="35818-157">Il metodo **GetValueByIndex** restituisce un elemento di metadati in base a un valore di indice.</span><span class="sxs-lookup"><span data-stu-id="35818-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="35818-158">Questo metodo consente alle applicazioni di scorrere in ciclo ogni elemento di metadati in un blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="35818-159">Nel codice seguente viene illustrato come un'applicazione può utilizzare questo metodo per recuperare ogni elemento di metadati in un blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="35818-160">Il metodo **GetValue** recupera un elemento di metadati specifico per schema e/o ID.</span><span class="sxs-lookup"><span data-stu-id="35818-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="35818-161">Questo metodo è simile al metodo **GetValueByIndex** , con la differenza che recupera un elemento di metadati con uno schema o un ID specifico.</span><span class="sxs-lookup"><span data-stu-id="35818-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="35818-162">Il metodo **GetEnumerator** restituisce un enumeratore di ogni elemento di metadati nel blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="35818-163">Ciò consente alle applicazioni di utilizzare un enumeratore per esplorare il formato dei metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="35818-164">Se il formato dei metadati non ha una nozione di schemi per gli elementi di metadati, GetValue... i metodi devono ignorare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="35818-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="35818-165">Se, tuttavia, il formato supporta la denominazione dello schema, è necessario prevedere un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="35818-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="35818-166">Se un elemento dei metadati è un blocco di metadati incorporato, creare un gestore di metadati dal sottoflusso del contenuto incorporato e restituire il nuovo gestore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="35818-167">Se non è disponibile alcun lettore di metadati per il blocco annidato, creare un'istanza di e restituire un lettore di metadati sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="35818-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="35818-168">Per creare un nuovo lettore di metadati per il blocco incorporato, chiamare i metodi **CreateMetadataReaderFromContainer** o **CreateMetadataReader** della factory del componente oppure chiamare la funzione [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .</span><span class="sxs-lookup"><span data-stu-id="35818-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="35818-169">Se il flusso di metadati contiene contenuto big endian, il lettore di metadati è responsabile dello scambio di tutti i valori di dati elaborati.</span><span class="sxs-lookup"><span data-stu-id="35818-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="35818-170">È anche responsabile di informare i lettori di metadati annidati che lavorano con il flusso di dati big-endian.</span><span class="sxs-lookup"><span data-stu-id="35818-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="35818-171">Tuttavia, tutti i valori devono essere restituiti in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="35818-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="35818-172">Implementare il supporto per la navigazione dello spazio dei nomi supportando le query in cui l'ID elemento dei metadati è un `VT_CLSID` (Guid) corrispondente a un formato di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="35818-173">Se un lettore di metadati annidati per tale formato viene identificato durante l'analisi, deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="35818-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="35818-174">Ciò consente alle applicazioni di utilizzare un lettore di query di metadati per eseguire ricerche nel formato dei metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="35818-175">Quando si recupera un elemento di metadati in base all'ID, è necessario utilizzare la [funzione PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) per assegnare l'ID al tipo previsto.</span><span class="sxs-lookup"><span data-stu-id="35818-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="35818-176">Il lettore IFD, ad esempio, forza l'assegnazione di un ID al tipo `VT_UI2` in concomitanza con il tipo di dati di un ID di tag IFD UShort.</span><span class="sxs-lookup"><span data-stu-id="35818-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="35818-177">Per eseguire questa operazione, è necessario che il tipo di input e il tipo previsto siano [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="35818-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="35818-178">Questa operazione non è necessaria, ma questa coercizione semplifica il codice che chiama il Reader per eseguire una query per gli elementi di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="35818-179">Interfaccia IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="35818-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="35818-180">L'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) eredita da **IPersistStream** e fornisce metodi aggiuntivi per il salvataggio e il caricamento di oggetti tramite l'enumerazione [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="35818-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="35818-181">Nel codice seguente viene illustrata la definizione dell'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) come definito nel file wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="35818-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="35818-182">Il metodo **LoadEx** fornisce al lettore di metadati un flusso di dati contenente il blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="35818-183">Il lettore analizza questo flusso per accedere agli elementi di metadati sottostanti.</span><span class="sxs-lookup"><span data-stu-id="35818-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="35818-184">Il lettore di metadati viene inizializzato con un sottoflusso posizionato all'inizio del contenuto dei metadati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="35818-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="35818-185">Se il lettore non richiede il flusso completo, il sottoflusso è limitato nell'intervallo al solo contenuto del blocco di metadati. in caso contrario, il flusso di metadati completo viene fornito con la posizione impostata all'inizio del blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="35818-186">Il metodo **SaveEx** viene utilizzato dai writer di metadati per serializzare il blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="35818-187">Quando **SaveEx** viene utilizzato in un lettore di metadati, deve restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="35818-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="35818-188">Interfaccia IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="35818-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="35818-189">L'interfaccia [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) consente al lettore di metadati di fornire riferimenti al relativo flusso di contenuto, fornire informazioni sul flusso e aggiornare le versioni memorizzate nella cache del flusso.</span><span class="sxs-lookup"><span data-stu-id="35818-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="35818-190">Nel codice seguente viene illustrata la definizione dell'interfaccia [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) come definito nel file wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="35818-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="35818-191">Il metodo **GetStream** recupera un riferimento al flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="35818-192">Il flusso restituito deve avere il puntatore del flusso reimpostato sulla posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="35818-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="35818-193">Se il formato dei metadati richiede l'accesso completo al flusso, la posizione iniziale deve essere l'inizio del blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="35818-194">Il metodo **GetPersistOptions** restituisce le opzioni correnti del flusso dall'enumerazione [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="35818-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="35818-195">Il metodo **GetPreferredVendorGUID** restituisce il GUID del fornitore del lettore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="35818-196">Il metodo **RefreshStream** aggiorna il flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="35818-197">Questo metodo deve chiamare **LoadEx** con un flusso **null** per qualsiasi blocco di metadati annidato.</span><span class="sxs-lookup"><span data-stu-id="35818-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="35818-198">Questa operazione è necessaria perché i blocchi di metadati annidati e i relativi elementi potrebbero non esistere più, a causa della modifica sul posto.</span><span class="sxs-lookup"><span data-stu-id="35818-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="35818-199">Creazione di un writer di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="35818-200">Un writer di metadati è un tipo di gestore di metadati che fornisce un modo per serializzare un blocco di metadati in un frame immagine o all'esterno di un singolo frame se il formato dell'immagine lo supporta.</span><span class="sxs-lookup"><span data-stu-id="35818-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="35818-201">L'accesso principale ai writer di metadati all'interno di un codec è tramite l'interfaccia [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) implementata da ciascun codificatore WIC.</span><span class="sxs-lookup"><span data-stu-id="35818-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="35818-202">Questa interfaccia consente alle applicazioni di enumerare ogni blocco di metadati incorporato in un'immagine in modo che il writer di metadati appropriato possa essere individuato e di cui è stata creata un'istanza per ogni blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="35818-203">I blocchi di metadati che non dispongono di un writer di metadati corrispondente sono considerati sconosciuti e sono definiti come CLSID GUID \_ WICUnknownMetadataReader.</span><span class="sxs-lookup"><span data-stu-id="35818-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="35818-204">Per abilitare le applicazioni abilitate per WIC per la serializzazione e la scrittura del formato dei metadati, è necessario creare una classe che implementi le interfacce seguenti: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)e [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="35818-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="35818-205">Se il formato dei metadati presenta restrizioni che eseguono il rendering di alcuni metodi delle interfacce richieste inappropriate, tali metodi devono restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="35818-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="35818-206">Interfaccia IWICMetadataWriter</span><span class="sxs-lookup"><span data-stu-id="35818-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="35818-207">L'interfaccia [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) deve essere implementata dal writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="35818-208">Poiché **IWICMetadataWriter** eredita da [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), è inoltre necessario implementare tutti i metodi di **IWICMetadataReader**.</span><span class="sxs-lookup"><span data-stu-id="35818-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="35818-209">Poiché entrambi i tipi di gestori richiedono la stessa ereditarietà dell'interfaccia, potrebbe essere necessario creare una singola classe che fornisca la funzionalità di lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="35818-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="35818-210">Nel codice seguente viene illustrata la definizione dell'interfaccia del writer dei metadati come definito nel file wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="35818-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="35818-211">Il metodo **SetValue** scrive l'elemento dei metadati specificato nel flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="35818-212">Il metodo **SetValueByIndex** scrive l'elemento dei metadati specificato nell'indice specificato nel flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="35818-213">L'indice non fa riferimento all'ID ma alla posizione dell'elemento all'interno del blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="35818-214">Il metodo **RemoveValue** rimuove l'elemento di metadati specificato dal flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="35818-215">Il metodo **RemoveValueByIndex** rimuove l'elemento di metadati in corrispondenza dell'indice specificato dal flusso di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="35818-216">Dopo la rimozione di un elemento, è previsto che gli elementi dei metadati rimanenti occupino l'indice sgomberato se l'indice non è l'ultimo indice.</span><span class="sxs-lookup"><span data-stu-id="35818-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="35818-217">Si prevede anche che il conteggio cambierà dopo la rimozione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="35818-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="35818-218">È responsabilità del writer dei metadati convertire gli elementi [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) nella struttura sottostante richiesta dal formato.</span><span class="sxs-lookup"><span data-stu-id="35818-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="35818-219">Tuttavia, a differenza del lettore di metadati, i tipi VARIANT non devono essere in genere assegnati a tipi diversi perché il chiamante indica in modo specifico il tipo di dati da usare.</span><span class="sxs-lookup"><span data-stu-id="35818-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="35818-220">Il writer di metadati deve eseguire il commit di tutti gli elementi di metadati nel flusso dell'immagine, inclusi i valori nascosti o non riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="35818-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="35818-221">Sono inclusi i blocchi di metadati annidati sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="35818-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="35818-222">Tuttavia, è responsabilità del codificatore impostare gli elementi di metadati critici prima di avviare l'operazione di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="35818-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="35818-223">Se il flusso di metadati contiene contenuto big endian, il writer dei metadati è responsabile dello scambio di tutti i valori di dati elaborati.</span><span class="sxs-lookup"><span data-stu-id="35818-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="35818-224">È anche responsabile di informare eventuali writer di metadati annidati che utilizzano un flusso di dati Big-Endian quando vengono salvati.</span><span class="sxs-lookup"><span data-stu-id="35818-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="35818-225">Implementare il supporto per la creazione e la rimozione dello spazio dei nomi supportando operazioni set e Remove sugli elementi di metadati con un tipo di `VT_CLSID` (Guid) corrispondente a un formato di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="35818-226">Il writer di metadati chiama la funzione [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) per incorporare correttamente il contenuto del writer di metadati annidato nel writer di metadati padre.</span><span class="sxs-lookup"><span data-stu-id="35818-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="35818-227">Se il formato dei metadati supporta la codifica sul posto, si è responsabili della gestione della spaziatura interna necessaria.</span><span class="sxs-lookup"><span data-stu-id="35818-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="35818-228">Per ulteriori informazioni sulla codifica sul posto, vedere [Cenni preliminari sui metadati WIC](-wic-about-metadata.md) e [Cenni preliminari sulla lettura e scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="35818-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="35818-229">Interfaccia IWICPersistStream</span><span class="sxs-lookup"><span data-stu-id="35818-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="35818-230">L'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) eredita da **IPersistStream** e fornisce metodi aggiuntivi per il salvataggio e il caricamento di oggetti tramite l'enumerazione [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="35818-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="35818-231">Nel codice seguente viene illustrata la definizione dell'interfaccia [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) come definito nel file wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="35818-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="35818-232">Il metodo **LoadEx** fornisce al gestore di metadati un flusso di dati contenente il blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="35818-233">Il metodo **SaveEx** serializza i metadati in un flusso.</span><span class="sxs-lookup"><span data-stu-id="35818-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="35818-234">Se il flusso specificato è uguale al flusso di inizializzazione, è consigliabile eseguire la codifica sul posto.</span><span class="sxs-lookup"><span data-stu-id="35818-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="35818-235">Se è supportata la codifica sul posto, questo metodo deve restituire WINCODEC \_ Err \_ TOOMUCHMETADATA quando la spaziatura interna non è sufficiente per eseguire la codifica sul posto.</span><span class="sxs-lookup"><span data-stu-id="35818-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="35818-236">Se la codifica sul posto non è supportata, questo metodo deve restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="35818-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="35818-237">Il metodo **IPersistStream:: GetSizeMax** deve essere implementato e deve restituire la dimensione esatta del contenuto dei metadati che verrà scritto nel salvataggio successivo.</span><span class="sxs-lookup"><span data-stu-id="35818-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="35818-238">È necessario implementare il metodo **IPersistStream:: IsDirty** se il writer dei metadati viene inizializzato tramite un flusso, in modo che un'immagine possa determinare in modo affidabile se il relativo contenuto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="35818-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="35818-239">Se il formato dei metadati supporta i blocchi di metadati annidati, il writer di metadati deve delegare ai writer di metadati annidati la serializzazione del contenuto durante il salvataggio in un flusso.</span><span class="sxs-lookup"><span data-stu-id="35818-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="35818-240">Interfaccia IWICStreamProvider</span><span class="sxs-lookup"><span data-stu-id="35818-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="35818-241">L'implementazione dell'interfaccia [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) per un writer di metadati è identica a quella di un lettore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="35818-242">Per ulteriori informazioni, vedere la sezione Creazione di un lettore di metadati in questo documento.</span><span class="sxs-lookup"><span data-stu-id="35818-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="35818-243">Installazione e registrazione di un gestore di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="35818-244">Per installare un gestore di metadati, è necessario fornire l'assembly del gestore e registrarlo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="35818-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="35818-245">È possibile decidere come e quando vengono popolate le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="35818-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="35818-246">Per migliorare la leggibilità, i GUID esadecimali effettivi non vengono visualizzati nelle chiavi del registro di sistema illustrate nelle sezioni seguenti di questo documento.</span><span class="sxs-lookup"><span data-stu-id="35818-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="35818-247">Per trovare il valore esadecimale per un nome descrittivo specificato, vedere i file wincodec. idl e wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="35818-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="35818-248">Chiavi del registro di sistema del gestore dei metadati</span><span class="sxs-lookup"><span data-stu-id="35818-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="35818-249">Ogni gestore di metadati è identificato da un CLSID univoco e ogni gestore è necessario per registrare il relativo CLSID sotto il GUID dell'ID di categoria del gestore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="35818-250">Ogni ID di categoria del tipo di gestore è definito in wincodec. idl; il nome dell'ID categoria per i lettori è CATId \_ WICMetadataReader e il nome ID categoria per Writers è CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="35818-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="35818-251">Ogni gestore di metadati è identificato da un CLSID univoco e ogni gestore è necessario per registrare il relativo CLSID sotto il GUID dell'ID di categoria del gestore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="35818-252">Ogni ID di categoria del tipo di gestore è definito in wincodec. idl; il nome dell'ID categoria per i lettori è CATId \_ WICMetadataReader e il nome ID categoria per Writers è CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="35818-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="35818-253">Negli elenchi di chiavi del registro di sistema seguenti, {Reader CLSID} fa riferimento al CLSID univoco fornito per il lettore di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="35818-254">{Writer CLSID} fa riferimento al CLSID univoco fornito per il writer di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="35818-255">{Handler CLSID} fa riferimento al CLSID del Reader, al CLSID del writer o a entrambi, a seconda dei gestori che vengono fornite.</span><span class="sxs-lookup"><span data-stu-id="35818-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="35818-256">{Container GUID} fa riferimento all'oggetto contenitore (formato di immagine o formato dei metadati) che può contenere il blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="35818-257">Le chiavi del registro di sistema seguenti registrano il gestore di metadati con gli altri gestori di metadati disponibili:</span><span class="sxs-lookup"><span data-stu-id="35818-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="35818-258">Oltre a registrare i gestori nelle rispettive categorie, è necessario registrare anche chiavi aggiuntive che forniscono informazioni specifiche per il gestore.</span><span class="sxs-lookup"><span data-stu-id="35818-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="35818-259">I lettori e i writer condividono requisiti di chiave del registro di sistema simili.</span><span class="sxs-lookup"><span data-stu-id="35818-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="35818-260">Nella sintassi seguente viene illustrato come registrare un gestore.</span><span class="sxs-lookup"><span data-stu-id="35818-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="35818-261">Il gestore del lettore e il gestore del writer devono essere registrati in questo modo, usando i rispettivi CLSID:</span><span class="sxs-lookup"><span data-stu-id="35818-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="35818-262">Lettori di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-262">Metadata Readers</span></span>

<span data-ttu-id="35818-263">La registrazione del lettore di metadati include anche chiavi che descrivono come è possibile incorporare il Reader in un formato di contenitore.</span><span class="sxs-lookup"><span data-stu-id="35818-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="35818-264">Un formato di contenitore può essere un formato di immagine, ad esempio TIFF o JPEG. può anche essere un altro formato di metadati, ad esempio un blocco di metadati IFD.</span><span class="sxs-lookup"><span data-stu-id="35818-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="35818-265">I formati di contenitori di immagini supportati in modo nativo sono elencati in wincodec. idl; ogni formato di contenitore di immagini viene definito come GUID con un nome che inizia con GUID \_ containerFormat.</span><span class="sxs-lookup"><span data-stu-id="35818-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="35818-266">I formati di contenitori di metadati supportati in modo nativo sono elencati in wincodecsdk. idl; ogni formato di contenitore di metadati viene definito come GUID con un nome che inizia con GUID \_ MetadataFormat.</span><span class="sxs-lookup"><span data-stu-id="35818-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="35818-267">Le chiavi seguenti registrano un contenitore supportato dal lettore di metadati e i dati necessari per la lettura da tale contenitore.</span><span class="sxs-lookup"><span data-stu-id="35818-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="35818-268">Ogni contenitore supportato dal reader deve essere registrato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="35818-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="35818-269">La chiave del modello descrive il modello binario utilizzato per associare il blocco di metadati al lettore.</span><span class="sxs-lookup"><span data-stu-id="35818-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="35818-270">Quando si definisce un modello per il lettore di metadati, è consigliabile che il lettore dei metadati possa comprendere i metadati nel blocco di metadati in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="35818-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="35818-271">La chiave dataOffset descrive l'offset fisso dei metadati dall'intestazione del blocco.</span><span class="sxs-lookup"><span data-stu-id="35818-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="35818-272">Questa chiave è facoltativa e, se non specificata, significa che i metadati effettivi non possono essere individuati usando un offset fisso dall'intestazione del blocco.</span><span class="sxs-lookup"><span data-stu-id="35818-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="35818-273">Writer di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-273">Metadata Writers</span></span>

<span data-ttu-id="35818-274">La registrazione del writer dei metadati include anche chiavi che descrivono come scrivere l'intestazione che precede il contenuto dei metadati incorporato in un formato di contenitore.</span><span class="sxs-lookup"><span data-stu-id="35818-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="35818-275">Come nel lettore, un formato di contenitore può essere un formato di immagine o un altro blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="35818-276">Le chiavi seguenti registrano un contenitore supportato dal writer di metadati e i dati necessari per scrivere l'intestazione e i metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="35818-277">Ogni contenitore supportato dal writer deve essere registrato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="35818-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="35818-278">La chiave WriteHeader descrive il modello binario dell'intestazione del blocco di metadati da scrivere.</span><span class="sxs-lookup"><span data-stu-id="35818-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="35818-279">Questo schema binario coincide con la chiave del pattern Reader del formato dei metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="35818-280">La chiave WriteOffset descrive l'offset fisso dall'intestazione del blocco in cui devono essere scritti i metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="35818-281">Questa chiave è facoltativa e, se non specificata, significa che i metadati effettivi non devono essere scritti con l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="35818-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="35818-282">Firma di un gestore di metadati</span><span class="sxs-lookup"><span data-stu-id="35818-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="35818-283">Tutti i gestori di metadati devono essere firmati digitalmente per partecipare al processo di individuazione WIC.</span><span class="sxs-lookup"><span data-stu-id="35818-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="35818-284">Per WIC non verrà caricato alcun gestore non firmato da un'autorità di certificazione attendibile.</span><span class="sxs-lookup"><span data-stu-id="35818-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="35818-285">Per ulteriori informazioni sulla firma digitale, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35818-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="35818-286">Considerazioni speciali</span><span class="sxs-lookup"><span data-stu-id="35818-286">Special Considerations</span></span>

<span data-ttu-id="35818-287">Le sezioni seguenti includono informazioni aggiuntive che è necessario prendere in considerazione durante la creazione di gestori di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="35818-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="35818-288">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="35818-288">PROPVARIANTS</span></span>

<span data-ttu-id="35818-289">WIC usa un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) per rappresentare un elemento di metadati sia per la lettura che per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="35818-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="35818-290">Un PROPVARIANT fornisce un tipo di dati e un valore di dati per un elemento di metadati utilizzato in un formato di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="35818-291">In qualità di writer di un gestore di metadati, è possibile avere una grande flessibilità sulla modalità di archiviazione dei dati nel formato dei metadati e sulla modalità di rappresentazione dei dati all'interno di un blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="35818-292">Nella tabella seguente vengono fornite le linee guida che consentono di scegliere il tipo di PROPVARIANT appropriato da utilizzare in situazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="35818-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="35818-293">Il tipo di metadati è...</span><span class="sxs-lookup"><span data-stu-id="35818-293">Metadata type is...</span></span>          | <span data-ttu-id="35818-294">USA tipo PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="35818-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="35818-295">Proprietà PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="35818-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35818-296">Vuoto o inesistente.</span><span class="sxs-lookup"><span data-stu-id="35818-296">Empty or non-existent.</span></span>       | <span data-ttu-id="35818-297">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="35818-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="35818-298">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="35818-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="35818-299">Non definito.</span><span class="sxs-lookup"><span data-stu-id="35818-299">Undefined.</span></span>                   | <span data-ttu-id="35818-300">\_BLOB VT</span><span class="sxs-lookup"><span data-stu-id="35818-300">VT\_BLOB</span></span>                  | <span data-ttu-id="35818-301">Usare la proprietà BLOB per impostare le dimensioni e il puntatore all'oggetto BLOB allocato usando CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="35818-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="35818-302">Un blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-302">A metadata block.</span></span>            | <span data-ttu-id="35818-303">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="35818-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="35818-304">Questo tipo usa la proprietà punkVal.</span><span class="sxs-lookup"><span data-stu-id="35818-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="35818-305">Matrice di tipi.</span><span class="sxs-lookup"><span data-stu-id="35818-305">An array of types.</span></span>           | <span data-ttu-id="35818-306">VT \_ vettore \| VT \_ {Type}</span><span class="sxs-lookup"><span data-stu-id="35818-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="35818-307">Usare la proprietà CA {Type} per impostare il conteggio e il puntatore sulla matrice allocata usando CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="35818-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="35818-308">Matrice di blocchi di metadati.</span><span class="sxs-lookup"><span data-stu-id="35818-308">An array of metadata blocks.</span></span> | <span data-ttu-id="35818-309">\_ \| variante VT vector \_ VT</span><span class="sxs-lookup"><span data-stu-id="35818-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="35818-310">Utilizzare la proprietà capropvar per impostare la matrice di varianti.</span><span class="sxs-lookup"><span data-stu-id="35818-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="35818-311">Valore razionale con segno.</span><span class="sxs-lookup"><span data-stu-id="35818-311">A signed rational value.</span></span>     | <span data-ttu-id="35818-312">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="35818-312">VT\_I8</span></span>                    | <span data-ttu-id="35818-313">Utilizzare la proprietà hVal per impostare il valore.</span><span class="sxs-lookup"><span data-stu-id="35818-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="35818-314">Impostare la parola alta sul denominatore e la parola bassa sul numeratore.</span><span class="sxs-lookup"><span data-stu-id="35818-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="35818-315">Valore razionale.</span><span class="sxs-lookup"><span data-stu-id="35818-315">A rational value.</span></span>            | <span data-ttu-id="35818-316">\_UI8 VT</span><span class="sxs-lookup"><span data-stu-id="35818-316">VT\_UI8</span></span>                   | <span data-ttu-id="35818-317">Utilizzare la proprietà uhVal per impostare il valore.</span><span class="sxs-lookup"><span data-stu-id="35818-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="35818-318">Impostare HighPart sul denominatore e LowPart sul numeratore.</span><span class="sxs-lookup"><span data-stu-id="35818-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="35818-319">Si noti che LowPart è un int senza segno. Il numeratore deve essere convertito da un int senza segno a un int per garantire che il bit di segno venga mantenuto se presente.</span><span class="sxs-lookup"><span data-stu-id="35818-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="35818-320">Per evitare la ridondanza nella rappresentazione di elementi di matrice, non usare matrici sicure; usare solo matrici semplici.</span><span class="sxs-lookup"><span data-stu-id="35818-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="35818-321">In questo modo si riduce il lavoro che un'applicazione deve eseguire quando si interpretano i tipi [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="35818-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="35818-322">Evitare `VT_BYREF` di usare e archiviare i valori in linea laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="35818-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="35818-323">`VT_BYREF` è inefficiente per i tipi piccoli (comuni per gli elementi di metadati) e non fornisce informazioni sulle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="35818-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="35818-324">Prima di usare un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), chiamare sempre **PropVariantInit** per inizializzare il valore.</span><span class="sxs-lookup"><span data-stu-id="35818-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="35818-325">Al termine del PROPVARIANT, chiamare sempre **PropVariantClear** per rilasciare la memoria allocata per la variabile.</span><span class="sxs-lookup"><span data-stu-id="35818-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="35818-326">Gestori 8BIM</span><span class="sxs-lookup"><span data-stu-id="35818-326">8BIM Handlers</span></span>

<span data-ttu-id="35818-327">Quando si scrive un gestore di metadati per un blocco di metadati 8BIM, è necessario usare una firma che incapsula sia la firma 8BIM che l'ID.</span><span class="sxs-lookup"><span data-stu-id="35818-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="35818-328">Il lettore di metadati 8BIMIPTC nativo, ad esempio, fornisce le seguenti informazioni del registro di sistema per l'individuazione dei Reader:</span><span class="sxs-lookup"><span data-stu-id="35818-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="35818-329">Il lettore 8BIMIPTC ha un modello registrato di 0x38, 0x42, 0x49, irreversibile 0x4D, 0x04, 0x04.</span><span class="sxs-lookup"><span data-stu-id="35818-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="35818-330">I primi quattro byte (0x38, 0x42, 0x49, irreversibile 0x4D) sono la firma 8BIM e gli ultimi due byte (0x04, 0x04) sono l'ID del record IPTC.</span><span class="sxs-lookup"><span data-stu-id="35818-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="35818-331">Quindi, per scrivere un lettore di metadati 8BIM per le informazioni di risoluzione, è necessario un modello registrato di 0x38, 0x42, 0x49, irreversibile 0x4D, 0x03, 0xED.</span><span class="sxs-lookup"><span data-stu-id="35818-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="35818-332">Anche in questo caso i primi quattro byte (0x38, 0x42, 0x49, irreversibile 0x4D) sono la firma 8BIM.</span><span class="sxs-lookup"><span data-stu-id="35818-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="35818-333">Gli ultimi due byte (0x03, 0xED), tuttavia, sono l'ID delle informazioni di risoluzione definito dal formato PSD.</span><span class="sxs-lookup"><span data-stu-id="35818-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35818-334">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35818-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="35818-335">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="35818-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35818-336">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="35818-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="35818-337">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="35818-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="35818-338">Cenni preliminari sul linguaggio di query dei metadati</span><span class="sxs-lookup"><span data-stu-id="35818-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="35818-339">Panoramica della lettura e della scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="35818-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="35818-340">Procedura: ricodificare un'immagine JPEG con i metadati</span><span class="sxs-lookup"><span data-stu-id="35818-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="35818-341">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="35818-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="35818-342">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="35818-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
