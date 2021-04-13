---
title: Proprietà EmailAction. Server
description: Per la creazione di script, ottiene o imposta il nome del server SMTP da usare per l'invio di messaggi di posta elettronica.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Utilità di pianificazione proprietà server
- Proprietà Server Utilità di pianificazione, oggetto EmailAction
- Utilità di pianificazione oggetto EmailAction, proprietà server
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340772"
---
# <a name="emailactionserver-property"></a>Proprietà EmailAction. Server

\[Questo oggetto non è più supportato. Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]

Per la creazione di script, ottiene o imposta il nome del server SMTP da usare per l'invio di messaggi di posta elettronica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valore proprietà

Nome del server utilizzato per l'invio di messaggi di posta elettronica.

## <a name="remarks"></a>Commenti

Verificare che il server SMTP che invia il messaggio di posta elettronica sia configurato correttamente. La posta elettronica viene inviata utilizzando l'autenticazione NTLM per i server SMTP di Windows, il che significa che le credenziali di sicurezza utilizzate per l'esecuzione dell'attività devono disporre anche dei privilegi sul server SMTP per l'invio di messaggi di posta elettronica. Se il server SMTP è un server non basato su Windows, il messaggio di posta elettronica verrà inviato se il server consente l'accesso anonimo. Per informazioni sulla configurazione del server SMTP, vedere [configurazione del server SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)e per informazioni sulla gestione delle impostazioni del server SMTP, vedere [Amministrazione SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

