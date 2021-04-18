---
description: Viene descritto come Chroma è stato campionato per un tipo di supporto video YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Attributo MF_MT_VIDEO_CHROMA_SITING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314030"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a>\_Attributo di \_ localizzazione del video MF mt \_ \_

Descrive il modo in cui Chroma è stato campionato per un tipo di supporto video Cb'Cr.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è **un operatore OR** bit per bit di flag dell'enumerazione [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Informazioni sui colori estesi](extended-color-information.md)
</dt> </dl>

 

 




