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
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400344"
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

L'elemento **Priority** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Il livello di priorità 0 è la priorità più alta e il livello di priorità 10 è la priorità più bassa. Il valore predefinito è 7. I valori minimo e massimo vengono impostati dal tipo semplice [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) . I livelli di priorità 7 e 8 vengono usati per le attività in background e i livelli di priorità 4, 5 e 6 vengono usati per le attività interattive.

L'azione dell'attività viene avviata in un processo con una priorità basata su un valore della classe di priorità. Un valore del livello di priorità (priorità thread) viene usato per le azioni del gestore COM, della finestra di messaggio e dell'attività di posta elettronica. Per ulteriori informazioni sui valori della classe di priorità e del livello di priorità, vedere [priorità di pianificazione](/windows/desktop/ProcThread/scheduling-priorities). Nella tabella seguente sono elencati i valori possibili per l'elemento **Priority** e i valori della classe di priorità e del livello di priorità corrispondenti.



| Priorità attività | Classe Priority                 | Livello di priorità                   |
|---------------|--------------------------------|----------------------------------|
| 0             | \_classe priorità in tempo reale \_      | \_tempo di priorità thread \_ \_ critico |
| 1             | \_classe con priorità alta \_          | \_priorità thread \_ più elevata        |
| 2             | \_classe di \_ priorità \_ normale sopra | \_priorità thread \_ superiore al \_ normale  |
| 3             | \_classe di \_ priorità \_ normale sopra | \_priorità thread \_ superiore al \_ normale  |
| 4             | \_classe di priorità normale \_        | priorità THREAD- \_ \_ normale         |
| 5             | \_classe di priorità normale \_        | priorità THREAD- \_ \_ normale         |
| 6             | \_classe di priorità normale \_        | priorità THREAD- \_ \_ normale         |
| 7             | classe di priorità inferiore al \_ normale \_ \_ | priorità THREAD al di \_ \_ sotto del \_ normale  |
| 8             | classe di priorità inferiore al \_ normale \_ \_ | priorità THREAD al di \_ \_ sotto del \_ normale  |
| 9             | \_classe priorità INattiva \_          | \_priorità thread \_ più bassa         |
| 10            | \_classe priorità INattiva \_          | \_priorità thread \_ inattiva           |



 

Per lo sviluppo in C++, vedere [**proprietà Priority di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Per lo sviluppo di script, vedere [**TaskSettings. Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

