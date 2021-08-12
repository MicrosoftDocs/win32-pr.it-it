---
title: Elemento UseUnifiedSchedulingEngine (settingsType)
description: Specifica che il motore di pianificazione unificato verrà utilizzato per eseguire questa attività.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Elemento UseUnifiedSchedulingEngine Utilità di pianificazione
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faf27ea132fb47e35cd248e183fbec0584cb5d44414d6cacda6baac0d595c32d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610454"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>Elemento UseUnifiedSchedulingEngine (settingsType)

Specifica che il motore di pianificazione unificato verrà utilizzato per eseguire questa attività.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**L'elemento UseUnifiedSchedulingEngine** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'impostazione predefinita per questo elemento è False.

Per lo sviluppo in C++, è possibile accedere a queste informazioni tramite la [**proprietà ITaskSettings2::UseUnifiedSchedulingEngine.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento settings che specifica che il motore di pianificazione unificato verrà usato per eseguire questa attività.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





