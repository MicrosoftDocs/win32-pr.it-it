---
title: TaskSettings.Priority - proprietà
description: Per lo scripting, ottiene o imposta il livello di priorità dell'attività.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Proprietà Priority Utilità di pianificazione
- Proprietà Priority Utilità di pianificazione , oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b24c0281e8df314b070e0569176899b96071e1ef43caab17af4978e74f6b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354828"
---
# <a name="tasksettingspriority-property"></a>TaskSettings.Priority - proprietà

Per lo scripting, ottiene o imposta il livello di priorità dell'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Valore proprietà

Livello di priorità (0-10) dell'attività. Il valore predefinito è 7.

## <a name="remarks"></a>Commenti

Il livello di priorità 0 è la priorità più alta e il livello di priorità 10 è la priorità più bassa. Il valore predefinito è 7. I livelli di priorità 7 e 8 vengono usati per le attività in background e i livelli di priorità 4, 5 e 6 vengono usati per le attività interattive.

L'azione dell'attività viene avviata in un processo con una priorità basata su un valore classe di priorità. Un valore livello di priorità (priorità del thread) viene usato per le azioni del gestore COM, della finestra di messaggio e dell'attività di posta elettronica. Per altre informazioni sui valori Classe di priorità e Livello di priorità, vedere [Priorità di pianificazione](/windows/desktop/ProcThread/scheduling-priorities). Nella tabella seguente sono elencati i valori possibili per il *parametro priority* e i valori Priority Class e Priority Level corrispondenti.



| Priorità *attività* | Classe Priority                 | Livello di priorità                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | CLASSE DI \_ PRIORITÀ IN \_ TEMPO REALE      | PRIORITÀ \_ THREAD \_ TIME \_ CRITICAL |
| 1               | CLASSE \_ CON \_ PRIORITÀ ALTA          | PRIORITÀ \_ THREAD \_ PIÙ ALTA        |
| 2               | CLASSE \_ DI PRIORITÀ SUPERIORE ALLA \_ \_ NORMALE | PRIORITÀ \_ DEL THREAD SUPERIORE ALLA \_ \_ NORMALE  |
| 3               | CLASSE \_ DI PRIORITÀ SUPERIORE ALLA \_ \_ NORMALE | PRIORITÀ \_ DEL THREAD SUPERIORE ALLA \_ \_ NORMALE  |
| 4               | CLASSE \_ DI PRIORITÀ \_ NORMALE        | PRIORITÀ \_ THREAD \_ NORMALE         |
| 5               | CLASSE \_ DI PRIORITÀ \_ NORMALE        | PRIORITÀ \_ THREAD \_ NORMALE         |
| 6               | CLASSE \_ DI PRIORITÀ \_ NORMALE        | PRIORITÀ \_ THREAD \_ NORMALE         |
| 7               | SOTTO \_ LA CLASSE DI PRIORITÀ \_ \_ NORMALE | PRIORITÀ \_ THREAD AL DI SOTTO DEL \_ \_ NORMALE  |
| 8               | SOTTO \_ LA CLASSE DI PRIORITÀ \_ \_ NORMALE | PRIORITÀ \_ THREAD AL DI SOTTO DEL \_ \_ NORMALE  |
| 9               | CLASSE \_ DI PRIORITÀ IDLE \_          | PRIORITÀ \_ THREAD \_ PIÙ BASSA         |
| 10              | CLASSE \_ DI PRIORITÀ IDLE \_          | PRIORITÀ \_ THREAD \_ INATTIVA           |



 

Quando si legge o si scrive codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) dello schema Utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

