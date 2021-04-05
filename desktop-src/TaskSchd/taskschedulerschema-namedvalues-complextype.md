---
title: Tipo complesso namedValues
description: Definisce una coppia nome-valore in cui il nome è associato al valore.
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- Utilità di pianificazione di tipo complesso namedValues
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742162"
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





