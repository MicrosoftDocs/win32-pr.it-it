---
description: Specifica i tipi di frame di sincronizzazione supportati per un flusso video H.264.
ms.assetid: A2E548F1-A5FA-4110-AD07-46BE9D7DC4A5
title: MF_MT_H264_SUPPORTED_SYNC_FRAME_TYPES attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f6b6d00b3914ebcf55952baf372c139d43a02689605f800628df58b2d71395b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113741"
---
# <a name="mf_mt_h264_supported_sync_frame_types-attribute"></a>Attributo \_ MF MT \_ H264 \_ SUPPORTED SYNC FRAME \_ \_ \_ TYPES

Specifica i tipi di frame di sincronizzazione supportati per un flusso video H.264.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti per i flussi H.264 trasmessi tramite USB. Il valore corrisponde al **campo bmSupportedSyncFrameTypes** nel descrittore del formato video UVC 1.5 H.264.

Questo attributo viene usato anche con codificatori [di fotocamera H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




