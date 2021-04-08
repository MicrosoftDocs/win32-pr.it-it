---
title: Proprietà TaskSettings. Hidden
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività non sarà visibile nell'interfaccia utente.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Utilità di pianificazione proprietà nascosta
- Utilità di pianificazione proprietà nascosta, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà Hidden
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742738"
---
# <a name="tasksettingshidden-property"></a>Proprietà TaskSettings. Hidden

Per gli script, ottiene o imposta un valore booleano che indica che l'attività non sarà visibile nell'interfaccia utente. Tuttavia, gli amministratori possono eseguire l'override di questa impostazione tramite l'uso di un "Master switch" che rende visibili tutte le attività nell'interfaccia utente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se **true**, il valore indica che l'attività non sarà visibile nell'interfaccia utente. Se **false**, l'attività sarà visibile nell'interfaccia utente. Il valore predefinito è **False**.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





