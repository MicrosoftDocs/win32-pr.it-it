---
title: Oggetto ShowMessageAction
description: Per gli script, rappresenta un'azione che visualizza una finestra di messaggio quando un'attività viene attivata.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Utilità di pianificazione oggetto ShowMessageAction
- Oggetto ShowMessageAction Utilità di pianificazione, descritto
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
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400410"
---
# <a name="showmessageaction-object"></a>Oggetto ShowMessageAction

\[Questo oggetto non è più supportato. È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]

Per gli script, rappresenta un'azione che visualizza una finestra di messaggio quando un'attività viene attivata.

## <a name="members"></a>Membri

L'oggetto **ShowMessageAction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ShowMessageAction** dispone di queste proprietà.



| Proprietà                                                        | Tipo di accesso           | Descrizione                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ID**](action-id.md)<br/>                              | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**azione**](action.md) . Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.<br/>                |
| [**Titolo**](showmessageaction-title.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il titolo della finestra di messaggio.<br/>                                                     |
| [**Tipo**](action-type.md)<br/>                          | Sola lettura<br/>  | Ereditato dall'oggetto [**azione**](action.md) . Ottiene il tipo dell'azione.<br/>               |



 

## <a name="remarks"></a>Commenti

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo. Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività oppure nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, un'azione della finestra di messaggio viene specificata utilizzando l'elemento [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di finestra di messaggio (scripting)](/previous-versions//aa381916(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

