---
description: Definisce la sezione del manifesto di strumentazione che identifica il provider e i contatori che forniscono.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipi complessi di contatori
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967507"
---
# <a name="counters-complex-type"></a>Tipi complessi di contatori

Definisce la sezione del manifesto di strumentazione che identifica il provider e i contatori che forniscono.

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
| **provider** | [**uomo: provider**](performance-counters-provider-complex-type.md) | Identifica un provider che fornisce contatori.<br/> |



## <a name="attributes"></a>Attributi



| Nome          | Tipo | Descrizione                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | Versione dello schema utilizzata per scrivere il manifesto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strumentazione**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

