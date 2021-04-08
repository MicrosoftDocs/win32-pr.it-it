---
description: Specifica lo stato di un tentativo di risoluzione di una topologia.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Attributo MF_TOPOLOGY_RESOLUTION_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880222"
---
# <a name="mf_topology_resolution_status-attribute"></a>\_Attributo di \_ stato di risoluzione TOPOLOGIa MF \_

Specifica lo stato di un tentativo di risoluzione di una topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il caricatore della topologia o la sessione multimediale potrebbe impostare questo attributo su una topologia. Il valore di questo attributo è un operatore OR bit per bit di **flag dell'enumerazione** di flag di [**stato di \_ risoluzione della topologia \_ \_ \_ MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




