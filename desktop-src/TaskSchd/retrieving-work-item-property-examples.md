---
title: Recupero degli esempi di proprietà degli elementi di lavoro
description: Per recuperare le proprietà di un elemento di lavoro, chiamare ITaskScheduler Activate per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per recuperare la proprietà dell'attività a cui si è interessati.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- recupero delle proprietà degli elementi di lavoro Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399299"
---
# <a name="retrieving-work-item-property-examples"></a>Recupero degli esempi di proprietà degli elementi di lavoro

Per recuperare le proprietà di un elemento di lavoro, chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per recuperare l'interfaccia dell'oggetto elemento di lavoro, quindi chiamare il metodo appropriato per recuperare la proprietà dell'attività a cui si è interessati. Attualmente, gli unici elementi di lavoro validi sono attività.

Gli esempi di codice elencati nella parte inferiore di questa pagina illustrano come recuperare le proprietà che si applicano a tutti gli elementi di lavoro. Per altre proprietà univoche per le attività, vedere [impostazione degli esempi di proprietà delle attività](setting-task-property-examples.md).

> [!Note]  
> Nell'esempio di codice seguente tutte le interfacce vengono rilasciate dopo che non sono più necessarie.

 

Si noti che se si sta recuperando una proprietà di stringa, ad esempio un commento per un elemento di lavoro, è necessario chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.

Nella procedura riportata di seguito viene descritto come recuperare una proprietà di attività.

**Per recuperare una proprietà di attività**

1.  Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) per inizializzare la libreria com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per ottenere un oggetto utilità di pianificazione. In questi esempi si presuppone che il servizio Utilità di pianificazione sia in esecuzione.
2.  Chiamare [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) per ottenere l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) dell'oggetto attività. Si noti che le attività sono attualmente l'unico tipo di elemento di lavoro valido.
3.  Chiamare il metodo appropriato per recuperare la proprietà a cui si è interessati.
4.  Elaborare la proprietà in base alle esigenze. In questi esempi la proprietà viene semplicemente stampata nella schermata.
5.  Se la proprietà restituita è una stringa, chiamare [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare la memoria allocata per la stringa restituita.



| Per un esempio di codice di                                                                        | Vedere                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Recupero delle informazioni sull'account di un'attività nota                                           | [Esempio di codice C/C++: recupero delle informazioni sull'account attività](c-c-code-example-retrieving-task-account-information.md)       |
| Recupero della stringa di commento di un'attività nota                                                | [Esempio di codice C/C++: recupero di un commento di attività](c-c-code-example-retrieving-a-task-comment.md)                           |
| Recupero del nome dell'autore dell'attività e visualizzazione dello schermo               | [Esempio di codice C/C++: recupero dell'autore dell'attività](c-c-code-example-retrieving-the-task-creator.md)                       |
| Recupero dell'ultimo codice di uscita restituito da un'attività nota                                       | [Esempio di codice C/C++: recupero del codice di uscita dell'attività](c-c-code-example-retrieving-task-exit-code.md)                           |
| Recupero del tempo di attesa di inattività dell'attività e visualizzazione dello schermo                    | [Esempio di codice C/C++: recupero del tempo di inattività del tempo di attesa](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Recupero dell'ora dell'ultima esecuzione dell'attività e visualizzazione dello schermo                    | [Esempio di codice C/C++: recupero del tempo di MostRecentRun dell'attività](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Recupero alla successiva esecuzione pianificata dell'attività e visualizzazione dell'ora sullo schermo | [Esempio di codice C/C++: recupero del tempo di NextRun dell'attività](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Recupero dei tempi di esecuzione dell'attività e visualizzazione dello schermo                       | [Esempio di codice C/C++: recupero dei tempi di esecuzione delle attività](c-c-code-example-retrieving-task-run-times.md)                           |
| Recupero dello stato corrente dell'attività e visualizzazione sullo schermo                    | [Esempio di codice C/C++: recupero dello stato dell'attività](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 