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
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518586"
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

L'elemento **userid** è definito dal tipo complesso [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                       | Derivato da                                                                                           | Descrizione                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**userid Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).

Per lo sviluppo di script, vedere [**SessionStateChangeTrigger. UserID**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





