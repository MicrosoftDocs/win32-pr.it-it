---
title: Esempi di recupero di proprietà di attività
description: Per recuperare le proprietà di un'attività, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il Metodo ITask appropriato per recuperare la proprietà dell'attività a cui si è interessati.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recupero delle proprietà dell'attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338694"
---
# <a name="retrieving-task-property-examples"></a>Esempi di recupero di proprietà di attività

Per recuperare le proprietà di un'attività, chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per recuperare la proprietà dell'attività a cui si è interessati. Gli esempi di codice elencati nella parte inferiore della pagina mostrano come recuperare le diverse proprietà dell'attività.

Gli esempi di codice elencati nella parte inferiore della pagina mostrano come recuperare le proprietà univoche degli oggetti attività. Per altre proprietà dell' [*elemento di lavoro*](w.md) che si applicano anche alle attività, vedere recupero degli esempi di [elementi di lavoro](retrieving-work-item-property-examples.md).

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Si noti che se si sta recuperando una proprietà di stringa, ad esempio il nome dell'applicazione, i parametri o la directory di lavoro, è necessario chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.

Nella procedura riportata di seguito viene descritto come recuperare una proprietà di attività.

**Per recuperare una proprietà di attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio Mostra come ottenere l'attività di test.
3.  Chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per recuperare la proprietà a cui si è interessati.
4.  Elaborare la proprietà in base alle esigenze. In questi esempi la proprietà viene stampata sullo schermo.
5.  Se la proprietà restituita è una stringa, chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.



| Per un esempio di codice di                                                                                                                           | Vedere                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Recupero del nome dell'applicazione associata a una determinata attività                                                                             | [Esempio di codice C/C++: recupero del nome dell'applicazione dell'attività](c-c-code-example-retrieving-the-task-application-name.md)   |
| Recupero del tempo massimo di esecuzione dell'attività e visualizzazione di tale numero sullo schermo                                                 | [Esempio di codice C/C++: recupero dell'attività MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Recupero della stringa di parametro eseguita durante l'esecuzione dell'attività e visualizzazione della stringa sullo schermo                                  | [Esempio di codice C/C++: recupero dei parametri delle attività](c-c-code-example-retrieving-task-parameters.md)                       |
| Recupero del [*livello di priorità*](p.md) dell'attività                                                                    | [Esempio di codice C/C++: recupero della priorità dell'attività](c-c-code-example-retrieving-task-priority.md)                           |
| Recupero della [*directory di lavoro*](w.md) di un'attività e visualizzazione del percorso della directory di lavoro sullo schermo | [Esempio di codice C/C++: recupero della directory di lavoro dell'attività](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 