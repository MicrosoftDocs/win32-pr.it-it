---
title: Elemento IdleSettings (settingsType)
description: Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in stato di inattività.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Elemento IdleSettings Utilità di pianificazione
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0a4c3fc978c93d13be8faa62012d3928d47da5b5a214ce50f5506992f1fc8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991220"
---
# <a name="idlesettings-settingstype-element"></a>Elemento IdleSettings (settingsType)

Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in stato di inattività. Per informazioni sulle condizioni di inattività, vedere [Condizioni di inattività delle attività](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

**L'elemento IdleSettings** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre

| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |

## <a name="child-elements"></a>Elementi figlio

> [!NOTE]
> Le *impostazioni Duration* e *WaitTimeout* sono deprecate. Sono ancora presenti nell'interfaccia Utilità di pianificazione utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.

| Elemento                                                                                  | Tipo     | Descrizione                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Specifica se l'attività viene riavviata quando il computer entra in una condizione di inattività più di una volta.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Specifica che l'Utilità di pianificazione interromperà l'attività se la condizione di inattività termina prima del completamento dell'attività.<br/> |
| **Deprecato:** [ **Durata**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Specifica per quanto tempo il computer deve essere inattivo prima dell'esecuzione dell'attività.<br/>                              |
| **Deprecato:** [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Specifica il periodo di tempo in cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.<br/>                |

## <a name="remarks"></a>Commenti

Per lo sviluppo di script, le impostazioni inattive vengono specificate tramite la [**proprietà TaskSettings.IdleSettings.**](tasksettings-idlesettings.md)

Per lo sviluppo C++, le impostazioni inattive vengono specificate usando la [**proprietà ITaskSettings::IdleSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento settings che consente Utilità di pianificazione di attendere 24 ore per una condizione di inattività e quindi consente solo 10 minuti {IdleDuration) per avviare l'attività.

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |

## <a name="see-also"></a>Vedi anche

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)

[Utilità di pianificazione](task-scheduler-start-page.md)
