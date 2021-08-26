---
title: Tipo complesso namedValue
description: Definisce un nome associato a un valore in una coppia nome-valore.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- Tipo complesso namedValue Utilità di pianificazione
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0f92b89114dfedfbfdbc61d476aff99332191317c1f67b2163eb9416ef3a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080421"
---
# <a name="namedvalue-complex-type"></a>Tipo complesso namedValue

Definisce un nome associato a un valore in una coppia nome-valore.

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome | Tipo                                                                    | Descrizione                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica il nome associato a un valore in una coppia nome-valore. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





