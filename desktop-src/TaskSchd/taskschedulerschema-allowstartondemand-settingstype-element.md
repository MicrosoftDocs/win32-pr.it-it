---
title: Elemento AllowStartOnDemand (settingsType)
description: Specifica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Elemento AllowStartOnDemand Utilità di pianificazione
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be89197c4ae88188fc1d2a746c40d69e385edc7ba08aaf2d3bf29067ee5f4a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516991"
---
# <a name="allowstartondemand-settingstype-element"></a>Elemento AllowStartOnDemand (settingsType)

Specifica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

**L'elemento AllowStartOnDemand** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Quando questo elemento è impostato su True, l'attività può essere avviata indipendentemente dal momento in cui qualsiasi trigger avvia l'attività.

Per lo sviluppo C++, vedere la [**proprietà AllowDemandStart di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Per lo sviluppo di script, [**vedere TaskSettings.AllowDemandStart.**](tasksettings-allowdemandstart.md)

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che consente l'avvio della domanda, vedere [Time Trigger Example (XML) ( Esempio di trigger temporale (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





