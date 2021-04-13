---
description: Frequenza dei fotogrammi di un tipo di supporto video, in frame al secondo.
ms.assetid: 8336559c-06f1-478e-b921-e9eae7425230
title: Attributo MF_MT_FRAME_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8df2ef4268bd643d9f65eb16c3f7257bcaceb1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401760"
---
# <a name="mf_mt_frame_rate-attribute"></a>\_ \_ Attributo frequenza di fotogrammi MF mt \_

Frequenza dei fotogrammi di un tipo di supporto video, in frame al secondo.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

La frequenza dei fotogrammi è espressa come rapporto. I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore. Se, ad esempio, la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1. Se la frequenza dei fotogrammi è 29,97 fps, il rapporto è 30000/1001.

Per impostare il valore, utilizzare la funzione [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Per ottenere il valore, usare la funzione [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene impostata la frequenza dei fotogrammi su un tipo di supporto video.


```
// Helper function to set the frame rate on a video media type.
inline HRESULT SetFrameRate(
    IMFMediaType *pType, 
    UINT32 numerator, 
    UINT32 denominator
    )
{
    return MFSetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        numerator, 
        denominator
        );
}
```



Nell'esempio seguente viene ottenuta la frequenza dei fotogrammi da un tipo di supporto video.


```
// Helper function to get the frame rate from a video media type.
inline HRESULT GetFrameRate(
    IMFMediaType *pType, 
    UINT32 *pNumerator, 
    UINT32 *pDenominator
    )
{
    return MFGetAttributeRatio(
        pType, 
        MF_MT_FRAME_RATE, 
        pNumerator, 
        pDenominator
        );
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate)
</dt> <dt>

[**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe)
</dt> </dl>

 

 




