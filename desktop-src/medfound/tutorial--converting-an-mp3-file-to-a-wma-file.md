---
description: Questa esercitazione illustra come usare l'API Transcode per codificare un file Windows Media Audio (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Esercitazione: Codifica di un file WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86301f301bb4f39f6c9258ec3eacfdd1646af8e76791e2df37ae6bf7d8f89880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972790"
---
# <a name="tutorial-encoding-a-wma-file"></a>Esercitazione: Codifica di un file WMA

Questa esercitazione illustra come usare [l'API Transcode](transcode-api.md) per codificare un file Windows Media Audio (WMA).

Questa esercitazione riutilizza la maggior parte del codice dell'esercitazione Codifica di un [file MP4,](tutorial--encoding-an-mp4-file-.md)quindi è consigliabile leggere prima l'esercitazione. L'unico codice diverso è la funzione `CreateTranscodeProfile` , che crea il profilo di transcodifica.

## <a name="create-the-transcode-profile"></a>Creare il profilo transcodifica

Un *profilo transcodifica* descrive i parametri di codifica e il contenitore di file. Per WMA, il contenitore di file è un file ASF (Advanced Streaming Format). Il file ASF contiene un flusso audio, che viene codificato usando Windows [**Media Audio Encoder.**](windowsmediaaudioencoder.md)

Per compilare la topologia di transcodifica, creare il profilo di transcodifica e specificare i parametri per il flusso audio e il contenitore. Creare quindi la topologia specificando l'origine di input, l'URL di output e il profilo di transcodifica.

Per creare il profilo, seguire questa procedura.

1.  Chiamare la [**funzione MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) per creare un profilo transcodifica vuoto.
2.  Chiamare [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) per ottenere un elenco di tipi di file multimediali audio dal codificatore. Questa funzione restituisce un [**puntatore IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) che rappresenta una raccolta di [**puntatori IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
3.  Scegliere il tipo di supporto audio che corrisponde ai requisiti di transcoding e copiare gli attributi in un archivio attributi. Per questa esercitazione viene usato il primo tipo di supporto nell'elenco.
    -   Chiamare [**IMFCollection::GetElement per**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) selezionare un tipo di supporto audio dall'elenco.
    -   Eseguire una query sul tipo di supporto per ottenere un puntatore [**all'interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dell'archivio attributi del tipo di supporto.
    -   Chiamare [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) per ottenere il numero di attributi contenuti nel tipo di supporto.
    -   Chiamare [**MFCreateAttributes per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) creare un nuovo archivio attributi.
    -   Chiamare [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) per copiare gli attributi dal tipo di supporto al nuovo archivio attributi.
4.  Chiamare [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) per impostare gli attributi per il flusso audio.
5.  Chiamare [**MFCreateAttributes per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) creare un archivio attributi per gli attributi a livello di contenitore.
6.  Impostare [l'attributo \_ MF TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md) su **MFTranscodeContainerType \_ ASF,** che specifica un contenitore di file ASF.
7.  Chiamare [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) per impostare gli attributi a livello di contenitore nel profilo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API transcodifica](transcode-api.md)
</dt> </dl>

 

 



