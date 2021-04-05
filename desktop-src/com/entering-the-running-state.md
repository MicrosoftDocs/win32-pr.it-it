---
title: Immissione dello stato in esecuzione
description: Immissione dello stato in esecuzione
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955409"
---
# <a name="entering-the-running-state"></a>Immissione dello stato in esecuzione

Quando un oggetto incorporato esegue la transizione allo stato di esecuzione, il gestore di oggetti deve individuare ed eseguire l'applicazione server per poter utilizzare i servizi forniti solo dal server. Gli oggetti incorporati vengono inseriti nello stato in esecuzione in modo esplicito tramite una richiesta da parte del contenitore, ad esempio la necessità di creare un formato non attualmente memorizzato nella cache o in modo implicito da OLE in risposta alla chiamata di un'operazione, ad esempio quando un utente del contenitore fa doppio clic sull'oggetto.

Quando un oggetto collegato esegue la transizione allo stato di esecuzione, il processo è noto come *Binding*. Nel processo di associazione, il gestore dell'oggetto chiede al moniker archiviato di individuare i dati del collegamento, quindi esegue l'applicazione server.

A prima vista, l'associazione di un oggetto collegato sembra non essere più complicata rispetto all'esecuzione di un oggetto incorporato. Tuttavia, i punti seguenti complicano il processo:

-   Un collegamento può fare riferimento a un oggetto o a una parte di esso incorporato in un altro contenitore. Questa funzionalità implica una potenziale presenza di incorporamenti annidati. La risoluzione dei riferimenti a tale gerarchia richiede l'attraversamento ricorsivo di un *moniker composito*, a partire dal membro più a destra.
-   Quando l'origine del collegamento è in esecuzione, OLE esegue l'associazione all'istanza in esecuzione dell'oggetto anziché eseguire un'altra istanza. Nel caso di oggetti incorporati annidati, uno dei quali è l'origine del collegamento, OLE deve essere in grado di eseguire il binding a un oggetto già in esecuzione in qualsiasi momento.
-   L'esecuzione di un oggetto richiede l'accesso all'area di archiviazione per l'oggetto. Quando viene eseguito un oggetto incorporato, OLE riceve un puntatore all'archiviazione durante il processo di caricamento, che viene passato all'applicazione server OLE. Per gli oggetti collegati, tuttavia, non esiste alcuna interfaccia standard per accedere all'archiviazione. L'applicazione server OLE può utilizzare l'interfaccia file system o un altro meccanismo.

 

 




