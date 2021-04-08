---
title: Proprietà EmailAction. Attachments
description: Per gli script, ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Utilità di pianificazione proprietà allegati
- Utilità di pianificazione proprietà allegati, oggetto EmailAction
- Utilità di pianificazione oggetto EmailAction, proprietà Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741903"
---
# <a name="emailactionattachments-property"></a>Proprietà EmailAction. Attachments

\[Questo oggetto non è più supportato. Per una soluzione alternativa, usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell.\]

Per gli script, ottiene o imposta una matrice di allegati inviati con il messaggio di posta elettronica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>Valore proprietà

Matrice di allegati inviata con il messaggio di posta elettronica.

## <a name="remarks"></a>Commenti

Un massimo di otto allegati può essere nella matrice di allegati.

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

 

