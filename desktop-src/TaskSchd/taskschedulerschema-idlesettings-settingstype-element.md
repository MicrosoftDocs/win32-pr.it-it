---
title: Elemento IdleSettings (settingsType)
description: Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Utilità di pianificazione elemento IdleSettings
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120798"
---
# <a name="idlesettings-settingstype-element"></a>Elemento IdleSettings (settingsType)

Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo. Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

L'elemento **IdleSettings** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre

| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |

## <a name="child-elements"></a>Elementi figlio

> [!NOTE]
> Le impostazioni *Duration* e *WaitTimeout* sono deprecate. Sono ancora presenti nel Utilità di pianificazione interfaccia utente e i relativi metodi di interfaccia possono comunque restituire valori validi, ma non vengono più usati.

| Elemento                                                                                  | Tipo     | Descrizione                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Specifica se l'attività viene riavviata quando il computer scorre una condizione di inattività più volte.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Specifica che il Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.<br/> |
| **Deprecato**: [ **durata**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Specifica per quanto tempo il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.<br/>                              |
| **Deprecato**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Specifica la quantità di tempo per cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.<br/>                |

## <a name="remarks"></a>Commenti

Per lo sviluppo di script, le impostazioni di inattività vengono specificate utilizzando la proprietà [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .

Per lo sviluppo in C++, le impostazioni di inattività vengono specificate usando la proprietà [**ITaskSettings:: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un elemento Settings che consente Utilità di pianificazione di attendere 24 ore per una condizione di inattività e quindi consente solo 10 minuti {IdleDuration) di avviare l'attività.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |

## <a name="see-also"></a>Vedi anche

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)

[Utilità di pianificazione](task-scheduler-start-page.md)
