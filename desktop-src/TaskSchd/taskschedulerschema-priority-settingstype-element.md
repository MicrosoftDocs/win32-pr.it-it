---
title: Elemento Priority (settingsType)
description: Specifica il livello di priorità per l'attività.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Elemento Priority Utilità di pianificazione
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11b71c88f63e7a3beb3c1c9ec8e1f3253bcd05a567ec5cd077f62175561ce2c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611893"
---
# <a name="priority-settingstype-element"></a>Elemento Priority (settingsType)

Specifica il livello di priorità per l'attività.

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

**L'elemento Priority** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Il livello di priorità 0 è la priorità più alta e il livello di priorità 10 è la priorità più bassa. Il valore predefinito è 7. I valori minimo e massimo vengono impostati dal [**tipo semplice priorityType.**](taskschedulerschema-prioritytype-simpletype.md) I livelli di priorità 7 e 8 vengono usati per le attività in background e i livelli di priorità 4, 5 e 6 vengono usati per le attività interattive.

L'azione dell'attività viene avviata in un processo con una priorità basata su un valore classe di priorità. Un valore livello di priorità (priorità del thread) viene usato per le azioni del gestore COM, della finestra di messaggio e dell'attività di posta elettronica. Per altre informazioni sui valori Classe di priorità e Livello di priorità, vedere [Priorità di pianificazione](/windows/desktop/ProcThread/scheduling-priorities). Nella tabella seguente sono elencati i valori possibili per **l'elemento Priority** e i valori Priority Class e Priority Level corrispondenti.



| Priorità attività | Classe Priority                 | Livello di priorità                   |
|---------------|--------------------------------|----------------------------------|
| 0             | CLASSE DI \_ PRIORITÀ IN \_ TEMPO REALE      | PRIORITÀ \_ THREAD \_ TIME \_ CRITICAL |
| 1             | CLASSE \_ CON \_ PRIORITÀ ALTA          | PRIORITÀ \_ THREAD \_ PIÙ ALTA        |
| 2             | CLASSE \_ DI PRIORITÀ SUPERIORE ALLA \_ \_ NORMALE | PRIORITÀ \_ DEL THREAD SUPERIORE ALLA \_ \_ NORMALE  |
| 3             | CLASSE \_ DI PRIORITÀ SUPERIORE ALLA \_ \_ NORMALE | PRIORITÀ \_ DEL THREAD SUPERIORE ALLA \_ \_ NORMALE  |
| 4             | CLASSE \_ DI PRIORITÀ \_ NORMALE        | PRIORITÀ \_ THREAD \_ NORMALE         |
| 5             | CLASSE \_ DI PRIORITÀ \_ NORMALE        | PRIORITÀ \_ THREAD \_ NORMALE         |
| 6             | CLASSE \_ DI PRIORITÀ \_ NORMALE        | PRIORITÀ \_ THREAD \_ NORMALE         |
| 7             | SOTTO \_ LA CLASSE DI PRIORITÀ \_ \_ NORMALE | PRIORITÀ \_ THREAD AL DI SOTTO DEL \_ \_ NORMALE  |
| 8             | SOTTO \_ LA CLASSE DI PRIORITÀ \_ \_ NORMALE | PRIORITÀ \_ THREAD AL DI SOTTO DEL \_ \_ NORMALE  |
| 9             | CLASSE \_ DI PRIORITÀ IDLE \_          | PRIORITÀ \_ THREAD \_ PIÙ BASSA         |
| 10            | CLASSE \_ DI PRIORITÀ IDLE \_          | PRIORITÀ \_ THREAD \_ INATTIVA           |



 

Per lo sviluppo C++, vedere [**Proprietà Priority di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Per lo sviluppo di script, vedere [**TaskSettings.Priority.**](tasksettings-priority.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

