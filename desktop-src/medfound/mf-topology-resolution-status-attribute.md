---
description: Specifica lo stato di un tentativo di risolvere una topologia.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: MF_TOPOLOGY_RESOLUTION_STATUS attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a62645b17efadb8216ba078b966bc2f7f47debae60103fa6665daaeaebc13306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691233"
---
# <a name="mf_topology_resolution_status-attribute"></a>Attributo MF \_ TOPOLOGY \_ RESOLUTION \_ STATUS

Specifica lo stato di un tentativo di risolvere una topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il caricatore della topologia o la sessione multimediale potrebbe impostare questo attributo in una topologia. Il valore di questo attributo è un **OR** bit per bit di flag dell'enumerazione [**MF \_ TOPOLOGY \_ RESOLUTION STATUS \_ \_ FLAGS.**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags)

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




