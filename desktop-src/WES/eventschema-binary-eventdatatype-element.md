---
title: Binary (EventDataType)-elemento
description: BLOB di dati binari per gli eventi scritti mediante la registrazione degli eventi.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- EventLog elemento binario
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047874"
---
# <a name="binary-eventdatatype-element"></a>Binary (EventDataType)-elemento

BLOB di dati binari per gli eventi scritti mediante la [registrazione degli eventi](/windows/desktop/EventLog/event-logging).

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

L'elemento **binario** è definito dal tipo complesso [**EventDataType**](eventschema-eventdatatype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

