---
description: Definisce un elenco di strutture che contengono valori del contatore.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Tipo complesso structs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314421"
---
# <a name="structs-complex-type"></a>Tipo complesso structs

Definisce un elenco di strutture che contengono valori del contatore.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento    | Tipo                                                           | Descrizione                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **Struct** | [**man:struct**](performance-counters-struct-complex-type.md) | Nome di una struttura che contiene i valori del contatore.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




