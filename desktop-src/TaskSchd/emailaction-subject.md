---
title: Proprietà EmailAction.Subject
description: Per lo scripting, ottiene o imposta l'oggetto del messaggio di posta elettronica.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Proprietà subject Utilità di pianificazione
- Proprietà Subject Utilità di pianificazione , oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione proprietà , Subject
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
ms.openlocfilehash: 7474fa4b7a6de59fd59a98c27a4877ab10c1acb6beac3c1682fccd05702aa275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943788"
---
# <a name="emailactionsubject-property"></a>Proprietà EmailAction.Subject

\[Questo oggetto non è più supportato. Usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) di PowerShell come soluzione alternativa.\]

Per lo scripting, ottiene o imposta l'oggetto del messaggio di posta elettronica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Valore proprietà

Oggetto del messaggio di posta elettronica.

## <a name="remarks"></a>Commenti

Quando si imposta il valore di questa proprietà, il valore può essere testo recuperato da una risorsa .dll file. Viene usata una stringa specializzata per fare riferimento al testo del file di risorse. Il formato della stringa è $(@ Dll , ResourceID ) dove Dll è il percorso del file .dll che contiene la risorsa e ResourceID è l'identificatore per il testo \[ \] della \[ \] \[ \] \[ \] risorsa. Ad esempio, l'impostazione di questo valore della proprietà su $(@ %SystemRoot% System32ResourceName.dll, -101) imposta la proprietà sul valore del testo della risorsa con un identificatore uguale a \\ \\ -101 nel file diResourceName.dll %SystemRoot% \\ System32. \\

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
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

 

