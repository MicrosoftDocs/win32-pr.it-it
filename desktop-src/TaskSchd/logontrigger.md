---
title: Oggetto LogonTrigger
description: Oggetto di scripting che rappresenta un trigger che avvia un'attività quando un utente accede.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- trigger di accesso Utilità di pianificazione , oggetto
- Oggetto LogonTrigger Utilità di pianificazione
- Oggetto LogonTrigger Utilità di pianificazione , descritto
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
ms.openlocfilehash: 1aed10ba9c0c792a5e4f882988ca07770c4ac568cb893b8ffac16a3a24efd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760098"
---
# <a name="logontrigger-object"></a>Oggetto LogonTrigger

Oggetto di scripting che rappresenta un trigger che avvia un'attività quando un utente accede. All'avvio del Utilità di pianificazione, vengono enumerati tutti gli utenti connessi e vengono eseguite tutte le attività registrate con i trigger di accesso che corrispondono all'utente connesso.

## <a name="members"></a>Membri

**L'oggetto LogonTrigger** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto LogonTrigger** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ritardo**](logontrigger-delay.md)<br/>                      | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica la quantità di tempo tra l'accesso dell'utente e l'avvio del processo.<br/>                                                                              |
| [**Abilitato**](trigger-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta un valore booleano che indica se il trigger è abilitato.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo la disattivazione.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la quantità massima di tempo consentita per l'esecuzione dell'attività avviata dal trigger.<br/>                                         |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta l'identificatore per il trigger.<br/>                                                                                             |
| [**Ripetizione**](trigger-repetition.md)<br/>                 | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta un valore che indica la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'avvio dell'attività.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene o imposta la data e l'ora di attivazione del trigger.<br/>                                                                            |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Sola lettura<br/>  | Ereditato [**dall'oggetto Trigger.**](trigger.md) Ottiene il tipo del trigger.<br/>                                                                                                            |
| [**Userid**](logontrigger-userid.md)<br/>                    | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore dell'utente.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Se si desidera che un'attività sia attivata quando un membro di un gruppo accede al computer anziché quando un utente specifico accede, non assegnare un valore alla proprietà [**LogonTrigger.UserId.**](logontrigger-userid.md) Creare invece un trigger di accesso con una proprietà **LogonTrigger.UserId** vuota e assegnare un valore all'entità per l'attività usando la [**proprietà Principal.GroupId.**](principal-groupid.md)

Quando si legge o si scrive codice XML per un'attività, viene specificato un trigger di accesso usando l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Esempio di trigger di accesso (scripting).](logon-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 





