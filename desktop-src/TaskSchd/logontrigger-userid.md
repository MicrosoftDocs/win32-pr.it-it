---
title: Proprietà LogonTrigger. UserId
description: Per lo scripting, ottiene o imposta l'identificatore dell'utente.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- Utilità di pianificazione proprietà UserId
- Utilità di pianificazione proprietà UserId, oggetto LogonTrigger
- Oggetto LogonTrigger Utilità di pianificazione, Proprietà UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400348"
---
# <a name="logontriggeruserid-property"></a>Proprietà LogonTrigger. UserId

Per lo scripting, ottiene o imposta l'identificatore dell'utente.

## <a name="syntax"></a>Sintassi


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore dell'utente. Ad esempio, "nome dominio \\ " o per un account locale, "Administrator".

Questa proprietà può essere in uno dei formati seguenti:

-   Nome utente o SID: l'attività viene avviata quando l'utente accede al computer.
-   NULL: l'attività viene avviata quando un utente accede al computer.

## <a name="remarks"></a>Commenti

Se si desidera che un'attività venga attivata quando un membro di un gruppo accede al computer anziché quando un utente specifico esegue l'accesso, non assegnare un valore alla proprietà **LogonTrigger. UserID** . In alternativa, creare un trigger LOGON con una proprietà **LogonTrigger. UserID** vuota e assegnare un valore all'entità per l'attività usando la proprietà [**Principal. GroupID**](principal-groupid.md) .

Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore utente di accesso viene specificato utilizzando l'elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





