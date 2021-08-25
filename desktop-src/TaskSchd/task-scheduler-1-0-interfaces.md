---
title: Utilità di pianificazione 1.0 Interfaces
description: Le interfacce descritte negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione usato nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2033c78594c0f4ef1d9f871275f425ef5189240ed7b432266464343cf86e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975031"
---
# <a name="task-scheduler-10-interfaces"></a>Utilità di pianificazione 1.0 Interfaces

\[\[Questa API può essere modificata o non disponibile nelle versioni successive del sistema operativo o del prodotto. Usare invece le [Utilità di pianificazione 2.0 o](task-scheduler-2-0-interfaces.md) Utilità di pianificazione tipi enumerati [2.0.](task-scheduler-2-0-enumerated-types.md) \]\]

Le interfacce descritte negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione usato nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.

Questi argomenti contengono una descrizione dell'interfaccia, un elenco delle proprietà e dei metodi definiti dall'interfaccia e commenti su eventuali circostanze speciali che devono essere notate quando si usa l'interfaccia .


Le interfacce seguenti sono state introdotte da Utilità di pianificazione 1.0.



| Interfaccia                                        | Descrizione                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Fornisce i metodi per enumerare le attività nella [*cartella Attività pianificate*](s.md).                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Fornisce i metodi per accedere alle impostazioni della finestra delle proprietà di un'attività.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Fornisce i metodi per la gestione di elementi [*di lavoro specifici.*](w.md)                                                                                                                                                 |
| [**Itask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Fornisce i metodi per l'esecuzione di attività, il recupero o l'impostazione delle informazioni sulle attività e la terminazione delle attività. Deriva [**dall'interfaccia IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ed eredita tutti i metodi di tale interfaccia. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Fornisce i metodi per la pianificazione delle attività.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Fornisce i metodi per accedere e impostare i trigger per un'attività. I trigger specificano le ore di inizio dell'attività, i criteri di ripetizione e altri parametri che controllano quando viene eseguita un'attività.                                                     |



 

 

 




