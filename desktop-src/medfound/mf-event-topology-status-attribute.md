---
description: Specifica lo stato di una topologia durante la riproduzione.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: MF_EVENT_TOPOLOGY_STATUS attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fecee6003b0275301a29b32ac34d03db32a22017ab1e828536c0631327f79ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973750"
---
# <a name="mf_event_topology_status-attribute"></a>Attributo MF \_ EVENT \_ TOPOLOGY \_ STATUS

Specifica lo stato di una topologia durante la riproduzione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione \_ TOPOSTATUS di MF.**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus)

Questo attributo viene usato con [l'evento MESessionTopologyStatus.](mesessiontopologystatus.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




