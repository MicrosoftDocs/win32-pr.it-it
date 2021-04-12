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
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519109"
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

L'elemento **userid** è definito dal tipo complesso [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, l'identificatore utente per il trigger LOGON viene specificato mediante la proprietà [**LogonTrigger. UserID**](logontrigger-userid.md) .

Per lo sviluppo in C++, l'identificatore utente per il trigger LOGON viene specificato tramite la proprietà [**ILogonTrigger:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che specifica un trigger LOGON, vedere [esempio di trigger LOGON (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





