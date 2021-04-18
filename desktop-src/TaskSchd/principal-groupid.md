---
title: Proprietà Principal. GroupId
description: Per gli script, ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Utilità di pianificazione proprietà GroupId
- Utilità di pianificazione proprietà GroupId, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302013"
---
# <a name="principalgroupid-property"></a>Proprietà Principal. GroupId

Per gli script, ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore del gruppo di utenti associato a questa entità.

## <a name="remarks"></a>Commenti

Non impostare questa proprietà se nella proprietà [**userid**](principal-userid.md) viene specificato un identificatore utente.

Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore di gruppo per un'entità viene specificato nell'elemento [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UserId**](principal-userid.md)
</dt> <dt>

[**Principale**](principal.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





