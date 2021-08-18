---
title: Esempi di impostazione delle proprietà degli elementi di lavoro
description: Per impostare le proprietà di un elemento di lavoro, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per impostare la proprietà dell'attività a cui si è interessati. Attualmente, gli unici elementi di lavoro validi sono attività.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- impostazione delle proprietà degli elementi di lavoro Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a29ff08c4f9129b8dc9ab749cd6db5807fd0c52449e48b64d5f3b36631fef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402541"
---
# <a name="setting-work-item-property-examples"></a>Esempi di impostazione delle proprietà degli elementi di lavoro

Per impostare le proprietà di un elemento di lavoro, chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per impostare la proprietà dell'attività a cui si è interessati. Attualmente, gli unici elementi di lavoro validi sono attività.

Gli esempi di codice elencati nella parte inferiore della pagina illustrano come impostare le proprietà che si applicano a tutti gli elementi di lavoro. Per altre proprietà univoche per le attività, vedere [Impostazione di esempi di proprietà delle attività](setting-task-property-examples.md).

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Negli esempi seguenti l'oggetto modificato viene sempre salvato su disco da una chiamata a [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). [**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia COM standard ereditata dall'oggetto attività.

La procedura seguente descrive come impostare una proprietà dell'attività.

**Per impostare una proprietà dell'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questi esempi presuppongono che il Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che le attività sono attualmente l'unico tipo di elemento di lavoro valido.
3.  Chiamare il metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) appropriato per impostare la proprietà a cui si è interessati. Si noti **che i metodi IScheduledWorkItem** vengono ereditati dall'interfaccia [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Chiamare [**IPersistFile::Save per**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) archiviare l'oggetto attività modificato su disco.



| Per un esempio di codice di                            | Vedere                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Impostazione delle informazioni sull'account per un'attività nota | [Esempio di codice C/C++: Impostazione delle informazioni sull'account attività](c-c-code-example-setting-task-account-information.md) |
| Impostazione del commento di un'attività nota              | [Esempio di codice C/C++: Impostazione del commento dell'attività](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 