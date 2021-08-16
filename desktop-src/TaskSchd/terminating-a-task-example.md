---
title: Esempio di terminazione di un'attività
description: È possibile terminare un'attività mentre è in esecuzione chiamando IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2705687b5383589c297348b1b5efa805b8ab407aeaef1c8c1213b1f9f6b0e894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354773"
---
# <a name="terminating-a-task-example"></a>Esempio di terminazione di un'attività

È possibile terminare un'attività mentre è in esecuzione chiamando [**IScheduledWorkItem::Terminate.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)

Nella procedura seguente viene descritto come terminare un'attività se è in esecuzione.

**Per terminare un'attività se è in esecuzione**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate per**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che in questo esempio viene recuperata l'attività "Test Task".
3.  Chiamare **ITask::GetStatus** per verificare se l'attività è in esecuzione. Si noti che [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) è un [**metodo IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Controllare lo stato dell'attività e quindi chiamare **ITask::Terminate** se l'attività è in esecuzione. Si noti che [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) è un [**metodo IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Per un esempio di codice di                | Vedere                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Verifica dello stato di un'attività nota | [Esempio di codice C/C++: terminazione di un'attività](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 