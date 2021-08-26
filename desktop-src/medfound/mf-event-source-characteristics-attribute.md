---
description: Specifica le caratteristiche correnti dell'origine multimediale.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: MF_EVENT_SOURCE_CHARACTERISTICS attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a9b72adaa5869d806ab0a3c8afcddff7892f93872e86aa6dfe96bde1b8348b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956591"
---
# <a name="mf_event_source_characteristics-attribute"></a>Attributo MF \_ EVENT \_ SOURCE \_ CHARACTERISTICS

Specifica le caratteristiche correnti dell'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è **un'operazione OR** bit per bit di flag dell'enumerazione [**MFMEDIASOURCE \_ CHARACTERISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)

Questo attributo viene usato con [l'evento MESourceCharacteristicsChanged.](mesourcecharacteristicschanged.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




