---
title: Tipo complesso sessionStateChangeTriggerType
description: Definisce gli elementi utilizzati per creare un trigger di attività per la connessione o la disconnessione della console, la connessione remota o disconnessione o le notifiche di blocco o sblocco della workstation.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Utilità di pianificazione di tipo complesso sessionStateChangeTriggerType
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341302"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Tipo complesso sessionStateChangeTriggerType

Definisce gli elementi utilizzati per creare un trigger di attività per la connessione o la disconnessione della console, la connessione remota o disconnessione o le notifiche di blocco o sblocco della workstation.

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
| [**Ritardo**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Specifica un valore che indica la lunghezza del ritardo prima che un'attività venga avviata quando viene rilevata una modifica dello stato della sessione Terminal Server.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Specifica il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Specifica l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.<br/>              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





