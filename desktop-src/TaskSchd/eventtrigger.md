---
title: Oggetto EventTrigger (Windows.ui.xaml.h)
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- trigger di evento Utilità di pianificazione , oggetto
- Oggetto EventTrigger Utilità di pianificazione
- Oggetto EventTrigger Utilità di pianificazione , descritto
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
ms.openlocfilehash: a355106ee4fcd6756e7aaf59c19664f91204ffb1caae6ebc2dbe45575a5f2ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060168"
---
# <a name="eventtrigger-object"></a>Oggetto EventTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.

## <a name="members"></a>Membri

**L'oggetto EventTrigger** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto EventTrigger** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](eventtrigger-delay.md)<br/>                      | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.<br/>                                                                                                                                                                                                                                                            |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                                                                                                                                                                                                             |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la quantità massima di tempo per cui è consentita l'esecuzione dell'attività avviata da questo trigger.<br/>                                                                                                                                                                                                                       |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                                                                                                                                                                                                            |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la frequenza di esecuzione dell'attività e la durata della ripetizione del modello di ripetizione dopo l'avvio dell'attività.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                                                                                                                                                                                                           |
| [**Subscription**](eventtrigger-subscription.md)<br/>        | Lettura/Scrittura<br/> | Ottiene o imposta la stringa di query XPath che identifica l'evento che attiva il trigger.<br/>                                                                                                                                                                                                                                                                                         |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene il tipo del trigger.<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | Lettura/Scrittura<br/> | Ottiene o imposta una raccolta di query XPath denominate. Ogni query nella raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella [**proprietà Subscription.**](eventtrigger-subscription.md) Il nome della query può essere usato come variabile nel messaggio di [**un'azione ShowMessageAction.**](showmessageaction.md)<br/> |



 

## <a name="remarks"></a>Commenti

È possibile creare un massimo di 500 attività con sottoscrizioni di eventi. Una sottoscrizione di eventi che esegue query per un'ampia gamma di eventi può essere usata per attivare un'attività che utilizza la stessa azione in risposta agli eventi registrati.

Durante la lettura o la scrittura di codice XML personalizzato per un'attività, viene specificato un trigger di evento usando [**l'elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) dello schema Utilità di pianificazione attività.

## <a name="examples"></a>Esempio

Per altre informazioni e un esempio di codice per questo oggetto di scripting, vedere [Esempio di trigger di evento (scripting).](/previous-versions//aa446887(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Windows.ui.xaml.h</dt> </dl> |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

