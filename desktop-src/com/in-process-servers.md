---
title: Server In-Process
description: Server In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221390"
---
# <a name="in-process-servers"></a><span data-ttu-id="1155a-103">Server In-Process</span><span class="sxs-lookup"><span data-stu-id="1155a-103">In-Process Servers</span></span>

<span data-ttu-id="1155a-104">Se si implementa un'applicazione server OLE come server in-process, ovvero una DLL in esecuzione nello spazio di processo dell'applicazione contenitore, anziché come server locale, un file EXE in esecuzione nello stesso spazio di processo, la comunicazione tra il contenitore e il server è semplificata perché la comunicazione tra i due può assumere la forma di normali chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="1155a-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="1155a-105">Non sono necessarie chiamate a procedure remote perché le due applicazioni vengono eseguite nello stesso spazio di processo.</span><span class="sxs-lookup"><span data-stu-id="1155a-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="1155a-106">Come ci si aspetterebbe, anche gli oggetti che gestiscono il marshalling dei parametri non sono necessari, anche se possono essere aggregati all'interno della DLL senza interferire con la comunicazione tra il contenitore e il server.</span><span class="sxs-lookup"><span data-stu-id="1155a-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="1155a-107">Quando un'applicazione server OLE viene implementata come server in-process, non è necessario un gestore di oggetti separato perché il server si trova nello spazio di elaborazione del client.</span><span class="sxs-lookup"><span data-stu-id="1155a-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="1155a-108">La differenza principale tra un server in-process e un gestore di oggetti è che il server è in grado di gestire l'oggetto in uno stato di esecuzione mentre il gestore non può.</span><span class="sxs-lookup"><span data-stu-id="1155a-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="1155a-109">Una conseguenza di questa differenza è che un server deve fornire un'interfaccia utente per la modifica dell'oggetto in esecuzione, mentre un gestore delega questo requisito al server dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1155a-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="1155a-110">Durante la creazione di un server in-process, è possibile aggregare il gestore predefinito OLE, consentendo di gestire le faccende di base, ad esempio la visualizzazione, l'archiviazione e le notifiche, mentre si implementano solo i servizi che il gestore non fornisce o non implementa nel modo necessario.</span><span class="sxs-lookup"><span data-stu-id="1155a-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="1155a-111">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="1155a-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1155a-112">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="1155a-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="1155a-113">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="1155a-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="1155a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1155a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1155a-115">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="1155a-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




