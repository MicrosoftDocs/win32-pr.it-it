---
title: Tipo complesso sessionStateChangeTriggerType
description: Definisce gli elementi usati per creare un trigger di attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Tipo complesso sessionStateChangeTriggerType Utilità di pianificazione
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e9779ae2f609f721e4417dc08698e9720bd4cbe03c2b59787edcf862c8d284d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990941"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Tipo complesso sessionStateChangeTriggerType

Definisce gli elementi usati per creare un trigger di attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
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
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                      | Tipo                                                                                    | Descrizione                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Specifica un valore che indica la lunghezza del ritardo prima dell'avvio di un'attività quando viene rilevata una modifica dello stato della sessione di Terminal Server.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Specifica il tipo di modifica della sessione di Terminal Server che attiverebbe l'avvio di un'attività.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Specifica l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.<br/>              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





