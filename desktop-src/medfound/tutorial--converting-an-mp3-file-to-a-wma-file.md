---
description: Questa esercitazione illustra come usare l'API transcode per codificare un file di Windows Media Audio (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Esercitazione: codifica di un file WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310192"
---
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="3a131-103">Esercitazione: codifica di un file WMA</span><span class="sxs-lookup"><span data-stu-id="3a131-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="3a131-104">Questa esercitazione illustra come usare l' [API transcode](transcode-api.md) per codificare un file di Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="3a131-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="3a131-105">Questa esercitazione riutilizza la maggior parte del codice dall'esercitazione [codifica di un file MP4](tutorial--encoding-an-mp4-file-.md), quindi è consigliabile leggere prima di tutto l'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="3a131-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="3a131-106">L'unico codice che differisce è la funzione `CreateTranscodeProfile` , che consente di creare il profilo transcodifica.</span><span class="sxs-lookup"><span data-stu-id="3a131-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="3a131-107">Creare il profilo di transcodifica</span><span class="sxs-lookup"><span data-stu-id="3a131-107">Create the Transcode Profile</span></span>

<span data-ttu-id="3a131-108">Un *profilo di transcodifica* descrive i parametri di codifica e il contenitore di file.</span><span class="sxs-lookup"><span data-stu-id="3a131-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="3a131-109">Per WMA, il contenitore di file è un file di formato di streaming avanzato (ASF).</span><span class="sxs-lookup"><span data-stu-id="3a131-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="3a131-110">Il file ASF contiene un flusso audio, codificato tramite il [**codificatore Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="3a131-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="3a131-111">Per compilare la topologia transcode, creare il profilo transcode e specificare i parametri per il flusso audio e il contenitore.</span><span class="sxs-lookup"><span data-stu-id="3a131-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="3a131-112">Quindi creare la topologia specificando l'origine di input, l'URL di output e il profilo di transcodifica.</span><span class="sxs-lookup"><span data-stu-id="3a131-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="3a131-113">Per creare il profilo, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="3a131-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="3a131-114">Chiamare la funzione [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) per creare un profilo transcodifica vuoto.</span><span class="sxs-lookup"><span data-stu-id="3a131-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="3a131-115">Chiamare [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) per ottenere un elenco di tipi di supporti audio dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="3a131-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="3a131-116">Questa funzione restituisce un puntatore [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) che rappresenta una raccolta di puntatori [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3a131-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="3a131-117">Scegliere il tipo di supporto audio che corrisponde ai requisiti di transcodifica e copiare gli attributi in un archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="3a131-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="3a131-118">Per questa esercitazione viene usato il primo tipo di supporto nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3a131-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="3a131-119">Chiamare [**IMFCollection:: GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) per selezionare un tipo di supporto audio dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="3a131-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="3a131-120">Eseguire una query sul tipo di supporto per ottenere un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dell'archivio di attributi del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3a131-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="3a131-121">Chiamare [**IMFAttributes:: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) per ottenere il numero di attributi contenuti nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3a131-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="3a131-122">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="3a131-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="3a131-123">Chiamare [**IMFAttributes:: CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) per copiare gli attributi dal tipo di supporto al nuovo archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="3a131-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="3a131-124">Chiamare [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) per impostare gli attributi per il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="3a131-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="3a131-125">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi per gli attributi a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="3a131-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="3a131-126">Impostare l'attributo [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) su **MFTranscodeContainerType \_ ASF**, che specifica un contenitore di file ASF.</span><span class="sxs-lookup"><span data-stu-id="3a131-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="3a131-127">Chiamare [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) per impostare gli attributi a livello di contenitore sul profilo.</span><span class="sxs-lookup"><span data-stu-id="3a131-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3a131-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a131-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a131-129">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="3a131-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 



