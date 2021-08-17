---
description: Definisce una struttura che contiene uno o più valori del contatore.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Tipo complesso struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29796a259810cd03739c45338709966bd765f0c1fd9026777f435acb2c5de253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978851"
---
# <a name="struct-complex-type"></a>Tipo complesso struct

Definisce una struttura che contiene uno o più valori del contatore.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome | Tipo                                                                    | Descrizione                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nome della struttura.<br/>                                                                                                            |
| tipo | [**man:CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nome simbolico che identifica la struttura . Lo [strumento CTRPP](ctrpp.md) crea una variabile struct con questo nome che è possibile usare.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




