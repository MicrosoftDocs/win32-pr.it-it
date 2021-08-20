---
title: Oggetto ShowMessageAction
description: Per lo scripting, rappresenta un'azione che visualizza una finestra di messaggio quando viene attivata un'attività.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Oggetto ShowMessageAction Utilità di pianificazione
- Oggetto ShowMessageAction Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2daec97e66c160cc9da1369e44970f5d9e9ee7c5dcbbcea14cee1e4847a9df0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132367"
---
# <a name="showmessageaction-object"></a>Oggetto ShowMessageAction

\[Questo oggetto non è più supportato. È possibile usare IExecAction con la Windows di scripting [**msgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]

Per lo scripting, rappresenta un'azione che visualizza una finestra di messaggio quando viene attivata un'attività.

## <a name="members"></a>Membri

**L'oggetto ShowMessageAction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ShowMessageAction** ha queste proprietà.



| Proprietà                                                        | Tipo di accesso           | Descrizione                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Id**](action-id.md)<br/>                              | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto**](action.md) Action. Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.<br/>                |
| [**Titolo**](showmessageaction-title.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il titolo della finestra di messaggio.<br/>                                                     |
| [**Tipo**](action-type.md)<br/>                          | Sola lettura<br/>  | Ereditato [**dall'oggetto**](action.md) Action. Ottiene il tipo dell'azione.<br/>               |



 

## <a name="remarks"></a>Commenti

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività ha un tipo di accesso interattivo. Per impostare il tipo di accesso all'attività su interattivo, specificare 3 (**TASK \_ LOGON INTERACTIVE \_ \_ TOKEN**) o 4 (**TASK LOGON \_ \_ GROUP**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività o nel *parametro logonType* di [**TaskFolder.RegisterTask**](taskfolder-registertask.md) o [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Durante la lettura o la scrittura di codice XML personalizzato per un'attività, viene specificata un'azione della finestra di messaggio usando [**l'elemento ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Esempio di finestra di messaggio (scripting).](/previous-versions//aa381916(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

