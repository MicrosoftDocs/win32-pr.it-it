---
title: Esempio di creazione di un trigger inattivo
description: Per creare un trigger inattivo, è necessario specificare un trigger inattivo quando si crea il trigger ed è necessario impostare il tempo di inattività per l'attività. Per informazioni sulle condizioni di inattività, vedere condizioni di inattività.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338527"
---
# <a name="creating-an-idle-trigger-example"></a>Esempio di creazione di un trigger inattivo

Per creare un trigger inattivo, è necessario specificare un trigger inattivo quando si crea il trigger ed è necessario impostare il tempo di inattività per l'attività. Per informazioni sulle condizioni di inattività, vedere [condizioni](task-idle-conditions.md)di inattività.

Dopo aver creato il trigger inattivo, chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare il nuovo trigger su disco.

Nella procedura riportata di seguito viene descritto come creare un trigger inattivo per un'attività nota.

**Per creare un trigger inattivo per un'attività nota**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) per impostare per quanto tempo il sistema deve rimanere inattivo prima che il trigger venga attivato. (Si noti che **SetIdleWait** viene ereditato da [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).
4.  Definire la struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) e chiamare [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) per creare il trigger inattivo. (Si noti che **CreateTrigger** viene ereditato da [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)).
5.  Salvare l'attività con il nuovo trigger di inattività su disco con [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
6.  Chiamare **ITask:: Release** per rilasciare tutte le risorse. Si noti che la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).



| Per un esempio di codice di                         | Vedere                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Creazione di un trigger inattivo per un'attività esistente | [Esempio di codice C/C++: creazione di un trigger inattivo](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 