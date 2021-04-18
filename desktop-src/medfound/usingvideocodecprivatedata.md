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
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Uso di dati privati di codec video (Microsoft Media Foundation)

L'output compresso prodotto dai codec Windows Media Video 9 non può essere decompresso correttamente senza alcuni dati forniti dal codificatore. Questi dati, detti codec private data, devono essere aggiunti al tipo di supporto di output. È possibile ottenere i dati privati del codec chiamando i metodi dell'interfaccia [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) . Passare la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) altrimenti completa a [IWMCodecPrivateData:: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype). Chiamare quindi [IWMCodecPrivateData:: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) due volte, una volta per ottenere la dimensione dei dati e quindi di nuovo per copiare i dati in un buffer di tale dimensione. Creare un nuovo buffer per conservare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con i dati privati accodati e copiare la struttura e i dati nel buffer. Infine, impostare il membro **pbFormat** della struttura **del \_ \_ tipo di supporto DMO** sull'indirizzo del buffer appena creato e impostare il membro **cbFormat** sulle dimensioni combinate, in byte, dei dati **VIDEOINFOHEADER** e privati.

Se si usa MediaFoundation, è possibile costruire una struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) da un'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chiamando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).

È necessario utilizzare i dati privati dei codec ottenuti dopo aver impostato le proprietà nel codificatore. Se vengono modificate proprietà, è necessario ottenere nuovi dati privati. Se non si utilizzano i dati privati ottenuti dopo l'impostazione di tutte le proprietà per la sessione di codifica, il decodificatore potrebbe non essere in grado di decomprimere i dati.

Nell'esempio di codice seguente viene illustrato come ottenere i dati privati per un tipo di video:


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
> I dati privati del codec forniti da un codificatore video non sono necessariamente uguali ai dati privati forniti da un'implementazione diversa dello stesso codec per la stessa configurazione. È necessario generare sempre questo valore utilizzando la procedura descritta in questo argomento. non copiare mai i dati privati da un altro file.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica video](configuringvideoencoding.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
