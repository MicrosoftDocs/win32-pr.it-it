---
title: Esempio di recupero di stringhe di trigger
description: È possibile recuperare le stringhe di trigger di un trigger noto usando l'interfaccia IScheduledWorkItem o ITaskTrigger, a seconda del tipo di oggetto in uso.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recupero di stringhe di trigger Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a05f95f19aaa68927059c87f7a73f162266454137fbe088923b25dce7ed3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002379"
---
# <a name="retrieving-trigger-strings-example"></a>Esempio di recupero di stringhe di trigger

È possibile recuperare le stringhe di trigger di un trigger noto usando [**l'interfaccia IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) o [**ITaskTrigger,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) a seconda del tipo di oggetto in uso.

Quando si usa un [*oggetto attività*](t.md), usare i metodi dell'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) per recuperare le stringhe di trigger di un elemento di lavoro.

Quando si usa un oggetto [*trigger*](t.md)di attività, usare i metodi dell'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) per recuperare la stringa di trigger del trigger.

L'esempio seguente illustra come usare [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) per visualizzare le stringhe di tutti i trigger associati a un'attività nota.

La procedura seguente descrive come recuperare le stringhe di trigger di un'attività.

**Per recuperare le stringhe di trigger di un'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio ottiene l'attività "Test Task".
3.  Chiamare **ITask::GetTriggerCount** per scoprire quanti trigger sono associati a un'attività. Si noti che [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) è un [**metodo IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Visualizzare le stringhe di trigger, chiamando **ITask::GetTriggerString** per ogni trigger associato all'attività. Si noti che [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) è un [**metodo IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
5.  Rilasciare tutte le risorse. Chiamare [**CoTaskMemFree per rilasciare**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) le stringhe di trigger e **ITask::Release** per rilasciare [**l'interfaccia ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) Si noti che [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un [**metodo IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da **ITask.**



| Per un esempio di codice di                                                         | Vedere                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Recupero di una stringa di trigger per tutti i trigger associati a un'attività nota | [Esempio di codice: recupero di stringhe di trigger](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 