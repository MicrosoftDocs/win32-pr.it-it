---
description: Le informazioni di intestazione ASF vengono archiviate negli oggetti intestazione ASF di un file multimediale.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Recupero di informazioni da oggetti Header ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305372"
---
# <a name="getting-information-from-asf-header-objects"></a><span data-ttu-id="7f91e-103">Recupero di informazioni da oggetti Header ASF</span><span class="sxs-lookup"><span data-stu-id="7f91e-103">Getting Information from ASF Header Objects</span></span>

<span data-ttu-id="7f91e-104">Le informazioni di intestazione ASF vengono archiviate negli oggetti intestazione ASF di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="7f91e-104">ASF header information is stored in the ASF Header Objects of a media file.</span></span> <span data-ttu-id="7f91e-105">Media Foundation fornisce l' [oggetto ContentInfo ASF](asf-contentinfo-object.md) da usare con l'oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-105">Media Foundation provides the [ASF ContentInfo Object](asf-contentinfo-object.md) to work with the Header Object.</span></span> <span data-ttu-id="7f91e-106">Un oggetto ContentInfo popolato è necessario affinché l'applicazione legga le informazioni di intestazione di un file esistente.</span><span class="sxs-lookup"><span data-stu-id="7f91e-106">A populated ContentInfo object is required in order for the application to read header information of an existing file.</span></span> <span data-ttu-id="7f91e-107">Questa operazione viene eseguita chiamando [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="7f91e-107">This is achieved by calling [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span> <span data-ttu-id="7f91e-108">Se l'analisi viene completata correttamente, la libreria ASF per il file, gestita internamente da Media Foundation, viene popolata con le informazioni di intestazione di diversi oggetti intestazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-108">If parsing completes successfully, the ASF library for the file, which is maintained internally by Media Foundation, is populated with header information from various Header Objects.</span></span> <span data-ttu-id="7f91e-109">Alcune di queste proprietà sono esposte all'applicazione, che è possibile recuperare tramite gli attributi sul descrittore della presentazione, il descrittore del flusso, il profilo e le proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="7f91e-109">Some of these properties are exposed to the application, which it can retrieve through attributes on the presentation descriptor, stream descriptor, the profile, and metadata properties.</span></span>

<span data-ttu-id="7f91e-110">Per l'elenco completo degli attributi, vedere [Media Foundation attributi per gli oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7f91e-110">For the complete list of attributes, see [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a><span data-ttu-id="7f91e-111">Recupero delle informazioni di intestazione da un descrittore di presentazione</span><span class="sxs-lookup"><span data-stu-id="7f91e-111">Retrieving Header Information from a Presentation Descriptor</span></span>

<span data-ttu-id="7f91e-112">Un oggetto descrittore di presentazione contiene la descrizione di una particolare origine multimediale, in questo caso l'origine del supporto ASF.</span><span class="sxs-lookup"><span data-stu-id="7f91e-112">A presentation descriptor object contains the description of a particular media source, in this case the ASF media source.</span></span> <span data-ttu-id="7f91e-113">Se la chiamata **ParseHeader** viene completata correttamente, le informazioni a livello di file dell'oggetto Header vengono archiviate come attributi nel descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-113">If the **ParseHeader** call completes successfully, file-level information from the Header Object is stored as attributes on the presentation descriptor.</span></span> <span data-ttu-id="7f91e-114">Per creare il descrittore della presentazione, chiamare [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="7f91e-114">To create the presentation descriptor, call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="7f91e-115">Questo metodo restituisce un puntatore a un oggetto descrittore di presentazione popolato contenente questi attributi per il file ASF associato all'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="7f91e-115">This method returns a pointer to a populated presentation descriptor object that contains these attributes for the ASF file associated with the ContentInfo object.</span></span> <span data-ttu-id="7f91e-116">Per ottenere i valori per attributi specifici, chiamare i metodi **IMFAttributes:: GetXXX** sul descrittore della presentazione e specificare l'attributo **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="7f91e-116">To get values for specific attributes, call **IMFAttributes::Getxxx** methods on the presentation descriptor and specify the **MF\_PD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="7f91e-117">Il codice di esempio seguente recupera la durata di riproduzione di un file ASF, specificato da un oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="7f91e-117">The following example code retrieves the play duration of an ASF file, specified by a ContentInfo object.</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



<span data-ttu-id="7f91e-118">Per ulteriori informazioni sui descrittori di presentazione in generale, vedere [descrittori di presentazione](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7f91e-118">For more information about presentation descriptors in general, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="7f91e-119">Per il set completo di attributi del descrittore di presentazione, vedere [attributi](presentation-descriptor-attributes.md)del descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-119">For the complete set of presentation descriptor attributes, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-a-stream-descriptor"></a><span data-ttu-id="7f91e-120">Recupero delle informazioni di intestazione da un descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="7f91e-120">Retrieving Header Information from a Stream Descriptor</span></span>

<span data-ttu-id="7f91e-121">Un oggetto descrittore di flusso espone l'interfaccia [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) e descrive le caratteristiche dei flussi nel file.</span><span class="sxs-lookup"><span data-stu-id="7f91e-121">A stream descriptor object exposes the [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface and describes the characteristics of the streams in the file.</span></span> <span data-ttu-id="7f91e-122">Il descrittore di presentazione per il contenuto ASF contiene uno o più descrittori di flusso che rappresentano i flussi elencati nell'oggetto intestazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-122">The presentation descriptor for the ASF content contains one or more stream descriptors that represent the streams listed in the Header Object.</span></span> <span data-ttu-id="7f91e-123">Dopo che la chiamata a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) è stata completata correttamente, i descrittori di flusso sottostanti vengono popolati con informazioni a livello di flusso dai vari oggetti intestazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-123">After the call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) completes successfully, the underlying stream descriptors are populated with stream-level information from the various Header Objects.</span></span> <span data-ttu-id="7f91e-124">Per ottenere un descrittore di flusso per un flusso ASF, chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) sul descrittore della presentazione generato dall'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="7f91e-124">To get a stream descriptor for an ASF stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) on the presentation descriptor that is generated from the ContentInfo object.</span></span>

<span data-ttu-id="7f91e-125">Alcune delle proprietà del flusso sono impostate come attributi nei descrittori di flusso.</span><span class="sxs-lookup"><span data-stu-id="7f91e-125">Some of the stream properties are set as attributes on stream descriptors.</span></span> <span data-ttu-id="7f91e-126">Chiamare i metodi **IMFAttributes:: GetXXX** in un descrittore di flusso e specificare l'attributo **MF \_ SD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="7f91e-126">Call **IMFAttributes::Getxxx** methods on a stream descriptor and specify the **MF\_SD\_ASF\_xxx** attribute.</span></span>

<span data-ttu-id="7f91e-127">Per il set completo di attributi del descrittore di flusso, vedere gli attributi "descrittore di flusso specifico di ASF" elencati negli [attributi del descrittore di flusso](stream-descriptor-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="7f91e-127">For the complete set of stream descriptor attributes, see "ASF-Specific Stream Descriptor" attributes listed in [Stream Descriptor Attributes](stream-descriptor-attributes.md).</span></span>

## <a name="retrieving-header-information-from-the-profile-object"></a><span data-ttu-id="7f91e-128">Recupero delle informazioni di intestazione dall'oggetto profilo</span><span class="sxs-lookup"><span data-stu-id="7f91e-128">Retrieving Header Information from the Profile Object</span></span>

<span data-ttu-id="7f91e-129">Oltre ai descrittori di flusso, l'oggetto profilo ASF descrive anche le proprietà del flusso.</span><span class="sxs-lookup"><span data-stu-id="7f91e-129">In addition to stream descriptors, the ASF profile object also describes the stream properties.</span></span> <span data-ttu-id="7f91e-130">Per ottenere il profilo di un file ASF esistente, chiamare [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="7f91e-130">To get the profile of an existing ASF file, call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="7f91e-131">L'oggetto profilo ASF restituito da questo metodo non include gli attributi **MF \_ PD \_ ASF \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="7f91e-131">The ASF profile object returned by this method does not include any of the **MF\_PD\_ASF\_xxx** attributes.</span></span> <span data-ttu-id="7f91e-132">Questi attributi sono disponibili per l'applicazione solo dopo la chiamata a [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) per generare l'oggetto profilo da un descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="7f91e-132">These attributes are available to the application only after it calls [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) to generate the profile object from a presentation descriptor.</span></span> <span data-ttu-id="7f91e-133">È possibile usare il profilo per ottenere i puntatori agli oggetti di esclusione reciproca e di assegnazione delle priorità dei flussi.</span><span class="sxs-lookup"><span data-stu-id="7f91e-133">You can use the profile to get pointers to the mutual exclusion and stream prioritization objects.</span></span>

<span data-ttu-id="7f91e-134">Per informazioni sull'oggetto profilo, vedere [profilo ASF](asf-profile.md) .</span><span class="sxs-lookup"><span data-stu-id="7f91e-134">For information about the profile object, see [ASF Profile](asf-profile.md) .</span></span>

## <a name="retrieving-metadata-from-header-objects"></a><span data-ttu-id="7f91e-135">Recupero di metadati da oggetti Header</span><span class="sxs-lookup"><span data-stu-id="7f91e-135">Retrieving Metadata from Header Objects</span></span>

<span data-ttu-id="7f91e-136">Un file ASF può contenere diverse proprietà dei metadati impostate durante la codifica dei file.</span><span class="sxs-lookup"><span data-stu-id="7f91e-136">An ASF file can contain several metadata properties that are set during file encoding.</span></span> <span data-ttu-id="7f91e-137">Un'applicazione può enumerare queste proprietà con l'oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="7f91e-137">An application can enumerate these properties with the ContentInfo object.</span></span> <span data-ttu-id="7f91e-138">Alcune di queste proprietà, ad esempio le informazioni sulla velocità in bit variabile (VBR), sono disponibili per l'applicazione tramite attributi per il descrittore di presentazione, i descrittori di flusso e i tipi di supporto per il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="7f91e-138">Some of these properties, such as variable bit rate (VBR) information, are available to the application through attributes on presentation descriptor, stream descriptors, and media types for the media file.</span></span> <span data-ttu-id="7f91e-139">Questi attributi vengono impostati nell'oggetto ContentInfo durante l'inizializzazione tramite la chiamata [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="7f91e-139">These attributes are set on the ContentInfo object during initialization through the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f91e-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f91e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f91e-141">Oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="7f91e-141">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> </dl>

 

 



