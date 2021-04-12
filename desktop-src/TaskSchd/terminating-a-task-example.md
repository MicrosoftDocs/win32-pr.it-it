---
title: Chiusura di un esempio di attività
description: È possibile terminare un'attività mentre è in esecuzione chiamando IScheduledWorkItem terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223971"
---
# <a name="terminating-a-task-example"></a>Chiusura di un esempio di attività

È possibile terminare un'attività mentre è in esecuzione chiamando [**IScheduledWorkItem:: terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).

Nella procedura riportata di seguito viene descritto come terminare un'attività se è in esecuzione.

**Per terminare un'attività se è in esecuzione**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare **ITask:: GetStatus** per verificare se l'attività è in esecuzione. (Si noti che [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).
4.  Verificare lo stato dell'attività e quindi chiamare **ITask:: terminate** se l'attività è in esecuzione. (Si noti che [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).



| Per un esempio di codice di                | Vedere                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Verifica dello stato di un'attività nota | [Esempio di codice C/C++: terminazione di un'attività](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 