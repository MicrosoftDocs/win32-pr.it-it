---
title: Selezione di una sequenza di protocollo
description: Una sequenza di protocollo è il linguaggio usato da un sistema operativo di rete per comunicare in rete con altri computer.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045166"
---
# <a name="selecting-a-protocol-sequence"></a><span data-ttu-id="e2f51-103">Selezione di una sequenza di protocollo</span><span class="sxs-lookup"><span data-stu-id="e2f51-103">Selecting a Protocol Sequence</span></span>

<span data-ttu-id="e2f51-104">Una sequenza di protocollo è il linguaggio usato da un sistema operativo di rete per comunicare in rete con altri computer.</span><span class="sxs-lookup"><span data-stu-id="e2f51-104">A protocol sequence is the language that a network operating system uses to talk over the network to other computers.</span></span> <span data-ttu-id="e2f51-105">In termini più specifici, le applicazioni RPC devono specificare una stringa che rappresenta una combinazione di un protocollo RPC, un protocollo di trasporto e un protocollo di rete.</span><span class="sxs-lookup"><span data-stu-id="e2f51-105">In more specific terms, RPC applications must specify a string that represents a combination of an RPC protocol, a transport protocol, and a network protocol.</span></span>

<span data-ttu-id="e2f51-106">Microsoft RPC supporta tre protocolli RPC:</span><span class="sxs-lookup"><span data-stu-id="e2f51-106">Microsoft RPC supports three RPC protocols:</span></span>

-   <span data-ttu-id="e2f51-107">Protocollo NCACN (Network Computing Architecture)</span><span class="sxs-lookup"><span data-stu-id="e2f51-107">Network Computing Architecture connection-oriented protocol (NCACN)</span></span>
-   <span data-ttu-id="e2f51-108">NCADG (Network Computing Architecture datagramma Protocol)</span><span class="sxs-lookup"><span data-stu-id="e2f51-108">Network Computing Architecture datagram protocol (NCADG)</span></span>
-   <span data-ttu-id="e2f51-109">Chiamata di procedura remota locale per l'architettura di Network Computing (NCALRPC)</span><span class="sxs-lookup"><span data-stu-id="e2f51-109">Network Computing Architecture local remote procedure call (NCALRPC)</span></span>

<span data-ttu-id="e2f51-110">Le applicazioni RPC possono utilizzare il protocollo NCALRPC per richiamare le procedure offerte dai programmi server in esecuzione nello stesso computer in cui viene eseguito il programma client.</span><span class="sxs-lookup"><span data-stu-id="e2f51-110">RPC applications can use the NCALRPC protocol to invoke procedures offered by server programs running on the same computer that the client program runs on.</span></span> <span data-ttu-id="e2f51-111">Questo è, di gran lunga, il metodo più efficiente per chiamare la funzionalità in un processo diverso nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="e2f51-111">This is, by far, the most efficient method for calling functionality in a different process on the same computer.</span></span>

<span data-ttu-id="e2f51-112">I protocolli di trasporto e di rete utilizzati dall'applicazione dipendono dai protocolli supportati dalla rete.</span><span class="sxs-lookup"><span data-stu-id="e2f51-112">The transport and network protocols that your application uses depend on which protocols the network supports.</span></span> <span data-ttu-id="e2f51-113">Molte reti attualmente, tra cui Internet, supportano TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e2f51-113">Many networks today, including the Internet, support TCP/IP.</span></span> <span data-ttu-id="e2f51-114">Altri protocolli di trasporto e di rete comuni sono IPX/SPX, NetBIOS e AppleTalk DSP.</span><span class="sxs-lookup"><span data-stu-id="e2f51-114">Other common transport and network protocols are IPX/SPX, NetBIOS, and AppleTalk DSP.</span></span> <span data-ttu-id="e2f51-115">Microsoft RPC supporta questi e altri protocolli di trasporto e di rete.</span><span class="sxs-lookup"><span data-stu-id="e2f51-115">Microsoft RPC supports these and other transport and network protocols.</span></span> <span data-ttu-id="e2f51-116">Per un elenco completo, vedere [costanti di sequenza del protocollo](protocol-sequence-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2f51-116">For a complete list, see [Protocol Sequence Constants](protocol-sequence-constants.md).</span></span>

<span data-ttu-id="e2f51-117">Quando l'applicazione usa handle di associazione automatici, non è necessario specificare la sequenza di protocolli.</span><span class="sxs-lookup"><span data-stu-id="e2f51-117">When your application uses automatic binding handles, it does not need to specify the protocol sequence.</span></span> <span data-ttu-id="e2f51-118">Se usa handle impliciti o espliciti, deve ottenere o specificare la sequenza di protocolli.</span><span class="sxs-lookup"><span data-stu-id="e2f51-118">If it uses implicit or explicit handles, it must obtain or specify the protocol sequence.</span></span> <span data-ttu-id="e2f51-119">Ogni sistema distribuito deve esaminare l'ambiente in cui verrà distribuito per determinare la sequenza di protocollo più adatta a tale ambiente.</span><span class="sxs-lookup"><span data-stu-id="e2f51-119">Each distributed system must examine the environment in which it will be deployed to determine which protocol sequence is best suited for that environment.</span></span>

<span data-ttu-id="e2f51-120">Non tutte le sequenze di protocollo hanno funzionalità equivalenti.</span><span class="sxs-lookup"><span data-stu-id="e2f51-120">Not all protocol sequences have equivalent functionality.</span></span> <span data-ttu-id="e2f51-121">Gli sviluppatori devono verificare che la sequenza di protocollo scelta supporti le funzionalità necessarie.</span><span class="sxs-lookup"><span data-stu-id="e2f51-121">Developers should verify that the chosen protocol sequence supports the required features.</span></span> <span data-ttu-id="e2f51-122">In generale, è consigliabile usare **ncalrpc** per le comunicazioni locali e **ncacn \_ IP \_ TCP** o **ncacn \_ http** per le comunicazioni remote. funzionano in tutti gli ambienti, presentano prestazioni ottimali e supportano tutte le funzionalità necessarie per le procedure consigliate.</span><span class="sxs-lookup"><span data-stu-id="e2f51-122">In general, **ncalrpc** for local communications and **ncacn\_ip\_tcp** or **ncacn\_http** for remote communications are recommended; they work in all environments, they have optimal performance, and they support all necessary, best-practice features.</span></span>

<span data-ttu-id="e2f51-123">I client possono inoltre specificare le informazioni sulla sequenza di protocollo ottenute dal Active Directory, dal registro di sistema, dalle variabili di ambiente create e inizializzate dal programma di installazione, dai file di configurazione specifici dell'applicazione o dalle stringhe letterali nel codice sorgente del programma.</span><span class="sxs-lookup"><span data-stu-id="e2f51-123">Clients can also specify protocol sequence information that they obtain from Active Directory, the registry, environment variables created and initialized by the setup program, application-specific configuration files, or from literal strings in the program source code.</span></span>

<span data-ttu-id="e2f51-124">Quando il programma client dispone di una stringa di sequenza di protocollo valida, può passare le informazioni alle funzioni [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) e [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per creare l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="e2f51-124">After your client program has a valid protocol sequence string, it can pass that information to the [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) and [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) functions to create the binding handle.</span></span>

 

 




