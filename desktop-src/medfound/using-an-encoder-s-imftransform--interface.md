---
description: Per la conversione di file multimediali in formato ASF, è possibile utilizzare codificatori Windows Media. Per usare questi codificatori, è necessario registrarli nel sistema.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Creazione di un codificatore tramite CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310178"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Creazione di un codificatore tramite CoCreateInstance

Per la conversione di file multimediali in formato ASF, è possibile utilizzare codificatori Windows Media. Per usare questi codificatori, è necessario registrarli nel sistema. I codificatori vengono implementati come [trasformazioni Media Foundation](media-foundation-transforms.md) (MFTS) ed è necessario esporre l'interfaccia IMFTransform. Questo argomento descrive il modo in cui un'applicazione può ottenere un puntatore all'interfaccia IMFTransform del codificatore MFT richiesta e crearne un'istanza per l'uso.

Per informazioni sulla registrazione del codificatore, vedere Creazione di un' [istanza di un codificatore MFT](instantiating-the-encoder-mft.md).

-   [Uso dell'interfaccia IMFTransform di un codificatore](#creating-an-encoder-by-using-cocreateinstance)
    -   [Esempio di creazione del codificatore](#encoder-creation-example)
-   [Argomenti correlati](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Uso dell'interfaccia IMFTransform di un codificatore

Una volta completata la registrazione dei codificatori Windows Media con il sistema, un'applicazione può enumerare i codificatori chiamando [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Per cercare il codificatore corretto, è necessario specificare quanto segue:

-   Il GUID che rappresenta la categoria, ovvero la categoria **MFT \_ \_ audio \_ encoder** o la **\_ categoria MFT \_ video \_ encoder**.

-   Formato da confrontare. Questa impostazione è configurata nella struttura di [**\_ informazioni sul \_ tipo \_ di registro MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che specifica il tipo principale e il sottotipo del tipo di supporto in cui il codificatore genererà gli esempi. Questa struttura viene passata nel parametro *pOutputType* . Per informazioni sui tipi supportati, vedere [GUID di tipo multimediale](media-type-guids.md).

    > [!Note]  
    > Le informazioni sul tipo di input nel parametro *pInputType* non sono necessarie. Questo perché il tipo di input è noto all'applicazione e il codificatore prevede che il flusso di input sia in un formato non compresso.

     

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) restituisce una matrice di puntatori [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) per il codificatore MFTS che corrispondono ai criteri di ricerca. È possibile creare un'istanza di un codificatore chiamando la funzione COM **CoCreateInstance** e passando il CLSID del codificatore che si desidera utilizzare. Questa funzione restituisce un puntatore all'interfaccia **IMFTransform** che rappresenta il codificatore. Per ulteriori informazioni su questa chiamata di funzione, vedere la documentazione di Windows SDK per il Component Object Model (COM).

### <a name="encoder-creation-example"></a>Esempio di creazione del codificatore

Nell'esempio di codice seguente viene illustrato come creare un codificatore audio o video.


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

[Codificatori Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



