---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Specifica che l'Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Elemento StopOnIdleEnd Utilità di pianificazione
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e6497ca88d43b96096ee6a23ee81a322b0f397757466ed8cf09dd1b3cd45fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356059"
---
# <a name="stoponidleend-idlesettingstype-element"></a>Elemento StopOnIdleEnd (idleSettingsType)

Specifica che l'Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

**L'elemento StopOnIdleEnd** è definito dal tipo complesso [**idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in uno stato di inattività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, [**vedere Proprietà StopOnIdleEnd di IIdleSettings.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend)

Per lo sviluppo di script, [**vedere IdleSettings.StopOnIdleEnd.**](idlesettings-stoponidleend.md)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definita un'impostazione di inattività che indica che l'attività non deve essere eseguita al termine della condizione di inattività.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





