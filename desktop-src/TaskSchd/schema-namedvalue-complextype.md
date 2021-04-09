---
title: Tipo complesso namedValue
description: Definisce un nome associato a un valore in una coppia nome-valore.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- Utilità di pianificazione di tipo complesso namedValue
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964516"
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





