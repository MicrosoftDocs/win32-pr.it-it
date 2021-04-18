---
description: Specifica il rettangolo di origine per il mixer video del renderer video avanzato (EVR). Il rettangolo di origine è la parte del fotogramma video che il mixer Blits alla superficie di destinazione.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Attributo VIDEO_ZOOM_RECT (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308968"
---
# <a name="video_zoom_rect-attribute"></a>\_ \_ Attributo Rect zoom video

Specifica il rettangolo di origine per il mixer video del [renderer video avanzato](enhanced-video-renderer.md) (EVR). Il rettangolo di origine è la parte del fotogramma video che il mixer Blits alla superficie di destinazione.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una struttura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

Il rettangolo di origine è definito in relazione a un sistema di coordinate normalizzato, in cui l'intero frame video occupa un rettangolo con le coordinate {0, 0, 1, 1}. Il rettangolo di origine deve rientrare nel fotogramma video; le coordinate del rettangolo di origine hanno un intervallo di (0... 1).

Il relatore EVR standard imposta questo attributo sul mixer. Per impostare l'attributo, procedere come segue:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul mixer per ottenere l'archivio di attributi del mixer.
2.  Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) SetAttribute per impostare l'attributo **video \_ Zoom \_ Rect** nel mixer. Il valore è una struttura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

In un EVR Presenter personalizzato è possibile usare questo attributo per implementare il metodo [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) . Per altre informazioni, vedere [rettangoli di origine e di destinazione](how-to-write-an-evr-presenter.md).

La costante GUID per questo attributo viene esportata da strmiids. lib.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>EVR. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi renderer video avanzati](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




