---
description: Specifica le modalità di controllo della frequenza supportate per un flusso video H.264.
ms.assetid: DAA62ECD-AFA2-40C2-9B52-F2D581F4D894
title: MF_MT_H264_SUPPORTED_RATE_CONTROL_MODES attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9665fd99635749e2400437e77cb89e74d2cb8675689f6f4b867a20ac82fadaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692283"
---
# <a name="mf_mt_h264_supported_rate_control_modes-attribute"></a>Attributo \_ MF MT \_ H264 \_ SUPPORTED RATE CONTROL \_ \_ \_ MODES

Specifica le modalità di controllo della frequenza supportate per un flusso video H.264.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti per i flussi H.264 trasmessi tramite USB. Il valore corrisponde al **campo bmSupportedRateControlModes** nel descrittore del formato video UVC 1.5 H.264.

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

 

 




