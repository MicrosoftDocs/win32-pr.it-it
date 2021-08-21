---
title: Elemento RestartOnIdle (idleSettingsType)
description: Specifica se l'attività viene riavviata quando il computer si trova in una condizione di inattività più volte.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Elemento RestartOnIdle Utilità di pianificazione
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16a636ebc052bb04a150390659909f0b73cae78871acaacfb4ba529ea2d8e917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575141"
---
# <a name="restartonidle-idlesettingstype-element"></a>Elemento RestartOnIdle (idleSettingsType)

Specifica se l'attività viene riavviata quando il computer si trova in una condizione di inattività più volte.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

**L'elemento RestartOnIdle** è definito dal tipo complesso [**idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in stato di inattività.<br/> |



## <a name="remarks"></a>Commenti

Questo elemento viene usato solo se [**l'elemento TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) è impostato su True.

Per lo sviluppo di script, le impostazioni di questa attività vengono specificate usando la [**proprietà IdleSettings.RestartOnIdle.**](idlesettings-restartonidle.md)

Per lo sviluppo C++, le impostazioni di questa attività vengono specificate usando la [**proprietà IIdleSettings::RestartOnIdle.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'impostazione inattiva che indica che l'attività non deve essere riavviata quando la condizione di inattività viene cicliata.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





