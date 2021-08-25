---
title: Proprietà EmailAction.HeaderFields
description: Per lo scripting, ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica che si vuole inviare.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- Proprietà HeaderFields Utilità di pianificazione
- Proprietà HeaderFields Utilità di pianificazione , oggetto EmailAction
- Oggetto EmailAction Utilità di pianificazione proprietà , HeaderFields
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8131528c3fec93a6df78b58c4eda76f1f78e7b996b74df1068e3be30b468d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100301"
---
# <a name="emailactionheaderfields-property"></a>Proprietà EmailAction.HeaderFields

\[Questo oggetto non è più supportato. Usare IExecAction con il cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) di PowerShell come soluzione alternativa.\]

Per lo scripting, ottiene o imposta le informazioni di intestazione nel messaggio di posta elettronica che si vuole inviare.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a>Valore proprietà

Informazioni sull'intestazione nel messaggio di posta elettronica da inviare.

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

 

