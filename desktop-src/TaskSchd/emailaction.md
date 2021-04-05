---
title: Oggetto EmailAction
description: Oggetto di scripting che rappresenta un'azione che invia un messaggio di posta elettronica.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Utilità di pianificazione oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874385"
---
# <a name="emailaction-object"></a>Oggetto EmailAction

\[Questo oggetto non è più supportato. Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]

Oggetto di scripting che rappresenta un'azione che invia un messaggio di posta elettronica.

## <a name="members"></a>Membri

L'oggetto **EmailAction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **EmailAction** dispone di queste proprietà.



| Proprietà                                                    | Tipo di accesso           | Descrizione                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Allegati**](emailaction-attachments.md)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.<br/>                      |
| [**Bcc**](emailaction-bcc.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo o gli indirizzi di posta elettronica che si desidera includere nel messaggio di posta elettronica.<br/>         |
| [**Corpo**](emailaction-body.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.<br/>                            |
| [**CC**](emailaction-cc.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi da inserire in CC nel messaggio di posta elettronica.<br/>          |
| [**Da**](emailaction-from.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo di posta elettronica da cui si desidera inviare il messaggio di posta elettronica.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica che si desidera inviare.<br/>                        |
| [**ID**](action-id.md)<br/>                          | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**azione**](action.md) . Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo di posta elettronica a cui si desidera rispondere.<br/>                                      |
| [**Server**](emailaction-server.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il nome del server da utilizzare per l'invio di messaggi di posta elettronica.<br/>                           |
| [**Oggetto**](emailaction-subject.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto del messaggio di posta elettronica.<br/>                                                 |
| [**A**](emailaction-to.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo di posta elettronica o gli indirizzi a cui si desidera inviare il messaggio di posta elettronica.<br/>                |
| [**Tipo**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Sola lettura<br/>  | Ereditato dall'oggetto [**azione**](action.md) . Ottiene il tipo dell'azione.<br/>                   |



 

## <a name="remarks"></a>Commenti

L'azione di posta elettronica deve avere un valore valido per le proprietà [**Server**](emailaction-server.md), [**da**](emailaction-from.md)e [**a**](emailaction-to.md) o [**CC**](emailaction-cc.md) per la registrazione e l'esecuzione corretta dell'attività.

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificata un'azione di posta elettronica utilizzando l'elemento [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di evento (scripting)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

