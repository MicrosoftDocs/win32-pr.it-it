---
title: EventTrigger. Subscription (proprietà)
description: Per gli script, ottiene o imposta una stringa di query che identifica l'evento che attiva il trigger.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Utilità di pianificazione proprietà sottoscrizione
- Utilità di pianificazione proprietà di sottoscrizione, oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, Proprietà Subscription
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
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302230"
---
# <a name="eventtriggersubscription-property"></a>EventTrigger. Subscription (proprietà)

Per gli script, ottiene o imposta una stringa di query che identifica l'evento che attiva il trigger.

## <a name="syntax"></a>Sintassi


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valore proprietà

Stringa di query che identifica l'evento che attiva il trigger.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, la sottoscrizione dell'evento viene specificata utilizzando l'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) dello schema utilità di pianificazione.

Per ulteriori informazioni sulla scrittura di una stringa di query per determinati eventi, vedere [selezione](/previous-versions//aa385231(v=vs.85)) di eventi e [sottoscrizione degli eventi](../wes/subscribing-to-events.md).

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

