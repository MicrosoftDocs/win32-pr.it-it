---
title: T (Utilità di pianificazione)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517283"
---
# <a name="t-task-scheduler"></a>T (Utilità di pianificazione)

A B C D [E](e.md) F G H [i](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**oggetti attività**
</dt> <dd>

Istanze di un oggetto che fornisce i metodi per la gestione delle attività. Sono inclusi i metodi per l'impostazione e il recupero delle proprietà. esecuzione, terminazione ed eliminazione di attività; e la creazione di nuovi trigger e il recupero di trigger obsoleti.

L'oggetto attività viene creato da chiamate a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**oggetti utilità di pianificazione**
</dt> <dd>

Istanze di un oggetto che rappresenta il servizio Utilità di pianificazione. Questo oggetto supporta due interfacce: **IUnknown** e [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (attualmente le attività sono l'unico tipo di elementi di lavoro supportati dal servizio Utilità di pianificazione).

Gli oggetti utilità di pianificazione vengono creati tramite chiamate a **CoCreateInstance**.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**oggetti trigger attività**
</dt> <dd>

Istanze di un oggetto che fornisce i metodi per l'impostazione e il recupero di trigger di attività. Questo oggetto supporta due interfacce: **IUnknown** e [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).

Gli oggetti trigger di attività vengono creati tramite chiamate a [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) e [**IScheduledWorkItem:: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

Vedere anche: *trigger*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**attività**
</dt> <dd>

Qualsiasi elemento che può essere eseguito dal Utilità di pianificazione. Questi elementi possono includere uno degli elementi seguenti (come supportato dal sistema operativo in cui verrà eseguita l'attività): Win32® applicazioni, applicazioni Win16, applicazioni OS/2, MS-DOS® applicazioni, file batch ( \* . bat), file di comando ( \* cmd) o qualsiasi tipo di file registrato correttamente.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Cartella attività**
</dt> <dd>

La cartella in cui sono elencati tutti i file delle attività (attualmente, le attività sono gli unici elementi di lavoro disponibili). Questi file contengono le informazioni sull'attività. Il nome di questi file riflette il nome dell'attività.

È possibile recuperare il percorso della cartella attività dal registro di sistema ottenendo i dati per il valore seguente:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**trigger**
</dt> <dd>

Set di criteri che, se soddisfatti, comporterà l'esecuzione di un'attività. Utilità di pianificazione fornisce trigger basati sul tempo e sugli eventi che possono specificare gli orari di inizio, i criteri di ripetizione e altri parametri dell'attività.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**stringhe di trigger**
</dt> <dd>

Stringa che descrive il trigger. Questa stringa viene creata dal servizio Utilità di pianificazione e viene visualizzata nell'interfaccia utente Utilità di pianificazione in un formato simile a "alle 14:00 ogni giorno, a partire dal 5/11/97".

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**strutture trigger**
</dt> <dd>

Struttura [**del \_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) utilizzata durante l'impostazione o il recupero dei criteri che definiscono il trigger. I criteri includono quando il trigger viene attivato e il tipo del trigger.

</dd> </dl>

 

 




