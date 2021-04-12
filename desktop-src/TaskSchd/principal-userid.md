---
title: Proprietà Principal. UserId
description: Per gli script, ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Utilità di pianificazione proprietà UserId
- Utilità di pianificazione proprietà UserId, oggetto Principal
- Utilità di pianificazione oggetto Principal, Proprietà UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120222"
---
# <a name="principaluserid-property"></a>Proprietà Principal. UserId

Per gli script, ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore utente necessario per eseguire l'attività.

## <a name="remarks"></a>Commenti

Non impostare questa proprietà se nella proprietà [**GroupID**](principal-groupid.md) viene specificato un identificatore di gruppo.

Durante la lettura o la scrittura di codice XML per un'attività, l'identificatore utente per l'entità viene specificato utilizzando l'elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) dello schema utilità di pianificazione.

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

[**Principale**](principal.md)
</dt> <dt>

[**Entità. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





