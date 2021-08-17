---
title: Elemento string (StringTableType)
description: Definisce una stringa localizzata.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- Elemento string EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136174"
---
# <a name="string-stringtabletype-element"></a>Elemento string (StringTableType)

Definisce una stringa localizzata.

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

**L'elemento** stringa è definito dal [**tipo complesso StringTableType.**](eventmanifestschema-stringtabletype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome       | Tipo   | Descrizione                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Identificatore che identifica in modo univoco la stringa all'interno della tabella di stringhe.<br/> |
| stringType | string | Non usato.<br/>                                                                  |
| Valore      | string | Stringa localizzata.<br/>                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





