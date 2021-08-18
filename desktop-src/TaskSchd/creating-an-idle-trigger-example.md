---
title: Esempio di creazione di un trigger inattivo
description: Per creare un trigger inattivo, è necessario specificare un trigger inattivo quando si crea il trigger ed è necessario impostare il tempo di inattività per l'attività. Per informazioni sulle condizioni di inattività, vedere Condizioni di inattività delle attività.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac38eb3eb7520fde552f009a718fe188d247e3f9fef943f0f0f79ba6ea85970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139544"
---
# <a name="creating-an-idle-trigger-example"></a>Esempio di creazione di un trigger inattivo

Per creare un trigger inattivo, è necessario specificare un trigger inattivo quando si crea il trigger ed è necessario impostare il tempo di inattività per l'attività. Per informazioni sulle condizioni di inattività, vedere [Condizioni di inattività delle attività.](task-idle-conditions.md)

Dopo aver creato il trigger inattivo, chiamare [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare il nuovo trigger su disco.

Nella procedura seguente viene descritto come creare un trigger inattivo per un'attività nota.

**Per creare un trigger inattivo per un'attività nota**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate per**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che in questo esempio viene recuperata l'attività "Test Task".
3.  Chiamare [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) per impostare per quanto tempo il sistema deve rimanere inattivo prima che il trigger venga attivato. Si noti che **SetIdleWait** viene ereditato da [**IScheduledWorkItem.**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
4.  Definire la [**struttura TASK \_ TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) e chiamare [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per creare il trigger inattivo. Si noti che **CreateTrigger** viene ereditato da [**IScheduledWorkItem.**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
5.  Salvare l'attività con il nuovo trigger inattivo su disco [**usando IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). [**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia COM standard supportata dall'interfaccia [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
6.  Chiamare **ITask::Release** per rilasciare tutte le risorse. Si noti che [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un [**metodo IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Per un esempio di codice di                         | Vedere                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Creazione di un trigger inattivo per un'attività esistente | [Esempio di codice C/C++: creazione di un trigger inattivo](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 