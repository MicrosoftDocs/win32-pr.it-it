---
title: Elemento Enabled (settingsType)
description: Specifica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è True.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Elemento enabled Utilità di pianificazione
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff198520e354147ff092b2374bb5a766e1ce1c6db6a4b8fc6302b92670bddcda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131870"
---
# <a name="enabled-settingstype-element"></a>Elemento Enabled (settingsType)

Specifica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è True.

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

**L'elemento Enabled** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà Enabled di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).

Per lo sviluppo di script, vedere [**TaskSettings.Enabled**](tasksettings-enabled.md).

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività abilitata, vedere [Time Trigger Example (XML) .](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





