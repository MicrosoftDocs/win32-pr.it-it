---
title: Creazione di un nuovo trigger
description: Per creare un trigger è necessario usare tre interfacce.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0111fe8c45fdac5618407500b2168bf09c4ec01c5d68e78342f14d6bf103ff78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100441"
---
# <a name="creating-a-new-trigger"></a>Creazione di un nuovo trigger

Per creare un trigger è necessario usare tre interfacce. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce il metodo [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per la creazione dell'oggetto trigger, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fornisce il metodo [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) per impostare i criteri per il trigger e l'interfaccia COM [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fornisce un metodo **Save** per salvare il nuovo trigger su disco.

Nella procedura seguente viene descritto come creare un nuovo trigger.

**Per creare un nuovo trigger**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate per**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che in questo esempio viene recuperata l'attività "Test Task".
3.  Chiamare [**CreateTrigger per**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) creare un oggetto trigger. Si noti che [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) viene ereditato da [**IScheduledWorkItem.**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
4.  Definire una [**struttura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Si noti che i membri wBeginDay, wBeginMonth e wBeginYear di **TASK \_ TRIGGER** devono essere impostati rispettivamente su un giorno, un mese e un anno validi.
5.  Chiamare [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) per impostare i criteri del trigger.
6.  Salvare l'attività con il nuovo trigger su disco [**usando IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). [**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia COM standard supportata dall'interfaccia [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
7.  Chiamare [**Release per**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) rilasciare tutte le risorse. Si noti che **Release** è un [**metodo IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Per un esempio di codice di                       | Vedere                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Creazione di un nuovo trigger per un'attività esistente | [Esempio di codice C/C++: creazione di un trigger di attività](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 