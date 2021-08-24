---
title: Elemento StopIfGoingOnBatteries (settingsType)
description: Specifica che l'attività verrà arrestata se il computer sta caricando batterie.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Elemento StopIfGoingOnBatteries Utilità di pianificazione
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b92be11400d1dbb223115f11334e2a596e94e9df1fd018ce16e4a646c84825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516100"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>Elemento StopIfGoingOnBatteries (settingsType)

Specifica che l'attività verrà arrestata se il computer sta caricando batterie.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

**L'elemento StopIfGoingOnBatteries** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'impostazione predefinita per questo elemento è False. Si noti che il valore predefinito è stato modificato rispetto alle versioni precedenti di Utilità di pianificazione.

Per lo sviluppo di script, questa impostazione viene specificata tramite la [**proprietà TaskSettings.StopIfGoingOnBatteries.**](tasksettings-stopifgoingonbatteries.md)

Per lo sviluppo C++, questa impostazione viene specificata usando la [**proprietà ITaskSettings::StopIfGoingOnBatteries.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento settings che consente una terminazione hard dell'attività.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
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

 

 





