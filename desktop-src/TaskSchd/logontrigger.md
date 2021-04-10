---
title: Oggetto LogonTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando un utente esegue l'accesso.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Utilità di pianificazione trigger LOGON, oggetto
- Utilità di pianificazione oggetto LogonTrigger
- Oggetto LogonTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964518"
---
# <a name="logontrigger-object"></a>Oggetto LogonTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando un utente esegue l'accesso. All'avvio del servizio Utilità di pianificazione, vengono enumerati tutti gli utenti connessi e vengono eseguite tutte le attività registrate con i trigger LOGON corrispondenti all'utente connesso.

## <a name="members"></a>Membri

L'oggetto **LogonTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **LogonTrigger** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](logontrigger-delay.md)<br/>                      | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e il momento in cui il processo viene avviato.<br/>                                                                              |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.<br/>                                         |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore che indica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                                            |
| [**UserId**](logontrigger-userid.md)<br/>                    | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'utente.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Se si desidera che un'attività venga attivata quando un membro di un gruppo accede al computer anziché quando un utente specifico esegue l'accesso, non assegnare un valore alla proprietà [**LogonTrigger. UserID**](logontrigger-userid.md) . In alternativa, creare un trigger LOGON con una proprietà **LogonTrigger. UserID** vuota e assegnare un valore all'entità per l'attività usando la proprietà [**Principal. GroupID**](principal-groupid.md) .

Durante la lettura o la scrittura di codice XML per un'attività, viene specificato un trigger LOGON utilizzando l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger LOGON (scripting)](logon-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





