---
title: EmailAction.Server - proprietà
description: Per lo scripting, ottiene o imposta il nome del server SMTP da cui inviare messaggi di posta elettronica.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Proprietà server Utilità di pianificazione
- Proprietà server Utilità di pianificazione , oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione proprietà Server
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
ms.openlocfilehash: 3348b067698cfdcf3c7dbb95a97b6dd23f0f0cb7ca9225d70a9bb3d4ce2a93b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100261"
---
# <a name="emailactionserver-property"></a>EmailAction.Server - proprietà

\[Questo oggetto non è più supportato. Usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell come soluzione alternativa.\]

Per lo scripting, ottiene o imposta il nome del server SMTP da cui inviare messaggi di posta elettronica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valore proprietà

Nome del server da cui inviare messaggi di posta elettronica.

## <a name="remarks"></a>Commenti

Verificare che il server SMTP che invia il messaggio di posta elettronica sia configurato correttamente. I messaggi di posta elettronica vengono inviati utilizzando l'autenticazione NTLM per i server SMTP di Windows, il che significa che le credenziali di sicurezza utilizzate per l'esecuzione dell'attività devono avere anche privilegi sul server SMTP per inviare messaggi di posta elettronica. Se il server SMTP è un server non Windows, il messaggio di posta elettronica verrà inviato se il server consente l'accesso anonimo. Per informazioni sulla configurazione del server SMTP, vedere Smtp [Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)e per informazioni sulla gestione delle impostazioni del server SMTP, vedere [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                    |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

