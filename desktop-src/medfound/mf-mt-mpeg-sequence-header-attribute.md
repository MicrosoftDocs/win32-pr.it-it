---
description: Contiene l'intestazione della sequenza MPEG-1 o MPEG-2 per un tipo di supporto video.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Attributo MF_MT_MPEG_SEQUENCE_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315032"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>\_ \_ \_ Attributo header della sequenza MF mt MPEG \_

Contiene l'intestazione della sequenza MPEG-1 o MPEG-2 per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al membro **dwSequenceHeader** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) o al membro **bSequenceHeader** della struttura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .

Per i video H264 e H265, il BLOB contiene [unità NAL](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenate nel formato allegato B, insieme ai relativi codici iniziali. In particolare, per i video H264 si tratta di SPS & unità NAL di PPS. Per H265 sono VPS, SPS & PPS.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

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

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
