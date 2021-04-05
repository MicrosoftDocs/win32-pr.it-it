---
title: Client e server COM
description: Un aspetto fondamentale di COM è il modo in cui i client e i server interagiscono.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710969"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="d050e-103">Client e server COM</span><span class="sxs-lookup"><span data-stu-id="d050e-103">COM Clients and Servers</span></span>

<span data-ttu-id="d050e-104">Un aspetto fondamentale di COM è il modo in cui i client e i server interagiscono.</span><span class="sxs-lookup"><span data-stu-id="d050e-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="d050e-105">Un *client com* è qualsiasi codice o oggetto che ottiene un puntatore a un server com e utilizza i relativi servizi chiamando i metodi delle relative interfacce.</span><span class="sxs-lookup"><span data-stu-id="d050e-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="d050e-106">Un *Server com* è qualsiasi oggetto che fornisce servizi ai client; questi servizi sono sotto forma di implementazioni di interfaccia COM che possono essere chiamate da qualsiasi client in grado di ottenere un puntatore a una delle interfacce nell'oggetto server.</span><span class="sxs-lookup"><span data-stu-id="d050e-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="d050e-107">Esistono due tipi principali di server, *in-process* e *out-of-process*.</span><span class="sxs-lookup"><span data-stu-id="d050e-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="d050e-108">I server in-process sono implementati in una libreria a collegamento dinamico (DLL) e i server out-of-process sono implementati in un file eseguibile (EXE).</span><span class="sxs-lookup"><span data-stu-id="d050e-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="d050e-109">I server out-of-process possono risiedere nel computer locale o in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="d050e-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="d050e-110">Inoltre, COM fornisce un meccanismo che consente a un server in-process (DLL) di essere eseguito in un processo di EXE surrogato per ottenere il vantaggio di poter eseguire il processo in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="d050e-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="d050e-111">Per ulteriori informazioni, vedere la pagina relativa ai [surrogati dll](dll-surrogates.md).</span><span class="sxs-lookup"><span data-stu-id="d050e-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="d050e-112">Il modello di programmazione COM e i costrutti sono ora stati estesi in modo che i client e i server COM possano interagire in rete, non solo all'interno di un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="d050e-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="d050e-113">In questo modo le applicazioni esistenti possono interagire con le nuove applicazioni e tra loro attraverso le reti con l'amministrazione corretta e le nuove applicazioni possono essere scritte per sfruttare le funzionalità di rete.</span><span class="sxs-lookup"><span data-stu-id="d050e-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="d050e-114">Non è necessario che le applicazioni client COM siano consapevoli del modo in cui gli oggetti server sono inclusi nel pacchetto, che siano inclusi in un pacchetto come oggetti in-process (in dll) o come oggetti locali o remoti (in exe).</span><span class="sxs-lookup"><span data-stu-id="d050e-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="d050e-115">Distributed COM consente inoltre di creare pacchetti di oggetti come applicazioni di servizio, sincronizzando COM con le complesse funzionalità amministrative e di integrazione di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="d050e-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="d050e-116">In questa documentazione l'acronimo COM viene usato in modo preferenziale per DCOM.</span><span class="sxs-lookup"><span data-stu-id="d050e-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="d050e-117">Questo perché DCOM non è separato, ma è solo COM con una rete più lunga.</span><span class="sxs-lookup"><span data-stu-id="d050e-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="d050e-118">Nei casi in cui viene descritto in particolare un'operazione remota, viene usato il termine *Distributed COM* .</span><span class="sxs-lookup"><span data-stu-id="d050e-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="d050e-119">COM è progettato per consentire di aggiungere il supporto per la trasparenza della località che si estende in una rete.</span><span class="sxs-lookup"><span data-stu-id="d050e-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="d050e-120">Consente le applicazioni scritte per i singoli computer per l'esecuzione in una rete e fornisce funzionalità che estendono queste funzionalità e aggiungono alla sicurezza necessaria in una rete.</span><span class="sxs-lookup"><span data-stu-id="d050e-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="d050e-121">Per ulteriori informazioni, vedere [sicurezza in com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="d050e-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="d050e-122">COM specifica un meccanismo mediante il quale il codice della classe può essere utilizzato da molte applicazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="d050e-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="d050e-123">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="d050e-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d050e-124">Recupero di un puntatore a un oggetto</span><span class="sxs-lookup"><span data-stu-id="d050e-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="d050e-125">Creazione di un oggetto tramite un oggetto classe</span><span class="sxs-lookup"><span data-stu-id="d050e-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="d050e-126">Responsabilità server COM</span><span class="sxs-lookup"><span data-stu-id="d050e-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="d050e-127">Stato oggetto permanente</span><span class="sxs-lookup"><span data-stu-id="d050e-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="d050e-128">Fornire informazioni sulla classe</span><span class="sxs-lookup"><span data-stu-id="d050e-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="d050e-129">Comunicazione tra oggetti</span><span class="sxs-lookup"><span data-stu-id="d050e-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="d050e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d050e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d050e-131">Sincronizzazione delle chiamate</span><span class="sxs-lookup"><span data-stu-id="d050e-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="d050e-132">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="d050e-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




