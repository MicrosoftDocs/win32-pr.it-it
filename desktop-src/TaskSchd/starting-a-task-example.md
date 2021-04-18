---
title: Avvio di un esempio di attività
description: Per avviare un'attività, chiamare il metodo Run dell'interfaccia ITask. Run è un metodo asincrono che tenta di eseguire l'attività e viene restituito non appena l'attività è stata avviata. Per la riuscita di questo metodo, è necessario che il servizio Utilità di pianificazione sia in esecuzione.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300201"
---
# <a name="starting-a-task-example"></a>Avvio di un esempio di attività

Per avviare un'attività, chiamare il metodo [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) dell'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . **Run** è un metodo asincrono che tenta di eseguire l'attività e viene restituito non appena l'attività è stata avviata. Per la riuscita di questo metodo, è necessario che il servizio Utilità di pianificazione sia in esecuzione.

Nella procedura riportata di seguito viene descritto come avviare un'attività.

**Per avviare un'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questo esempio si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) per avviare l'attività. Si noti che questo metodo viene ereditato dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Continuare l'elaborazione in base alle esigenze.
5.  Chiamare **ITask:: Release** per liberare risorse e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione di com. In questo esempio viene chiamata la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per liberare il puntatore all'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . Si noti che la **versione** è un metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da **ITask**.



| Per un esempio di codice di    | Vedere                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Esecuzione di un'attività esistente | [Esempio di codice C/C++: avvio di un'attività](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 