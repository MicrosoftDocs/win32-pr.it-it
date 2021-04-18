---
title: Esempi di impostazione delle proprietà delle attività
description: Per impostare le proprietà di un'attività, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il Metodo ITask appropriato per impostare la proprietà dell'attività a cui si è interessati.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- impostazione delle proprietà dell'attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300144"
---
# <a name="setting-task-property-examples"></a>Esempi di impostazione delle proprietà delle attività

Per impostare le proprietà di un'attività, chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per impostare la proprietà dell'attività a cui si è interessati.

Gli esempi di codice elencati nella parte inferiore della pagina illustrano come impostare le proprietà univoche per gli oggetti attività. Per altre proprietà dell' [*elemento di lavoro*](w.md) che si applicano anche alle attività, vedere Impostazione degli esempi di proprietà degli [elementi di lavoro](setting-work-item-property-examples.md).

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Negli esempi seguenti, l'oggetto attività modificato viene sempre salvato su disco mediante una chiamata a [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard ereditata dall'oggetto attività).

Nella procedura riportata di seguito viene descritto come impostare una proprietà dell'attività.

**Per impostare una proprietà dell'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per impostare la proprietà a cui si è interessati.
4.  Chiamare [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per archiviare l'oggetto attività modificato su disco.



| Per un esempio di codice di                                                                                                                                | Vedere                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Impostazione del nome dell'applicazione associata a un'attività nota                                                                                     | [Esempio di codice C/C++: impostazione del nome dell'applicazione](c-c-code-example-setting-application-name.md)   |
| Impostazione del tempo di esecuzione massimo di un'attività nota                                                                                                         | [Esempio di codice C/C++: impostazione di MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Cancellazione di tutti i parametri della riga di comando associati a un'attività nota                                                                                    | [Esempio di codice C/C++: impostazione dei parametri delle attività](c-c-code-example-setting-task-parameters.md)     |
| In questo esempio viene impostata la priorità di un'attività di test e quindi viene salvata l'attività. In questo esempio si presuppone che l'attività di test esista già nel computer locale. | [Esempio di codice C/C++: impostazione della priorità delle attività](c-c-code-example-setting-task-priority.md)         |
| Impostazione della [*directory di lavoro*](w.md) di un'attività nota                                                                  | [Esempio di codice C/C++: impostazione della directory di lavoro](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 