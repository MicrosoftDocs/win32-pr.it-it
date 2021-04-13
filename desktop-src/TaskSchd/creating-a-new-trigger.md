---
title: Creazione di un nuovo trigger
description: Per creare un trigger è necessario usare tre interfacce.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399387"
---
# <a name="creating-a-new-trigger"></a>Creazione di un nuovo trigger

Per creare un trigger è necessario usare tre interfacce. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce il metodo [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per la creazione dell'oggetto trigger, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fornisce il metodo [**ITaskTrigger:: setrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) per l'impostazione dei criteri per il trigger e l'interfaccia com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fornisce un metodo **Save** per salvare il nuovo trigger su disco.

Nella procedura riportata di seguito viene descritto come creare un nuovo trigger.

**Per creare un nuovo trigger**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per creare un oggetto trigger. (Si noti che [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) viene ereditato da [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).
4.  Definire una struttura di [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Si noti che i membri wBeginDay, wBeginMonth e wBeginYear **del \_ trigger di attività** devono essere impostati rispettivamente su un giorno, un mese e un anno validi.
5.  Chiamare [**ITaskTrigger:: setrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) per impostare i criteri del trigger.
6.  Salvare l'attività con il nuovo trigger su disco usando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
7.  Chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare tutte le risorse. Si noti che la **versione** è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).



| Per un esempio di codice di                       | Vedere                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Creazione di un nuovo trigger per un'attività esistente | [Esempio di codice C/C++: creazione di un trigger di attività](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 