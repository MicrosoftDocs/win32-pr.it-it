---
title: Manipolazione degli elementi di lavoro
description: L'interfaccia IScheduledWorkItem fornisce metodi per il recupero e l'impostazione delle proprietà degli elementi di lavoro. creazione, recupero ed eliminazione di trigger per gli elementi di lavoro (l'impostazione del trigger deve essere eseguita con il metodo setrigger ITaskTrigger); e per l'esecuzione, la terminazione e l'eliminazione dell'elemento di lavoro. Nota per le proprietà di un tipo specifico di elemento di lavoro, fare riferimento all'interfaccia per quel tipo di oggetto. Ad esempio, non è possibile impostare il livello di priorità di un elemento di lavoro; Tuttavia, è possibile utilizzare i metodi dell'interfaccia ITask per recuperare e impostare la priorità di un'attività.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- elementi di lavoro Utilità di pianificazione, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728546"
---
# <a name="manipulating-work-items"></a>Manipolazione degli elementi di lavoro

L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce metodi per il recupero e l'impostazione delle proprietà degli elementi di lavoro. creazione, recupero ed eliminazione di trigger per gli elementi di lavoro (l'impostazione del trigger deve essere eseguita con il metodo [**ITaskTrigger:: setrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); e per l'esecuzione, la terminazione e l'eliminazione dell'elemento di lavoro.

> [!Note]  
> Per le proprietà di un tipo specifico di elemento di lavoro, fare riferimento all'interfaccia per quel tipo di oggetto. Ad esempio, non è possibile impostare il livello di priorità di un elemento di lavoro; Tuttavia, è possibile utilizzare i metodi dell'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) per recuperare e impostare la priorità di un'attività.

 

Ogni volta che si modifica un elemento di lavoro, è necessario chiamare l'oggetto [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare l'elemento di lavoro modificato su disco. L'interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) è un'interfaccia com standard supportata dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .

| Per esempi di                                                            | Vedere                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Recupero di proprietà che si applicano a tutti i tipi di elementi di lavoro                | [Recupero degli esempi di proprietà degli elementi di lavoro](retrieving-work-item-property-examples.md) |
| Impostazione delle proprietà che si applicano a tutti i tipi di elementi di lavoro                   | [Impostazione degli esempi di proprietà degli elementi di lavoro](setting-work-item-property-examples.md)       |
| Esecuzione di un'attività nota                                                       | [Avvio di un esempio di attività](starting-a-task-example.md)                               |
| Terminazione di un'attività in esecuzione                                                 | [Chiusura di un esempio di attività](terminating-a-task-example.md)                         |
| Creazione di un nuovo trigger per un'attività nota                                    | [Creazione di un nuovo trigger](creating-a-new-trigger.md)                                 |
| Creazione di un trigger inattivo basato su eventi per un'attività nota                      | [Esempio di creazione di un trigger inattivo](creating-an-idle-trigger-example.md)             |
| Recupero della stringa di trigger di tutti i trigger associati a un'attività nota | [Esempio di recupero di stringhe di trigger](retrieving-trigger-strings-example.md)         |



 

 

 