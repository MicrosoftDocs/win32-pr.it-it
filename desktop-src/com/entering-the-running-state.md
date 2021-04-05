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
# <a name="entering-the-running-state"></a><span data-ttu-id="6bed0-103">Immissione dello stato in esecuzione</span><span class="sxs-lookup"><span data-stu-id="6bed0-103">Entering the Running State</span></span>

<span data-ttu-id="6bed0-104">Quando un oggetto incorporato esegue la transizione allo stato di esecuzione, il gestore di oggetti deve individuare ed eseguire l'applicazione server per poter utilizzare i servizi forniti solo dal server.</span><span class="sxs-lookup"><span data-stu-id="6bed0-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="6bed0-105">Gli oggetti incorporati vengono inseriti nello stato in esecuzione in modo esplicito tramite una richiesta da parte del contenitore, ad esempio la necessità di creare un formato non attualmente memorizzato nella cache o in modo implicito da OLE in risposta alla chiamata di un'operazione, ad esempio quando un utente del contenitore fa doppio clic sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6bed0-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="6bed0-106">Quando un oggetto collegato esegue la transizione allo stato di esecuzione, il processo è noto come *Binding*.</span><span class="sxs-lookup"><span data-stu-id="6bed0-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="6bed0-107">Nel processo di associazione, il gestore dell'oggetto chiede al moniker archiviato di individuare i dati del collegamento, quindi esegue l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="6bed0-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="6bed0-108">A prima vista, l'associazione di un oggetto collegato sembra non essere più complicata rispetto all'esecuzione di un oggetto incorporato.</span><span class="sxs-lookup"><span data-stu-id="6bed0-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="6bed0-109">Tuttavia, i punti seguenti complicano il processo:</span><span class="sxs-lookup"><span data-stu-id="6bed0-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="6bed0-110">Un collegamento può fare riferimento a un oggetto o a una parte di esso incorporato in un altro contenitore.</span><span class="sxs-lookup"><span data-stu-id="6bed0-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="6bed0-111">Questa funzionalità implica una potenziale presenza di incorporamenti annidati.</span><span class="sxs-lookup"><span data-stu-id="6bed0-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="6bed0-112">La risoluzione dei riferimenti a tale gerarchia richiede l'attraversamento ricorsivo di un *moniker composito*, a partire dal membro più a destra.</span><span class="sxs-lookup"><span data-stu-id="6bed0-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="6bed0-113">Quando l'origine del collegamento è in esecuzione, OLE esegue l'associazione all'istanza in esecuzione dell'oggetto anziché eseguire un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="6bed0-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="6bed0-114">Nel caso di oggetti incorporati annidati, uno dei quali è l'origine del collegamento, OLE deve essere in grado di eseguire il binding a un oggetto già in esecuzione in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="6bed0-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="6bed0-115">L'esecuzione di un oggetto richiede l'accesso all'area di archiviazione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6bed0-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="6bed0-116">Quando viene eseguito un oggetto incorporato, OLE riceve un puntatore all'archiviazione durante il processo di caricamento, che viene passato all'applicazione server OLE.</span><span class="sxs-lookup"><span data-stu-id="6bed0-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="6bed0-117">Per gli oggetti collegati, tuttavia, non esiste alcuna interfaccia standard per accedere all'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6bed0-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="6bed0-118">L'applicazione server OLE può utilizzare l'interfaccia file system o un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="6bed0-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




