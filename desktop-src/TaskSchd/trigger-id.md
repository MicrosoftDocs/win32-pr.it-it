---
title: Proprietà Trigger.Id
description: Per lo scripting, ottiene o imposta l'identificatore per il trigger.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- ID Utilità di pianificazione proprietà
- ID Utilità di pianificazione proprietà, oggetto trigger
- Trigger Utilità di pianificazione oggetto, proprietà ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517559"
---
# <a name="triggerid-property"></a>Proprietà Trigger.Id

Per lo scripting, ottiene o imposta l'identificatore per il trigger.

## <a name="syntax"></a>Sintassi


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore del trigger. Questo identificatore viene utilizzato dal Utilità di pianificazione a scopo di registrazione.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore del trigger viene specificato nell'attributo ID dei singoli elementi trigger (ad esempio, l'attributo ID dell'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





