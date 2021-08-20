---
description: Specifica il rettangolo di origine per il mixer video di Enhanced Video Renderer (EVR). Il rettangolo di origine è la parte del fotogramma video che il mixer b blits alla superficie di destinazione.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT attributo (Evr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e6ce19c808545d400f53b9c0091cdbcc20c8efbc13372ae5386e419d244143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737146"
---
# <a name="video_zoom_rect-attribute"></a>Attributo VIDEO \_ ZOOM \_ RECT

Specifica il rettangolo di origine per il mixer video di [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR). Il rettangolo di origine è la parte del fotogramma video che il mixer b blits alla superficie di destinazione.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una [**struttura MFVideoNormalizedRect.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

Il rettangolo di origine è definito in relazione a un sistema di coordinate normalizzato, in cui l'intero fotogramma video occupa un rettangolo con coordinate {0, 0, 1, 1}. Il rettangolo di origine deve rientrare nel fotogramma video. Le coordinate del rettangolo di origine hanno un intervallo di (0...1).

Il presentatore EVR standard imposta questo attributo sul mixer. Per impostare l'attributo, eseguire le operazioni seguenti:

1.  Chiamare [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel mixer per ottenere l'archivio attributi del mixer.
2.  Chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) per impostare l'attributo **VIDEO ZOOM \_ \_ RECT** nel mixer. Il valore è una [**struttura MFVideoNormalizedRect.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

In un presentatore EVR personalizzato è possibile usare questo attributo per implementare il [**metodo IMFVideoDisplayControl::SetVideoPosition.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) Per altre informazioni, vedere [Rettangoli di origine e destinazione](how-to-write-an-evr-presenter.md).

La costante GUID per questo attributo viene esportata da strmiids.lib.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene impostato il rettangolo di origine nel mixer.


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Evr.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del renderer video avanzato](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




