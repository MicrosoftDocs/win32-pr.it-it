---
description: Definisce la sezione del manifesto di strumentazione che identifica il provider e i contatori forniti.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipo complesso counters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14630fa4e0e9461e59d377b4defc3edacee8dca9560d1f7eb42acb317ffd1f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143964"
---
# <a name="counters-complex-type"></a>Tipo complesso counters

Definisce la sezione del manifesto di strumentazione che identifica il provider e i contatori forniti.

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento      | Tipo                                                               | Descrizione                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **Provider** | [**man:provider**](performance-counters-provider-complex-type.md) | Identifica un provider che fornisce contatori.<br/> |



## <a name="attributes"></a>Attributi



| Nome          | Tipo | Descrizione                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Versione dello schema utilizzata per scrivere il manifesto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strumentazione**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

