---
title: Aggiunta di elementi di lavoro
description: Esistono due modi per aggiungere elementi di lavoro alla TasksFolder pianificata. È possibile creare un nuovo elemento di lavoro all'interno della cartella oppure è possibile aggiungere un elemento di lavoro esistente alla cartella.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- elementi di lavoro Utilità di pianificazione, aggiunta
- attività Utilità di pianificazione, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298479"
---
# <a name="adding-work-items"></a>Aggiunta di elementi di lavoro

Esistono due modi per aggiungere [*elementi di lavoro*](w.md) alla [*TasksFolder pianificata*](s.md). È possibile creare un nuovo elemento di lavoro all'interno della cartella oppure è possibile aggiungere un elemento di lavoro esistente alla cartella.

> [!Note]  
> Attualmente, solo gli oggetti attività possono essere aggiunti alla cartella attività pianificate. Quando si aggiunge un'attività, è necessario conoscerne gli identificatori per la classe dell'attività e l'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Per creare nuovi elementi di lavoro, chiamare il metodo [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) . Questo metodo crea un nuovo oggetto elemento di lavoro usando il nome fornito e aggiunge l'elemento di lavoro alla cartella delle attività pianificate. Quando si crea un nuovo elemento di lavoro, il Utilità di pianificazione alloca la memoria necessaria per il nuovo oggetto.

Per aggiungere elementi di lavoro esistenti alla cartella delle attività pianificate, chiamare il metodo [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) . Quando si chiama questo metodo, è necessario creare l'oggetto.

I nomi forniti per gli elementi di lavoro devono essere univoci all'interno della cartella attività pianificate. Se un elemento di lavoro con lo stesso nome esiste già quando si chiama il metodo [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) o [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , il metodo restituisce un errore relativo al **file di errore \_ \_ esistente** . Per altre informazioni, vedere [creazione di un'attività con l'esempio NewWorkItem](creating-a-task-using-newworkitem-example.md).

 

 




