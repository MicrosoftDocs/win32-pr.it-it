---
title: Esempi di proprietà di attività di impostazione
description: Per impostare le proprietà di un'attività, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo ITask appropriato per impostare la proprietà dell'attività a cui si è interessati.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- impostazione delle proprietà delle attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deac57ac28a16108eb886cc56cf697cd768ca7d2e351c4517728c2972be8582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681631"
---
# <a name="setting-task-property-examples"></a>Esempi di proprietà di attività di impostazione

Per impostare le proprietà di un'attività, chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per impostare la proprietà dell'attività a cui si è interessati.

Gli esempi di codice elencati nella parte inferiore della pagina illustrano come impostare le proprietà univoche per gli oggetti attività. Per altre [*proprietà degli elementi di*](w.md) lavoro che si applicano anche alle attività, vedere Impostazione di esempi di proprietà degli elementi di [lavoro](setting-work-item-property-examples.md).

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Negli esempi seguenti l'oggetto attività modificato viene sempre salvato su disco da una chiamata a [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). [**L'interfaccia IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia COM standard ereditata dall'oggetto attività.

La procedura seguente descrive come impostare una proprietà dell'attività.

**Per impostare una proprietà dell'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questi esempi presuppongono che il Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che in questo esempio viene recuperata l'attività "Test Task".
3.  Chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per impostare la proprietà a cui si è interessati.
4.  Chiamare [**IPersistFile::Save per**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) archiviare l'oggetto attività modificato su disco.



| Per un esempio di codice di                                                                                                                                | Vedere                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Impostazione del nome dell'applicazione associata a un'attività nota                                                                                     | [Esempio di codice C/C++: impostazione del nome dell'applicazione](c-c-code-example-setting-application-name.md)   |
| Impostazione del tempo di esecuzione massimo di un'attività nota                                                                                                         | [Esempio di codice C/C++: Impostazione di MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Cancellazione di tutti i parametri della riga di comando associati a un'attività nota                                                                                    | [Esempio di codice C/C++: impostazione dei parametri dell'attività](c-c-code-example-setting-task-parameters.md)     |
| Questo esempio imposta la priorità di un'attività di test e quindi salva l'attività. In questo esempio si presuppone che l'attività di test esista già nel computer locale. | [Esempio di codice C/C++: Impostazione della priorità delle attività](c-c-code-example-setting-task-priority.md)         |
| Impostazione della [*directory di lavoro*](w.md) di un'attività nota                                                                  | [Esempio di codice C/C++: impostazione della directory di lavoro](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 