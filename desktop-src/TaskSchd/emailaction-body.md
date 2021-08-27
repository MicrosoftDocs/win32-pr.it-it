---
title: EmailAction.Body - proprietà
description: Per lo scripting, ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Proprietà body Utilità di pianificazione
- Proprietà Body Utilità di pianificazione, oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione proprietà , Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57daf8d16da9f77a88d91a23cfaea88d1c3e27adb09a0d502b447b5987fce2ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100381"
---
# <a name="emailactionbody-property"></a>EmailAction.Body - proprietà

\[Questo oggetto non è più supportato. Usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell come soluzione alternativa.\]

Per lo scripting, ottiene o imposta il corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Valore proprietà

Corpo del messaggio di posta elettronica che contiene il messaggio di posta elettronica.

## <a name="remarks"></a>Commenti

Quando si imposta il valore di questa proprietà, il valore può essere testo recuperato da una risorsa .dll file. Una stringa specializzata viene usata per fare riferimento al testo dal file di risorse. Il formato della stringa è $(@ Dll , ResourceID ) dove Dll è il percorso del file .dll che contiene la risorsa e ResourceID è l'identificatore per il testo \[ \] della \[ \] \[ \] \[ \] risorsa. Ad esempio, l'impostazione del valore di questa proprietà su $(@ %SystemRoot% System32ResourceName.dll, -101) imposta la proprietà sul valore del testo della risorsa con un identificatore uguale a \\ \\ -101 nel file diResourceName.dll %SystemRoot% \\ System32. \\

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

 

