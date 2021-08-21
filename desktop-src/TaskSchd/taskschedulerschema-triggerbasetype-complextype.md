---
title: Tipo complesso triggerBaseType
description: Definisce l'attributo, gli elementi figlio di base e le informazioni di sequenziazione per tutti i tipi complessi di trigger.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- Tipo complesso triggerBaseType Utilità di pianificazione
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21eed68ff260d199a46adabc0e560533658c6cc1398d00f9507b80b40fb69955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611012"
---
# <a name="triggerbasetype-complex-type"></a>Tipo complesso triggerBaseType

Definisce l'attributo, gli elementi figlio di base e le informazioni di sequenziazione per tutti i tipi complessi di trigger.

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                      | Tipo                                                                     | Descrizione                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Attivato**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Specifica che il trigger è abilitato.<br/>                                                                      |
| [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Data e ora di disattivazione del trigger.<br/>                                                          |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Specifica l'intervallo in cui il trigger può avviare l'attività.<br/>                                                 |
| [**Ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Specifica la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'attivazione del trigger.<br/> |
| [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Data e ora di attivazione del trigger.<br/>                                                            |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                           |
|------|------|---------------------------------------|
| id   | ID   | Identificatore del trigger.<br/> |



## <a name="remarks"></a>Commenti

I tipi complessi trigger includono i seguenti.

-   [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)
-   [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)
-   [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)
-   [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)
-   [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)
-   [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)
-   [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





