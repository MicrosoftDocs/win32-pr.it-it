---
title: Elementi di lavoro pianificati
description: Il Utilità di pianificazione usa due termini per descrivere ciò che può pianificare gli elementi di lavoro e le attività.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- elementi di lavoro Utilità di pianificazione
- elementi di lavoro Utilità di pianificazione, rispetto alle attività
- Utilità di pianificazione attività
- Utilità di pianificazione attività, rispetto agli elementi di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329327"
---
# <a name="scheduled-work-items"></a>Elementi di lavoro pianificati

Il Utilità di pianificazione usa due termini per descrivere ciò che può pianificare: elementi di lavoro e attività. Di questi due termini, [*elemento di lavoro*](w.md) è un termine più generale che descrive qualsiasi tipo di elemento che è possibile pianificare. Un *elemento di lavoro* può essere qualsiasi elemento eseguito dal servizio Utilità di pianificazione in un momento specificato dal trigger o dai trigger dell'elemento.

Al contrario, un' [*attività*](t.md) è un tipo specifico di elemento di lavoro. Attualmente, l'unico tipo di elemento di lavoro pianificato supportato è un'attività.

L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contiene metodi supportati da tutti i tipi di elementi di lavoro pianificati. Ad esempio, le informazioni sull'account, le esecuzioni e i commenti definiti dall'applicazione sono proprietà che possono essere valide per tutti i tipi di elementi di lavoro. È possibile impostare e recuperare queste proprietà tramite l'interfaccia **IScheduledWorkItem** .

L'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contiene metodi supportati solo dalle attività.

I metodi dell'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) sono attualmente ereditati dall'interfaccia [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) e in futuro verranno ereditati da altre interfacce di elementi di lavoro.

| Per esempi di                                              | Vedere                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Creazione di una nuova attività.                                         | [Esempio di creazione di un'attività con NewWorkItem](creating-a-task-using-newworkitem-example.md) |
| Esecuzione di un'attività esistente.                                    | [Avvio di un esempio di attività](starting-a-task-example.md)                                     |
| Recupero di proprietà che si applicano a tutti i tipi di elementi di lavoro. | [Recupero degli esempi di proprietà degli elementi di lavoro](retrieving-work-item-property-examples.md)       |
| Impostazione delle proprietà che si applicano a tutti i tipi di elementi di lavoro.    | [Impostazione degli esempi di proprietà degli elementi di lavoro](setting-work-item-property-examples.md)             |



 

 

 




