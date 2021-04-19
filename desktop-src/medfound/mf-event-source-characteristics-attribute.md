---
description: Specifica le caratteristiche correnti dell'origine multimediale.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Attributo MF_EVENT_SOURCE_CHARACTERISTICS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307967"
---
# <a name="mf_event_source_characteristics-attribute"></a>\_ \_ Attributo caratteristiche origine evento MF \_

Specifica le caratteristiche correnti dell'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è **un operatore OR** bit per bit di flag dell'enumerazione delle [**\_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

Questo attributo viene utilizzato con l'evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




