---
title: Oggetto EventTrigger (Windows. UI. XAML. h)
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Utilità di pianificazione trigger evento, oggetto
- Utilità di pianificazione oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, descritto
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518604"
---
# <a name="eventtrigger-object"></a>EventTrigger (oggetto)

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.

## <a name="members"></a>Membri

L'oggetto **EventTrigger** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **EventTrigger** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](eventtrigger-delay.md)<br/>                      | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.<br/>                                                                                                                                                                                                                                                            |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                                                                                                                                                                                                             |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo durante il quale l'attività avviata da questo trigger può essere eseguita.<br/>                                                                                                                                                                                                                       |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                                                                                                                                                                                                            |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                                                                                                                                                                                                           |
| [**Abbonamento**](eventtrigger-subscription.md)<br/>        | Lettura/Scrittura<br/> | Ottiene o imposta la stringa di query XPath che identifica l'evento che attiva il trigger.<br/>                                                                                                                                                                                                                                                                                         |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | Lettura/Scrittura<br/> | Ottiene o imposta una raccolta di query XPath denominate. Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà di [**sottoscrizione**](eventtrigger-subscription.md) . Il nome della query può essere utilizzato come variabile nel messaggio di un'azione [**ShowMessageAction**](showmessageaction.md) .<br/> |



 

## <a name="remarks"></a>Commenti

È possibile creare un massimo di 500 attività con sottoscrizioni di eventi. Una sottoscrizione di eventi che esegue query per una varietà di eventi può essere usata per attivare un'attività che usa la stessa azione in risposta agli eventi che vengono registrati.

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificato un trigger di evento usando l'elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere [esempio di trigger di evento (scripting)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Windows. UI. XAML. h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

