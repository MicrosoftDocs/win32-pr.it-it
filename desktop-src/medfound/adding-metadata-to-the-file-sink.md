---
description: Il sink di file ASF è un'implementazione di IMFMediaSink fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai sink di supporto ASF.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Aggiunta di metadati al sink di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049533"
---
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="cca6a-104">Aggiunta di metadati al sink di file</span><span class="sxs-lookup"><span data-stu-id="cca6a-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="cca6a-105">Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file.</span><span class="sxs-lookup"><span data-stu-id="cca6a-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="cca6a-106">Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai [sink di supporto ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="cca6a-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="cca6a-107">Dopo aver [creato il sink di file ASF](creating-the-asf-file-sink.md), è necessario configurarlo con informazioni sui flussi e le informazioni di codifica nel file di output.</span><span class="sxs-lookup"><span data-stu-id="cca6a-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="cca6a-108">Queste procedure sono descritte in [aggiungere informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md) e [impostare le proprietà nel sink di file](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="cca6a-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="cca6a-109">Inoltre, è anche possibile aggiungere informazioni sui metadati, incluse le coppie nome/valore, ad esempio "autore", titolo ".</span><span class="sxs-lookup"><span data-stu-id="cca6a-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="cca6a-110">In questo argomento viene descritto il processo di aggiunta di informazioni sui metadati al sink di file in modo che venga visualizzato nell' [oggetto intestazione ASF](asf-file-structure.md)finale.</span><span class="sxs-lookup"><span data-stu-id="cca6a-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="cca6a-111">È possibile aggiungere informazioni sui metadati al sink di file ASF prima di compilare la topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="cca6a-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="cca6a-112">L'oggetto dell'oggetto ContentInfo ASF per il sink di file tiene traccia delle proprietà dei metadati e viene esposto all'applicazione tramite l'interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="cca6a-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="cca6a-113">Alcune di queste proprietà, ad esempio "IsVBR" che indica se il file contiene flussi di velocità in bit variabili (VBR), vengono impostate automaticamente dal sink di file analizzando le proprietà di codifica del flusso impostate.</span><span class="sxs-lookup"><span data-stu-id="cca6a-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="cca6a-114">Per un elenco completo delle proprietà, vedere l'argomento "elenco attributi" nella documentazione relativa al formato SDK.</span><span class="sxs-lookup"><span data-stu-id="cca6a-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="cca6a-115">Utilizzo dell'interfaccia IMFMetadata nel sink di file ASF</span><span class="sxs-lookup"><span data-stu-id="cca6a-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="cca6a-116">Eseguire una query sull'oggetto sink di file ASF per ottenere un puntatore all'implementazione dell'interfaccia [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="cca6a-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="cca6a-117">Chiamare [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) per ottenere un puntatore [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="cca6a-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="cca6a-118">Il parametro *pPresentationDescriptor* viene ignorato e l'applicazione può passare **null**.</span><span class="sxs-lookup"><span data-stu-id="cca6a-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="cca6a-119">Se l'applicazione passa zero come identificatore del flusso nel parametro *dwStreamIdentifier* , il metodo recupera i metadati che si applicano all'intero file ASF.</span><span class="sxs-lookup"><span data-stu-id="cca6a-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="cca6a-120">In caso contrario, vengono recuperati solo i metadati per il flusso.</span><span class="sxs-lookup"><span data-stu-id="cca6a-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="cca6a-121">Chiamare [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) per recuperare l'elenco delle proprietà di codifica dei file impostate sul contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="cca6a-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="cca6a-122">Chiamare [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) per ottenere i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="cca6a-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="cca6a-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="cca6a-123">Example</span></span>

<span data-ttu-id="cca6a-124">Nell'esempio di codice riportato di seguito viene illustrato come enumerare i nomi e i valori delle proprietà impostati nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="cca6a-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="cca6a-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cca6a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca6a-126">Sink di supporti ASF</span><span class="sxs-lookup"><span data-stu-id="cca6a-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="cca6a-127">Componenti ASF a livello pipeline</span><span class="sxs-lookup"><span data-stu-id="cca6a-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="cca6a-128">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cca6a-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



