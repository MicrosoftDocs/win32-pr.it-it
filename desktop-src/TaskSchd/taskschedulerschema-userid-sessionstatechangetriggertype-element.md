---
title: Elemento UserId (sessionStateChangeTriggerType)
description: Contiene l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
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
ms.openlocfilehash: d6f6ddaf196f83d727e4641df6e59375033eb60c076451d70866d9d227ca457d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355576"
---
# <a name="userid-sessionstatechangetriggertype-element"></a>Elemento UserId (sessionStateChangeTriggerType)

Contiene l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

**L'elemento UserId** è definito dal tipo complesso [**sessionStateChangeTriggerType.**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                       | Derivato da                                                                                           | Descrizione                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando lo stato di una sessione di Terminal Server cambia.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà UserId di ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).

Per lo sviluppo di script, [**vedere SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





