---
title: Esempi di recupero di proprietà degli elementi di lavoro
description: Per recuperare le proprietà di un elemento di lavoro, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per recuperare la proprietà dell'attività a cui si è interessati.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- recupero delle proprietà degli elementi di lavoro Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3519f3f995e4a5c49a58f0c8be590b34a82381bfd534b61bac6ff8aba05de33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059979"
---
# <a name="retrieving-work-item-property-examples"></a>Esempi di recupero di proprietà degli elementi di lavoro

Per recuperare le proprietà di un elemento di lavoro, chiamare [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per recuperare la proprietà dell'attività a cui si è interessati. Attualmente, gli unici elementi di lavoro validi sono le attività.

Gli esempi di codice elencati nella parte inferiore di questa pagina illustrano come recuperare le proprietà che si applicano a tutti gli elementi di lavoro. Per altre proprietà specifiche delle attività, vedere Impostazione [di esempi di proprietà delle attività.](setting-task-property-examples.md)

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate quando non sono più necessarie.

 

Si noti che se si recupera una proprietà stringa, ad esempio un commento per un elemento di lavoro, è necessario chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.

Nella procedura seguente viene descritto come recuperare una proprietà dell'attività.

**Per recuperare una proprietà dell'attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un Utilità di pianificazione oggetto . Questi esempi presuppongono che il Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler::Activate per**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) ottenere [**l'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che le attività sono attualmente l'unico tipo di elemento di lavoro valido.
3.  Chiamare il metodo appropriato per recuperare la proprietà a cui si è interessati.
4.  Elaborare la proprietà in base alle esigenze. Questi esempi stampano semplicemente la proprietà sullo schermo.
5.  Se la proprietà restituita è una stringa, chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.



| Per un esempio di codice di                                                                        | Vedere                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Recupero delle informazioni sull'account di un'attività nota                                           | [Esempio di codice C/C++: recupero di informazioni sull'account attività](c-c-code-example-retrieving-task-account-information.md)       |
| Recupero della stringa di commento di un'attività nota                                                | [Esempio di codice C/C++: recupero di un commento di attività](c-c-code-example-retrieving-a-task-comment.md)                           |
| Recupero del nome dell'autore dell'attività e visualizzazione sullo schermo               | [Esempio di codice C/C++: recupero del creatore di attività](c-c-code-example-retrieving-the-task-creator.md)                       |
| Recupero dell'ultimo codice di uscita restituito da un'attività nota                                       | [Esempio di codice C/C++: recupero del codice di uscita dell'attività](c-c-code-example-retrieving-task-exit-code.md)                           |
| Recupero del tempo di inattività dell'attività e visualizzazione sullo schermo                    | [Esempio di codice C/C++: recupero del tempo di inattività/attesa dell'attività](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Recupero dell'ora dell'ultima esecuzione dell'attività e visualizzazione sullo schermo                    | [Esempio di codice C/C++: recupero dell'attività MostRecentRun Time](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Recupero alla successiva esecuzione pianificata dell'attività e visualizzazione dell'ora sullo schermo | [Esempio di codice C/C++: recupero dell'attività NextRun Time](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Recupero dei tempi di esecuzione dell'attività e visualizzazione sullo schermo                       | [Esempio di codice C/C++: recupero dei tempi di esecuzione delle attività](c-c-code-example-retrieving-task-run-times.md)                           |
| Recupero dello stato corrente dell'attività e visualizzazione sullo schermo                    | [Esempio di codice C/C++: recupero dello stato dell'attività](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 