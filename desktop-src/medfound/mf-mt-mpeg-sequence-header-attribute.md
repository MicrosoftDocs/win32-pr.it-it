---
description: Contiene l'intestazione di sequenza MPEG-1 o MPEG-2 per un tipo di supporto video.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e988a5b64b7b1c99d3c84de7441f492cebe07f0b473ee3f5256c732fbb7697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035149"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>Attributo \_ MF MT \_ MPEG \_ SEQUENCE \_ HEADER

Contiene l'intestazione di sequenza MPEG-1 o MPEG-2 per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al membro **dwSequenceHeader** della struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) o al membro **bSequenceHeader** della struttura [**MPEG1VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)

Per i video h264 e h265, il BLOB contiene unità [NAL](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenate in formato Allegato B, insieme ai relativi codici di avvio. In particolare, per i video h264 si tratta di unità NAL & PPS. Per h265 sono VPS, SPS & PPS.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
