---
title: ComHandlerAction.ClassId - proprietà
description: Per lo scripting, ottiene o imposta l'identificatore della classe del gestore.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Proprietà ClassId Utilità di pianificazione
- Proprietà ClassId Utilità di pianificazione, oggetto ComHandlerAction
- Oggetto ComHandlerAction Utilità di pianificazione proprietà , ClassId
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
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100461"
---
# <a name="comhandleractionclassid-property"></a>ComHandlerAction.ClassId - proprietà

Per lo scripting, ottiene o imposta l'identificatore della classe del gestore.

## <a name="syntax"></a>Sintassi


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore della classe che definisce il gestore da attivato.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, la classe di un gestore COM viene specificata [**nell'elemento ClassId**](taskschedulerschema-classid-comhandlertype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





