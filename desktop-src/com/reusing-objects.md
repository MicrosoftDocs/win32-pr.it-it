---
title: Riutilizzo di oggetti
description: Riutilizzo di oggetti
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2020
ms.locfileid: "104516696"
---
# <a name="reusing-objects"></a>Riutilizzo di oggetti

Un obiettivo importante di qualsiasi modello a oggetti è quello di consentire agli autori di oggetti di riutilizzare ed estendere gli oggetti forniti da altri come parti delle proprie implementazioni. Un modo per eseguire questa operazione in Microsoft Visual C++ e in altri linguaggi consiste nell'usare l' *ereditarietà dell'implementazione*, che consente a un oggetto di ereditare ("sottoclasse") alcune delle funzioni di un altro oggetto durante l'override di altre funzioni.

Il problema per l'interazione dell'oggetto a livello con l'ereditarietà dell'implementazione tradizionale è che il contratto (l'interfaccia) tra gli oggetti in una gerarchia di implementazione non è chiaramente definito. In realtà, è implicito e ambiguo. Quando l'implementazione dell'oggetto padre o figlio viene modificata, il comportamento dei componenti correlati potrebbe diventare non definito o implementato in modo non stabile. In ogni singola applicazione, in cui l'implementazione può essere gestita da un singolo team di progettazione che Aggiorna contemporaneamente tutti i componenti, questo non è sempre un problema importante. In un ambiente in cui i componenti di un team vengono compilati tramite il riutilizzo della scatola nera di altri componenti creati da altri team, questo tipo di instabilità compromette il riutilizzo. Inoltre, l'ereditarietà dell'implementazione di in genere funziona solo all'interno dei limiti del processo. In questo modo l'ereditarietà tradizionale dell'implementazione non è praticabile per sistemi di grandi dimensioni e in continua evoluzione costituiti da componenti software creati da molti team di progettazione

La chiave per la creazione di componenti riutilizzabili consiste nell'essere in grado di trattare l'oggetto come una casella opaca. Ciò significa che il frammento di codice che tenta di riutilizzare un altro oggetto non conosce nulla e non deve necessariamente conoscere la struttura interna o l'implementazione del componente utilizzato. In altre parole, il codice che tenta di riutilizzare un componente dipende dal comportamento dell'oggetto e non dall'implementazione esatta.

Per ottenere la riusabilità nera, COM adotta altri meccanismi di riusabilità stabiliti, ad esempio *contenimento/delega* e *aggregazione*.

> [!NOTE]  
> Per praticità, l'oggetto da riutilizzare viene chiamato *oggetto interno* e l'oggetto che utilizza tale oggetto interno è l' *oggetto esterno*.

 

È importante ricordare in entrambi i meccanismi il modo in cui l'oggetto esterno appare ai client. Per quanto riguarda i client, entrambi gli oggetti implementano qualsiasi interfaccia a cui il client può ottenere un puntatore. Il client considera l'oggetto esterno come una casella opaca e pertanto non è rilevante, né deve preoccuparsi, sulla struttura interna del objectâ esterno, il client si occupa solo del comportamento.

Per altre informazioni, vedere i seguenti argomenti:

-   [Contenimento/delega](containment-delegation.md)
-   [Aggregazione](aggregation.md)

 

 




