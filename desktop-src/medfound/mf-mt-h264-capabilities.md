---
description: Specifica i flag di funzionalità per un flusso video H.264.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: MF_MT_H264_CAPABILITIES attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138cfa32fc50ebb02ca4d399a178b338e58016c64ae3486d7f7b4a76f3e47afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741803"
---
# <a name="mf_mt_h264_capabilities-attribute"></a>Attributo MF \_ MT \_ H264 \_ CAPABILITIES

Specifica i flag di funzionalità per un flusso video H.264.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti per i flussi H.264 trasmessi tramite USB. Il valore corrisponde al **campo bmCapabilities** nel descrittore del fotogramma video UVC 1.5 H.264.

Questo attributo viene usato anche con codificatori [di fotocamera H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




