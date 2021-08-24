---
title: Elemento Hidden (settingsType)
description: Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Elementi nascosti Utilità di pianificazione
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9820008ead01930eff23a50408f4952d08e9190984432f65c3d9e5f4eedbef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658911"
---
# <a name="hidden-settingstype-element"></a>Elemento Hidden (settingsType)

Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita. Tuttavia, gli amministratori possono eseguire l'override di questa impostazione tramite l'uso di un "commutatore master" che rende tutte le attività visibili nell'interfaccia utente.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**L'elemento Hidden** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà nascosta di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).

Per lo sviluppo di script, vedere [**TaskSettings.Hidden**](tasksettings-hidden.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





