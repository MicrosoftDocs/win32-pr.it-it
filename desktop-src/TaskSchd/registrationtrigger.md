---
title: Oggetto RegistrationTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando l'attività viene registrata o aggiornata.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Utilità di pianificazione trigger di registrazione, oggetto
- Utilità di pianificazione oggetto RegistrationTrigger
- Oggetto RegistrationTrigger Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518081"
---
# <a name="registrationtrigger-object"></a>Oggetto RegistrationTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando l'attività viene registrata o aggiornata.

## <a name="members"></a>Membri

L'oggetto **RegistrationTrigger** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **RegistrationTrigger** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](registrationtrigger-delay.md)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.<br/>                                                                                |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta il periodo di tempo massimo durante il quale è consentita l'esecuzione dell'attività avviata dal trigger.<br/>                           |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta l'identificatore per il trigger.<br/>                                                                               |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato dall'oggetto [**trigger**](trigger.md) . Ottiene il tipo del trigger.<br/>                                                                                              |



 

## <a name="remarks"></a>Commenti

Quando si crea un codice XML personalizzato per un'attività, viene specificato un trigger di registrazione usando l'elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) dello schema utilità di pianificazione.

Se un'attività con un trigger di registrazione ritardata viene registrata e il computer in cui è registrata l'attività viene arrestato o riavviato durante il ritardo, prima dell'esecuzione dell'attività, l'attività non verrà eseguita e il ritardo andrà perso.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e un esempio di codice per questo oggetto di scripting, vedere [esempio di trigger di registrazione (scripting)](registration-trigger-example--scripting-.md).

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
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





