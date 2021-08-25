---
title: Per enumerare i formati di input
description: Per enumerare i formati di input
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Advanced Systems Format (ASF), enumerazione dei formati di input
- ASF (Advanced Systems Format), enumerazione dei formati di input
- profili,enumerazione dei formati di input
- codec, enumerazione dei formati di input
- Advanced Systems Format (ASF), enumerazioni del formato di input
- ASF (Advanced Systems Format), enumerazioni del formato di input
- profili,enumerazioni del formato di input
- codec, enumerazioni del formato di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09e1583c9331e9cfab26e7ac64064224111ea58858d32b876ece843b83df0d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929251"
---
# <a name="to-enumerate-input-formats"></a>Per enumerare i formati di input

Ognuno dei codec Windows media accetta uno o più tipi di supporti di input per la compressione. L Windows Media Format SDK consente di immettere un'ampia gamma di formati rispetto a quelli supportati dai codec. L'SDK esegue questa operazione eseguendo trasformazioni di pre-elaborazione sugli input quando necessario, ad esempio ridimensionando fotogrammi video o ricampionando l'audio. In ogni caso, è necessario assicurarsi che i formati di input per i file che si scrivono corrispondano ai dati inviati al writer. Ogni codec ha un formato multimediale di input predefinito impostato nel writer quando viene caricato il profilo. È possibile esaminare il formato di input predefinito chiamando [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).

I codec video supportano i formati seguenti: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 e RGB 8. I codec audio supportano l'audio PCM.

Per enumerare i formati di input supportati da un codec, seguire questa procedura:

1.  Creare un oggetto writer e impostare un profilo da usare. Per altre informazioni sull'impostazione dei profili nel writer, vedere [Per usare i profili con writer](to-use-profiles-with-the-writer.md).
2.  Identificare il numero di input per il quale si desidera controllare i formati. Per altre informazioni sull'identificazione dei numeri di input, vedere [Per identificare gli input in base al numero](to-identify-inputs-by-number.md).
3.  Recuperare il numero totale di formati di input supportati dall'input desiderato chiamando [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Scorrere tutti i formati di input supportati, eseguendo i passaggi seguenti per ognuno.
    -   Recuperare [**l'interfaccia IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) per il formato di input chiamando [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Recuperare la [**struttura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il formato di input. Chiamare [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passando **NULL** per il *parametro pType* per ottenere le dimensioni della struttura. Allocare quindi memoria per contenere la struttura e chiamare **di nuovo GetMediaType** per ottenere la struttura. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) eredita da [**IWMMediaProps,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)quindi è possibile effettuare le chiamate a **GetMediaType** dall'istanza di **IWMInputMediaProps** recuperata nel passaggio precedente.
    -   Il formato descritto nella struttura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene tutte le informazioni pertinenti sul formato di input. Il formato di base del supporto è identificato da **WM \_ MEDIA \_ TYPE.subtype**. Per i flussi video, il **membro pbFormat** punta a una struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) allocata dinamicamente che contiene altri dettagli sul flusso, incluse le dimensioni del rettangolo. Non è necessario che le dimensioni dei fotogrammi di input corrispondano esattamente a una dimensione supportata dal codec. Se non corrispondono, i componenti di run-time dell'SDK, in molti casi, ridimensionano automaticamente i fotogrammi video di input in un elemento che il codec può accettare.

Il codice di esempio seguente trova il formato di input del sottotipo passato come parametro. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice](using-the-code-examples.md).


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




