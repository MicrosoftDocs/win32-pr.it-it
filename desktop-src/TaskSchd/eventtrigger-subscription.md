---
title: EventTrigger.Subscription - proprietà
description: Per lo scripting, ottiene o imposta una stringa di query che identifica l'evento che attiva il trigger.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Proprietà di sottoscrizione Utilità di pianificazione
- Proprietà Subscription Utilità di pianificazione , oggetto EventTrigger
- EventTrigger object Utilità di pianificazione , Subscription property
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d83225faa022de6e4a0823be3db971c71da503a885a46c1941fc1e5578f711b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100231"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger.Subscription - proprietà

Per lo scripting, ottiene o imposta una stringa di query che identifica l'evento che attiva il trigger.

## <a name="syntax"></a>Sintassi


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valore proprietà

Stringa di query che identifica l'evento che attiva il trigger.

## <a name="remarks"></a>Commenti

Quando si legge o si scrive codice XML personalizzato per un'attività, la sottoscrizione di eventi viene specificata usando l'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) dello schema Utilità di pianificazione dati.

Per altre informazioni sulla scrittura di una stringa di query per determinati eventi, vedere [Selezione](/previous-versions//aa385231(v=vs.85)) e sottoscrizione di eventi [.](../wes/subscribing-to-events.md)

## <a name="examples"></a>Esempio

La stringa di query seguente definisce una sottoscrizione a tutti gli eventi di livello 2 nel canale di sistema:


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

