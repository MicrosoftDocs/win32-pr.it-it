---
title: Tipo complesso DataType (registro eventi di Windows)
description: Definisce un elemento di dati.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Log eventi di tipo complesso DataType
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341053"
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
| Nome | stringa | Nome di un elemento di dati definito nel modello (vedere il tipo complesso [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |
| Tipo | QName  | Non usato.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Commenti

L'elemento dati può essere un elemento di dati di primo livello o un elemento dati in una struttura.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





