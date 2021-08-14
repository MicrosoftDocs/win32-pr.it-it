---
title: Elemento GroupId (principalType)
description: Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Elemento GroupId Utilità di pianificazione
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131840"
---
# <a name="groupid-principaltype-element"></a>Elemento GroupId (principalType)

Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

**L'elemento GroupId** è definito dal [**tipo complesso principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Non è possibile specificare contemporaneamente un identificatore di gruppo e un identificatore utente. Specificare gli [**elementi UserId**](taskschedulerschema-userid-principaltype-element.md) **o GroupId,** ma non entrambi.

Per lo sviluppo di script, l'identificatore di gruppo dell'entità viene specificato usando la [**proprietà Principal.GroupId.**](principal-groupid.md)

Per lo sviluppo in C++, l'identificatore di gruppo dell'entità viene specificato usando la [**proprietà IPrincipal::GroupId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa questo elemento, vedere [Logon Trigger Example (XML) .](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





