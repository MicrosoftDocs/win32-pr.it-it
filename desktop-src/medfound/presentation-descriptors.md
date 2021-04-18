---
description: Descrittori di presentazione
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descrittori di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309031"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="6b56a-103">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="6b56a-103">Presentation Descriptors</span></span>

<span data-ttu-id="6b56a-104">Una *presentazione* è un set di flussi multimediali correlati che condividono un tempo di presentazione comune.</span><span class="sxs-lookup"><span data-stu-id="6b56a-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="6b56a-105">Una presentazione, ad esempio, può essere costituita da flussi audio e video di un film.</span><span class="sxs-lookup"><span data-stu-id="6b56a-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="6b56a-106">Un *descrittore di presentazione* è un oggetto che contiene la descrizione di una particolare presentazione.</span><span class="sxs-lookup"><span data-stu-id="6b56a-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="6b56a-107">I descrittori di presentazione vengono usati per configurare origini multimediali e alcuni sink di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="6b56a-108">Ogni descrittore di presentazione contiene un elenco di uno o più descrittori di *flusso*.</span><span class="sxs-lookup"><span data-stu-id="6b56a-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="6b56a-109">Che descrivono i flussi nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="6b56a-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="6b56a-110">I flussi possono essere selezionati o deselezionati.</span><span class="sxs-lookup"><span data-stu-id="6b56a-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="6b56a-111">Solo i flussi selezionati generano dati.</span><span class="sxs-lookup"><span data-stu-id="6b56a-111">Only the selected streams produce data.</span></span> <span data-ttu-id="6b56a-112">I flussi deselezionati non sono attivi e non producono dati.</span><span class="sxs-lookup"><span data-stu-id="6b56a-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="6b56a-113">Ogni descrittore di flusso ha un *gestore di tipo di supporto*, che viene usato per modificare il tipo di supporto del flusso o ottenere il tipo di supporto corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="6b56a-114">Per ulteriori informazioni sui tipi di supporto, vedere [tipi di supporti](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="6b56a-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="6b56a-115">Nella tabella seguente sono illustrate le interfacce primarie esposte da ciascuno di questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="6b56a-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="6b56a-116">Oggetto</span><span class="sxs-lookup"><span data-stu-id="6b56a-116">Object</span></span>                  | <span data-ttu-id="6b56a-117">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="6b56a-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6b56a-118">Descrittore presentazione</span><span class="sxs-lookup"><span data-stu-id="6b56a-118">Presentation descriptor</span></span> | [<span data-ttu-id="6b56a-119">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6b56a-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="6b56a-120">Descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="6b56a-120">Stream descriptor</span></span>       | [<span data-ttu-id="6b56a-121">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6b56a-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="6b56a-122">Gestore del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="6b56a-122">Media type handler</span></span>      | [<span data-ttu-id="6b56a-123">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="6b56a-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="6b56a-124">Presentazioni di origini multimediali</span><span class="sxs-lookup"><span data-stu-id="6b56a-124">Media Source Presentations</span></span>

<span data-ttu-id="6b56a-125">Ogni origine multimediale fornisce un descrittore di presentazione che descrive la configurazione predefinita per l'origine.</span><span class="sxs-lookup"><span data-stu-id="6b56a-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="6b56a-126">Nella configurazione predefinita è selezionato almeno un flusso e ogni flusso selezionato ha un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="6b56a-127">Per ottenere il descrittore della presentazione, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="6b56a-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="6b56a-128">Il metodo restituisce un puntatore [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="6b56a-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="6b56a-129">È possibile modificare il descrittore di presentazione dell'origine per selezionare un set di flussi diverso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="6b56a-130">Non modificare il descrittore della presentazione, a meno che l'origine del supporto non sia stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="6b56a-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="6b56a-131">Le modifiche vengono applicate quando si chiama [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) per avviare l'origine.</span><span class="sxs-lookup"><span data-stu-id="6b56a-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="6b56a-132">Per ottenere il numero di flussi, chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span><span class="sxs-lookup"><span data-stu-id="6b56a-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="6b56a-133">Per ottenere il descrittore del flusso per un flusso, chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passare l'indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="6b56a-134">I flussi sono indicizzati da zero.</span><span class="sxs-lookup"><span data-stu-id="6b56a-134">Streams are indexed from zero.</span></span> <span data-ttu-id="6b56a-135">Il metodo **GetStreamDescriptorByIndex** restituisce un puntatore [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="6b56a-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="6b56a-136">Restituisce anche un flag booleano che indica se il flusso è selezionato.</span><span class="sxs-lookup"><span data-stu-id="6b56a-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="6b56a-137">Se il flusso è selezionato, l'origine multimediale produce dati per quel flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="6b56a-138">In caso contrario, l'origine non produce alcun dato per quel flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="6b56a-139">Per selezionare un flusso, chiamare [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) con l'indice del flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="6b56a-140">Per deselezionare un flusso, chiamare [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="6b56a-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="6b56a-141">Il codice seguente illustra come ottenere il descrittore di presentazione da un'origine multimediale ed enumerare i flussi.</span><span class="sxs-lookup"><span data-stu-id="6b56a-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="6b56a-142">Gestori di tipi multimediali</span><span class="sxs-lookup"><span data-stu-id="6b56a-142">Media Type Handlers</span></span>

<span data-ttu-id="6b56a-143">Per modificare il tipo di supporto del flusso o per ottenere il tipo di supporto corrente del flusso, usare il gestore del tipo di supporto del descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="6b56a-144">Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) per ottenere il gestore del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="6b56a-145">Questo metodo restituisce un puntatore [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="6b56a-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="6b56a-146">Se si vuole semplicemente conoscere il tipo di dati nel flusso, ad esempio audio o video, chiamare [**IMFMediaTypeHandler:: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="6b56a-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="6b56a-147">Questo metodo restituisce il GUID per il tipo di supporto principale.</span><span class="sxs-lookup"><span data-stu-id="6b56a-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="6b56a-148">Ad esempio, un'applicazione di riproduzione connette in genere un flusso audio al renderer audio e un flusso video al renderer video.</span><span class="sxs-lookup"><span data-stu-id="6b56a-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="6b56a-149">Se si usa la sessione multimediale o il caricatore della topologia per compilare una topologia, il GUID di tipo principale potrebbe essere l'unica informazione di formato necessaria.</span><span class="sxs-lookup"><span data-stu-id="6b56a-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="6b56a-150">Se per l'applicazione sono necessarie informazioni più dettagliate sul formato corrente, chiamare [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="6b56a-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="6b56a-151">Questo metodo restituisce un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="6b56a-152">Usare questa interfaccia per ottenere i dettagli del formato.</span><span class="sxs-lookup"><span data-stu-id="6b56a-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="6b56a-153">Il gestore del tipo di supporto contiene anche un elenco dei tipi di supporto supportati per il flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="6b56a-154">Per ottenere le dimensioni dell'elenco, chiamare [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span><span class="sxs-lookup"><span data-stu-id="6b56a-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="6b56a-155">Per ottenere un tipo di supporto dall'elenco, chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) con l'indice del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="6b56a-156">I tipi di supporto vengono restituiti nell'ordine di preferenza approssimativo.</span><span class="sxs-lookup"><span data-stu-id="6b56a-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="6b56a-157">Per i formati audio, ad esempio, sono preferite frequenze di campionamento maggiori rispetto alle frequenze di campionamento inferiori.</span><span class="sxs-lookup"><span data-stu-id="6b56a-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="6b56a-158">Tuttavia, non esiste una regola definitiva che regola l'ordinamento, pertanto è consigliabile gestirla semplicemente come linee guida.</span><span class="sxs-lookup"><span data-stu-id="6b56a-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="6b56a-159">L'elenco dei tipi supportati potrebbe non contenere tutti i possibili tipi di supporto supportati dal flusso.</span><span class="sxs-lookup"><span data-stu-id="6b56a-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="6b56a-160">Per verificare se è supportato un particolare tipo di supporto, chiamare [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span><span class="sxs-lookup"><span data-stu-id="6b56a-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="6b56a-161">Per impostare il tipo di supporto, chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="6b56a-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="6b56a-162">Se il metodo ha esito positivo, il flusso conterrà dati conformi al formato specificato.</span><span class="sxs-lookup"><span data-stu-id="6b56a-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="6b56a-163">Il metodo **SetCurrentMediaType** non modifica l'elenco dei tipi preferiti.</span><span class="sxs-lookup"><span data-stu-id="6b56a-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="6b56a-164">Nel codice seguente viene illustrato come ottenere il gestore del tipo di supporto, enumerare i tipi di supporto preferiti e impostare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="6b56a-165">In questo esempio si presuppone che l'applicazione disponga di un algoritmo, non illustrato di seguito, per la selezione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6b56a-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="6b56a-166">Le specifiche variano in base all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6b56a-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="6b56a-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b56a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b56a-168">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="6b56a-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="6b56a-169">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b56a-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



