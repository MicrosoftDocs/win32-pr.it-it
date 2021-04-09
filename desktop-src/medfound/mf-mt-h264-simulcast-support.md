---
description: Specifica il numero di endpoint di streaming e il numero di flussi supportati per un codificatore H. 264 UVC.
ms.assetid: 343EC59E-30E5-4F37-8B05-60EF51717835
title: Attributo MF_MT_H264_SIMULCAST_SUPPORT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879490c6984186cf45971d2b122f0c2217b0f164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879394"
---
# <a name="mf_mt_h264_simulcast_support-attribute"></a>Attributo di supporto di MF \_ mt \_ H264 \_ SIMULCAST \_

Specifica il numero di endpoint di streaming e il numero di flussi supportati per un codificatore H. 264 UVC.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporto per i flussi H. 264 trasmessi tramite USB. Il valore corrisponde al campo **bSimulcastSupport** nel descrittore di formato video UVC 1,5 H. 264.

Questo attributo viene usato anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




