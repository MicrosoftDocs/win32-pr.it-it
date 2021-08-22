---
title: Esempio di avvio di un'attività
description: Per avviare un'attività, chiamare il metodo Run dell'interfaccia ITask. Run è un metodo asincrono che tenta di eseguire l'attività e restituisce non appena l'attività è stata avviata. Il Utilità di pianificazione deve essere in esecuzione perché questo metodo riesca.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4176bf793e72acd3930d6e1e5cbc3d73e91c1d558e342a5a9804aa8f87526cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139334"
---
# <a name="starting-a-task-example"></a>Esempio di avvio di un'attività

Per avviare un'attività, chiamare [**il metodo Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) dell'interfaccia [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) **Run** è un metodo asincrono che tenta di eseguire l'attività e restituisce non appena l'attività è stata avviata. Il Utilità di pianificazione deve essere in esecuzione perché questo metodo riesca.

Nella procedura seguente viene descritto come avviare un'attività.

**Per avviare un'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questo esempio presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate per**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che in questo esempio viene recuperata l'attività "Test Task".
3.  Chiamare [**Esegui per**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) avviare l'attività. Si noti che questo metodo viene ereditato [**dall'interfaccia ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Continuare l'elaborazione in base alle esigenze.
5.  Chiamare **ITask::Release per** liberare risorse e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) per annullare l'inizializzazione di COM. Questo esempio chiama [**Release per**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) liberare il puntatore all'interfaccia [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) Si noti che **Release** è un [**metodo IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ereditato da **ITask.**



| Per un esempio di codice di    | Vedere                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Esecuzione di un'attività esistente | [Esempio di codice C/C++: avvio di un'attività](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 