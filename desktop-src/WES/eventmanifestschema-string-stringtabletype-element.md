---
title: Elemento String (StringTableType)
description: Definisce una stringa localizzata.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- EventLog elemento stringa
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964407"
---
# <a name="string-stringtabletype-element"></a>Elemento String (StringTableType)

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

L'elemento **String** è definito dal tipo complesso [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome       | Tipo   | Descrizione                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Identificatore che identifica in modo univoco la stringa nella tabella di stringhe.<br/> |
| stringType | string | Non usato.<br/>                                                                  |
| Valore      | string | Stringa localizzata.<br/>                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Un'StringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





