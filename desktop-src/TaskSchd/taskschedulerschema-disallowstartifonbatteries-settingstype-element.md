---
title: Elemento DisallowStartIfOnBatteries (settingsType)
description: Specifica che l'attività non verrà avviata se il computer è in esecuzione con batterie.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Elemento DisallowStartIfOnBatteries Utilità di pianificazione
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efd78b3e868c41431521b4c584a4044b9086362cf55d86466eb38ed75fcee148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100041"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Elemento DisallowStartIfOnBatteries (settingsType)

Specifica che l'attività non verrà avviata se il computer è in esecuzione con batterie.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

**L'elemento DisallowStartIfOnBatteries** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'impostazione predefinita per questo elemento è True.

Per lo sviluppo di script, queste informazioni sono accessibili tramite la [**proprietà TaskSettings.DisallowStartIfOnBatteries.**](tasksettings-disallowstartifonbatteries.md)

Per lo sviluppo C++, queste informazioni sono accessibili tramite la proprietà [**ITaskSettings::D isallowStartIfOnBatteries.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento settings che non consente l'esecuzione dell'attività se il computer è in esecuzione a batteria.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





