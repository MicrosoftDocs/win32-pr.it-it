---
title: Principal.UserId - proprietà
description: Per lo scripting, ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Proprietà UserId Utilità di pianificazione
- Proprietà UserId Utilità di pianificazione , oggetto Principal
- Proprietà UserId Utilità di pianificazione dell'oggetto Principal
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
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060029"
---
# <a name="principaluserid-property"></a>Principal.UserId - proprietà

Per lo scripting, ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valore proprietà

Identificatore utente necessario per eseguire l'attività.

## <a name="remarks"></a>Commenti

Non impostare questa proprietà se viene specificato un identificatore di gruppo nella [**proprietà GroupId.**](principal-groupid.md)

Quando si legge o si scrive codice XML per un'attività, l'identificatore utente per l'entità viene specificato usando [**l'elemento UserId**](taskschedulerschema-userid-principaltype-element.md) dello schema Utilità di pianificazione schema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**Principale**](principal.md)
</dt> <dt>

[**Principal.GroupId**](principal-groupid.md)
</dt> </dl>

 

 





