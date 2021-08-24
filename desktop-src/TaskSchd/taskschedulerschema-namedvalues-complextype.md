---
title: Tipo complesso namedValues
description: Definisce una coppia nome-valore in cui il nome è associato al valore.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- Tipi complessi namedValues Utilità di pianificazione
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d54e7c33d0b7ab2e5be3c4de6f3f648398a7e65670c0379f5621ae9e8a8bd46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513937"
---
# <a name="namedvalues-complex-type"></a>Tipo complesso namedValues

Definisce una coppia nome-valore in cui il nome è associato al valore.

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                        | Tipo                                                | Descrizione                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Valore**](taskschedulerschema-value-namedvalues-element.md) | [**namedValue**](schema-namedvalue-complextype.md) | Specifica il valore associato a un nome in una coppia nome-valore.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





