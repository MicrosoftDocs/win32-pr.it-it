---
title: Proprietà ExecAction.Arguments
description: Per lo scripting, ottiene o imposta gli argomenti associati all'operazione della riga di comando.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Proprietà Arguments Utilità di pianificazione
- Proprietà Arguments Utilità di pianificazione , oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione proprietà , Arguments
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
ms.openlocfilehash: 899e4ceaaf3a0d04dc678592add18184401d54569fea71f0570a0acbf2a33027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011491"
---
# <a name="execactionarguments-property"></a>Proprietà ExecAction.Arguments

Per lo scripting, ottiene o imposta gli argomenti associati all'operazione della riga di comando.

## <a name="syntax"></a>Sintassi


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valore proprietà

Argomenti necessari per l'operazione della riga di comando.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, gli argomenti dell'operazione della riga di comando vengono specificati [**nell'elemento Arguments**](taskschedulerschema-arguments-exectype-element.md) dello schema Utilità di pianificazione schema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





