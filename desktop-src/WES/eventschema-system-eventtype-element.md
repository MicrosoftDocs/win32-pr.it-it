---
title: System (EventType) (elemento)
description: Contiene informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- Log degli elementi di sistema
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300984"
---
# <a name="system-eventtype-element"></a>System (EventType) (elemento)

Contiene informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

L'elemento **System** è definito dal tipo complesso [**eventType**](eventschema-eventtype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**event**](eventschema-event-element.md)
</dt> </dl>

 

 





