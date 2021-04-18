---
title: Tipo complesso StringTableType
description: Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto. | Tipo complesso StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Log eventi di tipo complesso StringTableType
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321606"
---
# <a name="stringtabletype-complex-type"></a>Tipo complesso StringTableType

Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                              | Tipo | Descrizione                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**string**](eventmanifestschema-string-stringtabletype-element.md) |      | Definisce una stringa localizzata.<br/> |



## <a name="attributes"></a>Attributi



| Nome       | Tipo   | Descrizione                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | string | Identificatore che identifica in modo univoco la stringa nella tabella di stringhe. Ad esempio, "Printer. Connection".<br/> |
| stringType | string | Non usato.<br/>                                                                                                     |
| Valore      | string | Stringa localizzata.<br/>                                                                                         |



## <a name="remarks"></a>Commenti

È possibile fare riferimento alle stringhe da qualsiasi tipo di manifesto che contiene l'attributo del messaggio. Per fare riferimento a una stringa con un stringType di "String" e un ID "Printer. Connection", usare $ (String. Printer. Connection) come valore dell'attributo Message.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





