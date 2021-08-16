---
title: Elemento UserId (logonTriggerType)
description: Identificatore dell'utente. L'attività viene avviata quando l'utente accede al computer.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- Elemento UserId Utilità di pianificazione
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33a1e0f82a3005bfec8e689d088a8d8e28ebbf0a949e4288338d27e68c3a0314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355567"
---
# <a name="userid-logontriggertype-element"></a>Elemento UserId (logonTriggerType)

Identificatore dell'utente. L'attività viene avviata quando l'utente accede al computer.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

**L'elemento UserId** è definito dal [**tipo complesso logonTriggerType.**](taskschedulerschema-logontriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'identificatore utente per il trigger logon viene specificato usando la [**proprietà LogonTrigger.UserId.**](logontrigger-userid.md)

Per lo sviluppo in C++, l'identificatore utente per il trigger logon viene specificato usando la [**proprietà ILogonTrigger::UserId.**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger logon, vedere [Logon Trigger Example (XML) .](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





