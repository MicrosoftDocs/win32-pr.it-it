---
title: Proprietà ExecAction. Arguments
description: Per gli script, ottiene o imposta gli argomenti associati all'operazione della riga di comando.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Proprietà Arguments Utilità di pianificazione
- Utilità di pianificazione proprietà arguments, oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, proprietà Arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963989"
---
# <a name="execactionarguments-property"></a>Proprietà ExecAction. Arguments

Per gli script, ottiene o imposta gli argomenti associati all'operazione della riga di comando.

## <a name="syntax"></a>Sintassi


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valore proprietà

Argomenti necessari per l'operazione della riga di comando.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, gli argomenti dell'operazione della riga di comando vengono specificati nell'elemento [**arguments**](taskschedulerschema-arguments-exectype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





