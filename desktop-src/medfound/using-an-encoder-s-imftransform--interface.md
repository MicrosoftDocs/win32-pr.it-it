---
description: Per convertire i file multimediali in formato ASF, è possibile usare Windows codificatori multimediali. Informazioni sulla creazione di un codificatore con CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Creazione di un codificatore tramite CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd48931b7bc8e0b449ee8ffaa0141a6413f2699ebaae6e1ba01fdd1f4b38a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092321"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Creazione di un codificatore tramite CoCreateInstance

Per convertire i file multimediali in formato ASF, è possibile usare Windows codificatori multimediali. Per usare questi codificatori, è necessario registrarli con il sistema. I codificatori vengono implementati [Media Foundation e](media-foundation-transforms.md) devono esporre l'interfaccia IMFTransform. Questo argomento descrive come un'applicazione può ottenere un puntatore all'interfaccia IMFTransform del codificatore MFT richiesto e crearne un'istanza per l'uso.

Per informazioni sulla registrazione del codificatore, vedere [Creazione di un'istanza di un codificatore MFT.](instantiating-the-encoder-mft.md)

-   [Uso dell'interfaccia IMFTransform di un codificatore](#creating-an-encoder-by-using-cocreateinstance)
    -   [Esempio di creazione del codificatore](#encoder-creation-example)
-   [Argomenti correlati](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Uso dell'interfaccia IMFTransform di un codificatore

Al completamento della registrazione Windows codificatori multimediali con il sistema, un'applicazione può enumerare i codificatori chiamando [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Per cercare il codificatore giusto, è necessario specificare quanto segue:

-   GUID che rappresenta la categoria, ovvero **MFT \_ CATEGORY AUDIO \_ \_ ENCODER** o **MFT CATEGORY VIDEO \_ \_ \_ ENCODER.**

-   Formato di cui trovare la corrispondenza. Questa proprietà viene impostata nella [**struttura MFT \_ REGISTER TYPE \_ \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che specifica il tipo principale e il sottotipo del tipo di supporto in cui il codificatore genererà campioni. Questa struttura viene passata nel *parametro pOutputType.* Per informazioni sui tipi supportati, vedere [GUID dei tipi di supporti.](media-type-guids.md)

    > [!Note]  
    > Le informazioni sul tipo di input *nel parametro pInputType* non sono necessarie. Questo perché il tipo di input è noto all'applicazione e il codificatore prevede che il flusso di input sia in un formato non compresso.

     

[**MFTEnum restituisce**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) una matrice di puntatori [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) per i MFT del codificatore che corrispondono ai criteri di ricerca. È possibile creare un'istanza di un codificatore chiamando la funzione COM **CoCreateInstance** e passando il CLSID del codificatore che si vuole usare. Questa funzione restituisce un puntatore **all'interfaccia IMFTransform** che rappresenta il codificatore. Per altre informazioni su questa chiamata di funzione, vedere la documentazione Windows SDK per Component Object Model (COM).

### <a name="encoder-creation-example"></a>Esempio di creazione del codificatore

L'esempio di codice seguente illustra come creare un codificatore audio o video.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 



