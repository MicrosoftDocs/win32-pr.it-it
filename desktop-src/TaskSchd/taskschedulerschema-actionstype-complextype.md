---
title: Tipo complesso actionsType
description: Definisce gli elementi figlio e l'attributo per l'elemento Actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- Utilità di pianificazione di tipo complesso actionsType
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400797"
---
# <a name="actionstype-complex-type"></a>Tipo complesso actionsType

Definisce gli elementi figlio e l'attributo per l'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome    | Tipo  | Descrizione                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| Context | IDREF | Identificatore dell'entità utilizzata che rappresenta il contesto di sicurezza per le azioni dell'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





