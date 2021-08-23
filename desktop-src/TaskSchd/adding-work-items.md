---
title: Aggiunta di elementi di lavoro
description: Esistono due modi per aggiungere elementi di lavoro alla cartella Attività pianificate. È possibile creare un nuovo elemento di lavoro all'interno della cartella oppure aggiungere un elemento di lavoro esistente alla cartella.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- elementi di lavoro Utilità di pianificazione , aggiunta
- attività Utilità di pianificazione , aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc964b620a01b0f1114240dcb11f275fa8faffc37e8264d8854cb60191628943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621161"
---
# <a name="adding-work-items"></a>Aggiunta di elementi di lavoro

Esistono due modi per aggiungere [*elementi di lavoro*](w.md) alla cartella Attività [*pianificate*](s.md). È possibile creare un nuovo elemento di lavoro all'interno della cartella oppure aggiungere un elemento di lavoro esistente alla cartella.

> [!Note]  
> Attualmente, solo gli oggetti attività possono essere aggiunti alla cartella Attività pianificate. Quando si aggiunge un'attività, è necessario conoscere gli identificatori per la classe di attività e l'interfaccia dell'attività [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Per creare nuovi elementi di lavoro, chiamare il [**metodo ITaskScheduler::NewWorkItem.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) Questo metodo crea un nuovo oggetto elemento di lavoro usando il nome specificato e aggiunge l'elemento di lavoro alla cartella Attività pianificate. Quando si crea un nuovo elemento di lavoro, Utilità di pianificazione alloca la memoria necessaria per il nuovo oggetto.

Per aggiungere elementi di lavoro esistenti alla cartella Attività pianificate, chiamare il [**metodo ITaskScheduler::AddWorkItem.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) Quando si chiama questo metodo, è necessario creare l'oggetto .

I nomi specificati per gli elementi di lavoro devono essere univoci all'interno della cartella Attività pianificate. Se un elemento di lavoro con lo stesso nome esiste già quando si chiama il metodo [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) o il metodo [**ITaskScheduler::AddWorkItem,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) il metodo restituisce un errore **ERROR FILE \_ \_ EXISTS.** Per altre informazioni, vedere [Creazione di un'attività con l'esempio NewWorkItem](creating-a-task-using-newworkitem-example.md).

 

 




