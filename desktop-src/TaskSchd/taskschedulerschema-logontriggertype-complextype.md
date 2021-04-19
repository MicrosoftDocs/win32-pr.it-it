---
title: Tipo complesso logonTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Utilità di pianificazione di tipo complesso logonTriggerType
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302688"
---
# <a name="logontriggertype-complex-type"></a>Tipo complesso logonTriggerType

Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                                                    | Descrizione                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.<br/>         |
| [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Identificatore dell'utente. L'attività viene avviata quando l'utente accede al computer.<br/> |



## <a name="remarks"></a>Commenti

Oltre agli elementi figlio definiti in questa sezione, l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





