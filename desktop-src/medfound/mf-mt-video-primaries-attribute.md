---
description: Specifica le primarie colore per un tipo di supporto video.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Attributo MF_MT_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318064"
---
# <a name="mf_mt_video_primaries-attribute"></a>\_ \_ Attributo principali video MF mt \_

Specifica le primarie colore per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .

L'enumerazione [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica le primarie cromatiche associate a determinati standard video comuni. Se il tipo di supporto usa le primarie di colore non identificate nell'enumerazione **MFVideoPrimaries** , impostare l'attributo di [**\_ \_ \_ \_ primari video personalizzati MF mt**](mf-mt-custom-video-primaries-attribute.md) anziché questo attributo.

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

 

 




