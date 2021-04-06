---
title: Proprietà TaskSettings. Priority
description: Per lo scripting, ottiene o imposta il livello di priorità dell'attività.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Proprietà Priority Utilità di pianificazione
- Utilità di pianificazione proprietà priorità, oggetto TaskSettings
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
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963855"
---
# <a name="tasksettingspriority-property"></a>Proprietà TaskSettings. Priority

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

L'azione dell'attività viene avviata in un processo con una priorità basata su un valore della classe di priorità. Un valore del livello di priorità (priorità thread) viene usato per le azioni del gestore COM, della finestra di messaggio e dell'attività di posta elettronica. Per ulteriori informazioni sui valori della classe di priorità e del livello di priorità, vedere [priorità di pianificazione](/windows/desktop/ProcThread/scheduling-priorities). Nella tabella seguente sono elencati i valori possibili per il parametro *Priority* e i valori della classe di priorità e del livello di priorità corrispondenti.



| *Priorità* attività | Classe Priority                 | Livello di priorità                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | \_classe priorità in tempo reale \_      | \_tempo di priorità thread \_ \_ critico |
| 1               | \_classe con priorità alta \_          | \_priorità thread \_ più elevata        |
| 2               | \_classe di \_ priorità \_ normale sopra | \_priorità thread \_ superiore al \_ normale  |
| 3               | \_classe di \_ priorità \_ normale sopra | \_priorità thread \_ superiore al \_ normale  |
| 4               | \_classe di priorità normale \_        | priorità THREAD- \_ \_ normale         |
| 5               | \_classe di priorità normale \_        | priorità THREAD- \_ \_ normale         |
| 6               | \_classe di priorità normale \_        | priorità THREAD- \_ \_ normale         |
| 7               | classe di priorità inferiore al \_ normale \_ \_ | priorità THREAD al di \_ \_ sotto del \_ normale  |
| 8               | classe di priorità inferiore al \_ normale \_ \_ | priorità THREAD al di \_ \_ sotto del \_ normale  |
| 9               | \_classe priorità INattiva \_          | \_priorità thread \_ più bassa         |
| 10              | \_classe priorità INattiva \_          | \_priorità thread \_ inattiva           |



 

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

