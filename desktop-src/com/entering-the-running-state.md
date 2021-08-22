---
title: Immissione dello stato di esecuzione
description: Immissione dello stato di esecuzione
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91261df578697afef0e33dd8c8ea847eb50cfd546dd96ee0a0085d67100bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501061"
---
# <a name="entering-the-running-state"></a>Immissione dello stato di esecuzione

Quando un oggetto incorporato esegue la transizione allo stato in esecuzione, il gestore dell'oggetto deve individuare ed eseguire l'applicazione server per utilizzare i servizi forniti solo dal server. Gli oggetti incorporati vengono inseriti nello stato di esecuzione in modo esplicito tramite una richiesta del contenitore, ad esempio la necessità di disegnare un formato non attualmente memorizzato nella cache o in modo implicito da OLE in risposta alla chiamata di un'operazione, ad esempio quando un utente del contenitore fa doppio clic sull'oggetto.

Quando un oggetto collegato esegue la transizione allo stato in esecuzione, il processo è noto come *associazione*. Durante il processo di associazione, il gestore di oggetti chiede al moniker archiviato di individuare i dati del collegamento, quindi esegue l'applicazione server.

A prima vista, l'associazione di un oggetto collegato non risulta più complessa rispetto all'esecuzione di un oggetto incorporato. Tuttavia, i punti seguenti complicano il processo:

-   Un collegamento può fare riferimento a un oggetto o a una parte di tale oggetto incorporata in un altro contenitore. Questa funzionalità implica una potenziale incorporamento annidato. La risoluzione dei riferimenti a una gerarchia di questo tipo richiede l'attraversamento ricorsivo di un *moniker* composito, a partire dal membro più a destra.
-   Quando l'origine del collegamento è in esecuzione, OLE viene associato all'istanza in esecuzione dell'oggetto anziché a un'altra istanza. Nel caso di oggetti incorporati annidati, uno dei quali è l'origine del collegamento, OLE deve essere in grado di eseguire l'associazione a un oggetto già in esecuzione in qualsiasi momento.
-   L'esecuzione di un oggetto richiede l'accesso all'area di archiviazione per l'oggetto. Quando viene eseguito un oggetto incorporato, OLE riceve un puntatore all'archiviazione durante il processo di caricamento, che passa all'applicazione server OLE. Per gli oggetti collegati, tuttavia, non esiste un'interfaccia standard per l'accesso all'archiviazione. L'applicazione server OLE può usare l'interfaccia file system o un altro meccanismo.

 

 




