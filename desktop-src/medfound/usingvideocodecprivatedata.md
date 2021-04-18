---
description: Uso di dati privati del codec video
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Uso di dati privati di codec video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310165"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="0a6e0-103">Uso di dati privati di codec video (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="0a6e0-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="0a6e0-104">L'output compresso prodotto dai codec Windows Media Video 9 non può essere decompresso correttamente senza alcuni dati forniti dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="0a6e0-105">Questi dati, detti codec private data, devono essere aggiunti al tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="0a6e0-106">È possibile ottenere i dati privati del codec chiamando i metodi dell'interfaccia [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="0a6e0-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="0a6e0-107">Passare la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) altrimenti completa a [IWMCodecPrivateData:: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span><span class="sxs-lookup"><span data-stu-id="0a6e0-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="0a6e0-108">Chiamare quindi [IWMCodecPrivateData:: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) due volte, una volta per ottenere la dimensione dei dati e quindi di nuovo per copiare i dati in un buffer di tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="0a6e0-109">Creare un nuovo buffer per conservare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con i dati privati accodati e copiare la struttura e i dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="0a6e0-110">Infine, impostare il membro **pbFormat** della struttura **del \_ \_ tipo di supporto DMO** sull'indirizzo del buffer appena creato e impostare il membro **cbFormat** sulle dimensioni combinate, in byte, dei dati **VIDEOINFOHEADER** e privati.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="0a6e0-111">Se si usa MediaFoundation, è possibile costruire una struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) da un'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chiamando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span><span class="sxs-lookup"><span data-stu-id="0a6e0-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="0a6e0-112">È necessario utilizzare i dati privati dei codec ottenuti dopo aver impostato le proprietà nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="0a6e0-113">Se vengono modificate proprietà, è necessario ottenere nuovi dati privati.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="0a6e0-114">Se non si utilizzano i dati privati ottenuti dopo l'impostazione di tutte le proprietà per la sessione di codifica, il decodificatore potrebbe non essere in grado di decomprimere i dati.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="0a6e0-115">Nell'esempio di codice seguente viene illustrato come ottenere i dati privati per un tipo di video:</span><span class="sxs-lookup"><span data-stu-id="0a6e0-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="0a6e0-116">I dati privati del codec forniti da un codificatore video non sono necessariamente uguali ai dati privati forniti da un'implementazione diversa dello stesso codec per la stessa configurazione.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="0a6e0-117">È necessario generare sempre questo valore utilizzando la procedura descritta in questo argomento. non copiare mai i dati privati da un altro file.</span><span class="sxs-lookup"><span data-stu-id="0a6e0-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0a6e0-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a6e0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a6e0-119">Configurazione della codifica video</span><span class="sxs-lookup"><span data-stu-id="0a6e0-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="0a6e0-120">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="0a6e0-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
