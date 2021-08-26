---
description: Uso dei dati privati del codec video
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Uso dei dati privati del codec video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e417d4d83cc3ae3174e1bbf3310a6abb2900e2c5f3323192a8d17643e4066f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887091"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Uso dei dati privati del codec video (Microsoft Media Foundation)

L'output compresso prodotto dai codec Windows Media Video 9 non può essere decompresso correttamente senza alcuni dati forniti dal codificatore. Questi dati, denominati dati privati del codec, devono essere aggiunti al tipo di supporto di output. È possibile ottenere i dati privati del codec chiamando i metodi [dell'interfaccia IWMCodecPrivateData.](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) Passare la struttura MEDIA [**\_ \_ TYPE DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) altrimenti completa a [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype). Chiamare quindi [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) due volte, una volta per ottenere le dimensioni dei dati e quindi di nuovo per copiare i dati in un buffer di tale dimensione. Creare un nuovo buffer per contenere la [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con i dati privati aggiunti e copiare la struttura e i dati in tale buffer. Infine, impostare il membro **pbFormat** della struttura **DMO MEDIA \_ \_ TYPE** sull'indirizzo del buffer appena creato e impostare il membro **cbFormat** sulla dimensione combinata, in byte, di **VIDEOINFOHEADER** e dei dati privati.

Se si usa MediaFoundation, è possibile costruire una [**struttura DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) da un'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chiamando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).

È necessario usare i dati privati del codec ottenuti dopo aver prima impostato le proprietà sul codificatore. Se vengono modificate proprietà, è necessario ottenere nuovi dati privati. Se non si usano i dati privati ottenuti dopo che tutte le proprietà sono state impostate per la sessione di codifica, il decodificatore potrebbe non essere in grado di decomprimere i dati.

L'esempio di codice seguente illustra come ottenere i dati privati per un tipo di video:


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
> Non è garantito che i dati privati del codec recapitati da un codificatore video siano gli stessi dei dati privati recapitati da un'implementazione diversa dello stesso codec per la stessa configurazione. È sempre necessario generare questo valore usando la procedura descritta in questo argomento. non copiare mai i dati privati da un altro file.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica video](configuringvideoencoding.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
