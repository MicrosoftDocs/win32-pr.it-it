---
title: Elemento StateChange (sessionStateChangeTriggerType)
description: Contiene il tipo di modifica della sessione di Terminal Server che attiverebbe l'avvio di un'attività.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- Elemento StateChange Utilità di pianificazione
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88b7e46b23cf6778379a967e03d8f168de3b18d20a734812bacdad940850136a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356333"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>Elemento StateChange (sessionStateChangeTriggerType)

Contiene il tipo di modifica della sessione di Terminal Server che attiverebbe l'avvio di un'attività.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

**L'elemento StateChange** è definito dal tipo complesso [**sessionStateChangeTriggerType.**](taskschedulerschema-sessionstatechangetriggertype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                       | Derivato da                                                                                           | Descrizione                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando lo stato di una sessione di Terminal Server cambia.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà StateChange di ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Per lo sviluppo di script, [**vedere SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





