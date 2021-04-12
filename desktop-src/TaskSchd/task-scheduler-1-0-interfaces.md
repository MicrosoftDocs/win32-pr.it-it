---
title: Interfacce di Utilità di pianificazione 1,0
description: Le interfacce descritte negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione usato nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104224576"
---
# <a name="task-scheduler-10-interfaces"></a>Interfacce di Utilità di pianificazione 1,0

\[\[Questa API può essere modificata o non disponibile nelle versioni successive del sistema operativo o del prodotto. Usare invece le [interfacce Utilità di pianificazione 2,0](task-scheduler-2-0-interfaces.md) o [utilità di pianificazione 2,0 tipi enumerati](task-scheduler-2-0-enumerated-types.md) . \]\]

Le interfacce descritte negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione usato nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.

Questi argomenti contengono una descrizione dell'interfaccia, un elenco delle proprietà e dei metodi definiti dall'interfaccia e commenti sulle circostanze speciali che devono essere annotate quando si usa l'interfaccia.


Le interfacce seguenti sono introdotte da Utilità di pianificazione 1,0.



| Interfaccia                                        | Descrizione                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Fornisce i metodi per enumerare le attività nella [*cartella delle attività pianificate*](s.md).                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Fornisce i metodi per accedere alle impostazioni della finestra delle proprietà di un'attività.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Fornisce i metodi per la gestione di [*elementi di lavoro*](w.md)specifici.                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Fornisce i metodi per eseguire attività, ottenere o impostare informazioni sulle attività e terminare le attività. Viene derivato dall'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ed eredita tutti i metodi di tale interfaccia. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Fornisce i metodi per la pianificazione delle attività.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Fornisce i metodi per accedere ai trigger e impostarli per un'attività. I trigger specificano l'ora di inizio, i criteri di ripetizione e altri parametri di attività che controllano quando viene eseguita un'attività.                                                     |



 

 

 




