---
title: Elementi di lavoro pianificati
description: Il Utilità di pianificazione usa due termini per descrivere cosa può pianificare gli elementi di lavoro e le attività.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- elementi di lavoro Utilità di pianificazione
- elementi di lavoro Utilità di pianificazione , rispetto alle attività
- attività Utilità di pianificazione
- attività Utilità di pianificazione , rispetto agli elementi di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19455b6d1402439403629aa5f6fca81621571fc90d9e6d8b204e741c5129414
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080431"
---
# <a name="scheduled-work-items"></a>Elementi di lavoro pianificati

Il Utilità di pianificazione usa due termini per descrivere cosa può pianificare: elementi di lavoro e attività. Di questi due termini, [*l'elemento di*](w.md) lavoro è un termine più generale che descrive qualsiasi tipo di elemento che può essere pianificato. Un *elemento di* lavoro può essere qualsiasi elemento eseguito dal Utilità di pianificazione in un momento specificato dai trigger dell'elemento.

Al contrario, [*un'attività*](t.md) è un tipo specifico di elemento di lavoro. Attualmente, l'unico tipo di elemento di lavoro pianificato supportato è un'attività.

[**L'interfaccia IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contiene metodi supportati da tutti i tipi di elementi di lavoro pianificati. Ad esempio, le informazioni sull'account, i tempi di esecuzione e i commenti definiti dall'applicazione sono proprietà che possono essere applicate a tutti i tipi di elementi di lavoro. Queste proprietà possono essere impostate e recuperate tramite **l'interfaccia IScheduledWorkItem.**

[**L'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contiene metodi supportati solo dalle attività.

I metodi [**dell'interfaccia IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) sono attualmente ereditati [**dall'interfaccia ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) e in futuro verranno ereditati da altre interfacce dell'elemento di lavoro.

| Per esempi di                                              | Vedere                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Creazione di una nuova attività.                                         | [Esempio di creazione di un'attività con NewWorkItem](creating-a-task-using-newworkitem-example.md) |
| Esecuzione di un'attività esistente.                                    | [Avvio di un esempio di attività](starting-a-task-example.md)                                     |
| Recupero di proprietà che si applicano a tutti i tipi di elementi di lavoro. | [Esempi di proprietà degli elementi di lavoro](retrieving-work-item-property-examples.md)       |
| Impostazione delle proprietà che si applicano a tutti i tipi di elementi di lavoro.    | [Esempi di proprietà dell'elemento di lavoro](setting-work-item-property-examples.md)             |



 

 

 




