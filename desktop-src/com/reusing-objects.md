---
title: Riutilizzo di oggetti
description: Riutilizzo di oggetti
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b6ef6d28b23ff2fcda5ed46d9b99a6634389793e48275c36e2f8a708f7266d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309422"
---
# <a name="reusing-objects"></a>Riutilizzo di oggetti

Un obiettivo importante di qualsiasi modello a oggetti è consentire agli autori di oggetti di riutilizzare ed estendere gli oggetti forniti da altri come parti delle proprie implementazioni. Un modo per eseguire questa operazione in Microsoft Visual C++ e in altri linguaggi è usare l'ereditarietà dell'implementazione *,* che consente a un oggetto di ereditare ("sottoclasse") alcune delle funzioni da un altro oggetto durante l'override di altre funzioni.

Il problema dell'interazione tra oggetti a livello di sistema che usa l'ereditarietà dell'implementazione tradizionale è che il contratto (l'interfaccia) tra gli oggetti in una gerarchia di implementazione non è chiaramente definito. In realtà, è implicito e ambiguo. Quando l'oggetto padre o figlio modifica l'implementazione, il comportamento dei componenti correlati potrebbe diventare indefinito o non implementato in modo indefinito. In qualsiasi singola applicazione, in cui l'implementazione può essere gestita da un singolo team di progettazione che aggiorna tutti i componenti contemporaneamente, questo non è sempre un problema importante. In un ambiente in cui i componenti di un team vengono compilati tramite il riutilizzo black box di altri componenti creati da altri team, questo tipo di instabilità compromette il riutilizzo. Inoltre, l'ereditarietà dell'implementazione funziona in genere solo entro i limiti del processo. In questo modo l'ereditarietà dell'implementazione tradizionale non è pratica per sistemi di grandi dimensioni in evoluzione costituiti da componenti software creati da molti team di progettazione.

La chiave per la compilazione di componenti riutilizzabili è la possibilità di considerare l'oggetto come una casella opaca. Ciò significa che la parte di codice che tenta di riutilizzare un altro oggetto non conosce e non deve sapere nulla sulla struttura interna o sull'implementazione del componente in uso. In altre parole, il codice che tenta di riutilizzare un componente dipende dal comportamento dell'oggetto e non dall'implementazione esatta.

Per ottenere la riutilizzabilità black box, COM adotta altri meccanismi di riutilizzo stabiliti, ad esempio *contenimento/delega* e *aggregazione.*

> [!NOTE]  
> Per praticità, l'oggetto riutilizzato viene chiamato oggetto interno e l'oggetto che usa tale oggetto interno è l'oggetto *esterno*. 

 

È importante ricordare in entrambi questi meccanismi l'aspetto dell'oggetto esterno ai client. Per quanto riguarda i client, entrambi gli oggetti implementano qualsiasi interfaccia a cui il client può ottenere un puntatore. Il client considera l'oggetto esterno come una casella opaca e pertanto non è importante, né deve occuparsi, della struttura interna dell'oggetto esterno". Il client si occupa solo del comportamento.

Per altre informazioni, vedere i seguenti argomenti:

-   [Contenimento/delega](containment-delegation.md)
-   [Aggregazione](aggregation.md)

 

 




