---
title: Oggetto EmailAction
description: Oggetto di scripting che rappresenta un'azione che invia un messaggio di posta elettronica.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Oggetto EmailAction Utilità di pianificazione
- Oggetto EmailAction Utilità di pianificazione , descritto
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
ms.openlocfilehash: c918065515322696a33114d2d9b09b7b72d12eb6b74e120a7963835a23321fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002479"
---
# <a name="emailaction-object"></a>Oggetto EmailAction

\[Questo oggetto non è più supportato. Usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell come soluzione alternativa.\]

Oggetto di scripting che rappresenta un'azione che invia un messaggio di posta elettronica.

## <a name="members"></a>Membri

**L'oggetto EmailAction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto EmailAction** ha queste proprietà.



| Proprietà                                                    | Tipo di accesso           | Descrizione                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Allegati**](emailaction-attachments.md)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.<br/>                      |
| [**Bcc**](emailaction-bcc.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo o gli indirizzi di posta elettronica da inserire nel messaggio di posta elettronica.<br/>         |
| [**Corpo**](emailaction-body.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.<br/>                            |
| [**Cc**](emailaction-cc.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo o gli indirizzi di posta elettronica da cc nel messaggio di posta elettronica.<br/>          |
| [**Da**](emailaction-from.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo di posta elettronica da cui si vuole inviare il messaggio di posta elettronica.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica da inviare.<br/>                        |
| [**Id**](action-id.md)<br/>                          | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto**](action.md) Action. Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo di posta elettronica a cui si vuole rispondere.<br/>                                      |
| [**Server**](emailaction-server.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il nome del server da cui inviare messaggi di posta elettronica.<br/>                           |
| [**Oggetto**](emailaction-subject.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto del messaggio di posta elettronica.<br/>                                                 |
| [**A**](emailaction-to.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l'indirizzo o gli indirizzi di posta elettronica a cui si vuole inviare il messaggio di posta elettronica.<br/>                |
| [**Tipo**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Sola lettura<br/>  | Ereditato [**dall'oggetto**](action.md) Action. Ottiene il tipo dell'azione.<br/>                   |



 

## <a name="remarks"></a>Commenti

Per eseguire correttamente la registrazione e l'esecuzione [](emailaction-to.md) dell'attività, [](emailaction-from.md)l'azione di posta elettronica deve avere un valore valido per le proprietà [**Server**](emailaction-server.md), Da e A o [**Cc**](emailaction-cc.md) .

Durante la lettura o la scrittura di codice XML personalizzato per un'attività, viene specificata un'azione di posta elettronica usando l'elemento [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) dello schema Utilità di pianificazione dati.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Esempio di trigger di evento (scripting).](/previous-versions//aa446887(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

