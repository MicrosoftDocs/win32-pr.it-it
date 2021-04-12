---
title: Proprietà Principal.Id
description: Per lo scripting, ottiene o imposta l'identificatore dell'entità.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- ID Utilità di pianificazione proprietà
- Utilità di pianificazione proprietà ID, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400799"
---
# <a name="principalid-property"></a>Proprietà Principal.Id

Per lo scripting, ottiene o imposta l'identificatore dell'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.Id As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore dell'entità.

## <a name="remarks"></a>Commenti

Questo identificatore viene usato anche quando si specifica la proprietà [**ActionCollection. Context**](actioncollection-context.md) .

Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore dell'entità viene specificato nell'attributo ID dell'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActionCollection. Context**](actioncollection-context.md)
</dt> <dt>

[**Principale**](principal.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





