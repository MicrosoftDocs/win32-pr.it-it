---
title: Esempi di proprietà attività di recupero
description: Per recuperare le proprietà di un'attività, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo ITask appropriato per recuperare la proprietà dell'attività a cui si è interessati.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recupero delle proprietà dell'attività Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e46554c32d9d30941fd837b91e80e8e20d915b0f1c68a665fd72c8f1624c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002389"
---
# <a name="retrieving-task-property-examples"></a>Esempi di proprietà attività di recupero

Per recuperare le proprietà di un'attività, chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto attività, quindi chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per recuperare la proprietà dell'attività a cui si è interessati. Gli esempi di codice elencati nella parte inferiore della pagina illustrano come recuperare le diverse proprietà dell'attività.

Gli esempi di codice elencati nella parte inferiore della pagina illustrano come recuperare le proprietà univoche per gli oggetti attività. Per altre [*proprietà degli elementi*](w.md) di lavoro che si applicano anche alle attività, vedere Recupero di esempi di elementi di [lavoro](retrieving-work-item-property-examples.md).

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Si noti che se si recupera una proprietà stringa, ad esempio il nome dell'applicazione, i parametri o la directory di lavoro, è necessario chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.

La procedura seguente descrive come recuperare una proprietà dell'attività.

**Per recuperare una proprietà dell'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questi esempi presuppongono che il Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che questo esempio ottiene l'attività "Test Task".
3.  Chiamare il metodo [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriato per recuperare la proprietà a cui si è interessati.
4.  Elaborare la proprietà in base alle esigenze. In questi esempi la proprietà viene stampata sullo schermo.
5.  Se la proprietà restituita è una stringa, chiamare [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.



| Per un esempio di codice di                                                                                                                           | Vedere                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Recupero del nome dell'applicazione associata a una determinata attività                                                                             | [Esempio di codice C/C++: recupero del nome dell'applicazione task](c-c-code-example-retrieving-the-task-application-name.md)   |
| Recupero della quantità massima di tempo per l'esecuzione dell'attività e visualizzazione di tale numero sullo schermo                                                 | [Esempio di codice C/C++: recupero dell'attività MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Recupero della stringa di parametro eseguita durante l'esecuzione dell'attività e visualizzazione della stringa sullo schermo                                  | [Esempio di codice C/C++: recupero di parametri di attività](c-c-code-example-retrieving-task-parameters.md)                       |
| Recupero del livello [*di priorità dell'attività*](p.md)                                                                    | [Esempio di codice C/C++: recupero della priorità delle attività](c-c-code-example-retrieving-task-priority.md)                           |
| Recupero della [*directory di lavoro di*](w.md) un'attività e visualizzazione del percorso della directory di lavoro sullo schermo | [Esempio di codice C/C++: recupero della directory di lavoro delle attività](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 