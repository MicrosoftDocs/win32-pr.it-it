---
title: Proprietà ComHandlerAction. ClassID
description: Per gli script, ottiene o imposta l'identificatore della classe del gestore.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Utilità di pianificazione proprietà ClassID
- Utilità di pianificazione proprietà ClassID, oggetto ComHandlerAction
- Oggetto ComHandlerAction Utilità di pianificazione, proprietà ClassID
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740866"
---
# <a name="comhandleractionclassid-property"></a>Proprietà ComHandlerAction. ClassID

Per gli script, ottiene o imposta l'identificatore della classe del gestore.

## <a name="syntax"></a>Sintassi


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore della classe che definisce il gestore da attivare.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, la classe di un gestore COM viene specificata nell'elemento [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) dello schema utilità di pianificazione.

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
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





