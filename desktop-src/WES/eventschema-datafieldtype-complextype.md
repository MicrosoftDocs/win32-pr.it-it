---
title: Tipo complesso DataType (Windows eventi)
description: Definisce un elemento di dati.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- EventLog di tipo complesso DataType
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fcbf217b16fb675a7a4eca00c8faa201737c07eea35a809f85617e96e9445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620281"
---
# <a name="datatype-complex-type"></a>Tipo complesso DataType

Definisce un elemento di dati.

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome | stringa | Nome di un elemento di dati definito nel modello (vedere il tipo complesso [**TemplateItemType).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |
| Tipo | QName  | Non usato.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Commenti

L'elemento dati può essere un elemento dati di primo livello o un elemento dati in una struttura .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





