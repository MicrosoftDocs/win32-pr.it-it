---
title: Esempio di recupero di stringhe di trigger
description: È possibile recuperare le stringhe di trigger di un trigger noto usando l'interfaccia IScheduledWorkItem o ITaskTrigger, a seconda del tipo di oggetto in uso.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recupero delle stringhe del trigger Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300104"
---
# <a name="retrieving-trigger-strings-example"></a>Esempio di recupero di stringhe di trigger

È possibile recuperare le stringhe di trigger di un trigger noto usando l'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) o [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , a seconda del tipo di oggetto in uso.

Quando si utilizza un [*oggetto attività*](t.md), utilizzare i metodi dell'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) per recuperare le stringhe di trigger di un elemento di lavoro.

Quando si utilizza un [*oggetto trigger di attività*](t.md), utilizzare i metodi dell'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) per recuperare la stringa di trigger del trigger.

Nell'esempio seguente viene illustrato come utilizzare [**IScheduledWorkItem:: GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) per visualizzare le stringhe di tutti i trigger associati a un'attività nota.

Nella procedura riportata di seguito viene descritto come recuperare le stringhe di trigger di un'attività.

**Per recuperare le stringhe di trigger di un'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare **ITask:: GetTriggerCount** per verificare il numero di trigger associati a un'attività. Si noti che [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).
4.  Visualizzare le stringhe del trigger, chiamando **ITask:: GetTriggerString** per ogni trigger associato all'attività. Si noti che [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) è un metodo [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ereditato da [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).
5.  Rilasciare tutte le risorse. Chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per rilasciare le stringhe del trigger e **ITask:: Release** per rilasciare l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . Si noti che la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da **ITask**.



| Per un esempio di codice di                                                         | Vedere                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Recupero di una stringa di trigger per tutti i trigger associati a un'attività nota | [Esempio di codice: recupero di stringhe di trigger](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 