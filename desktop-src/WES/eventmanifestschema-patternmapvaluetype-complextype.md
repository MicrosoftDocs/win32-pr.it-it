---
title: Tipo complesso PatternMapValueType
description: Non usato. Definisce le espressioni regolari utilizzate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Log eventi di tipo complesso PatternMapValueType
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739730"
---
# <a name="patternmapvaluetype-complex-type"></a>Tipo complesso PatternMapValueType

Non usato. Definisce le espressioni regolari utilizzate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





