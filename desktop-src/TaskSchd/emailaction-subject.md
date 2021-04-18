---
title: Proprietà EmailAction. Subject
description: Per lo scripting, ottiene o imposta l'oggetto del messaggio di posta elettronica.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Proprietà Subject Utilità di pianificazione
- Utilità di pianificazione proprietà Subject, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione, proprietà Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304746"
---
# <a name="emailactionsubject-property"></a>Proprietà EmailAction. Subject

\[Questo oggetto non è più supportato. Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) di PowerShell.\]

Per lo scripting, ottiene o imposta l'oggetto del messaggio di posta elettronica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Valore proprietà

Oggetto del messaggio di posta elettronica.

## <a name="remarks"></a>Commenti

Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll. Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse. Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa. Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.

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

 

