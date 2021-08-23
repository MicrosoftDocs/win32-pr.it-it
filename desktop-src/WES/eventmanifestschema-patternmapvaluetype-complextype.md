---
title: Tipo complesso PatternMapValueType
description: Non usato. Definisce le espressioni regolari usate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- EventLog di tipo complesso PatternMapValueType
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136164"
---
# <a name="patternmapvaluetype-complex-type"></a>Tipo complesso PatternMapValueType

Non usato. Definisce le espressioni regolari usate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome  | Tipo   | Descrizione                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | string | Espressione regolare utilizzata per trovare una stringa corrispondente nella stringa del messaggio.<br/>                   |
| Valore | string | Espressione regolare utilizzata per modificare la stringa corrispondente trovata nella stringa del messaggio.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





