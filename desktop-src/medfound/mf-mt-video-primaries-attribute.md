---
description: Specifica i colori primari per un tipo di supporto video.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: MF_MT_VIDEO_PRIMARIES attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b4e1c99dc9a4f288ebab36d413f7eed7c74881e7c10d3c7e9a8a4fe3f0bcf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876711"
---
# <a name="mf_mt_video_primaries-attribute"></a>Attributo \_ MF MT \_ VIDEO \_ PRIMARIES

Specifica i colori primari per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione MFVideoPrimaries.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries)

[**L'enumerazione MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica le primarie dei colori associate a determinati standard video comuni. Se il tipo di supporto usa le primarie di colore non identificate nell'enumerazione **MFVideoPrimaries,** impostare l'attributo [**MF \_ MT CUSTOM \_ VIDEO \_ \_ PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) anziché questo attributo.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Informazioni estese sui colori](extended-color-information.md)
</dt> </dl>

 

 




