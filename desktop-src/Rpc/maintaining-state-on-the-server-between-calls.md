---
title: Gestione dello stato sul server tra le chiamate
description: Spesso è necessario mantenere lo stato sul server tra le chiamate RPC separate \ 8212. l'uso di handle di contesto è il modo migliore per eseguire questa operazione. Di seguito sono riportate alcune parole sulla modalità di funzionamento interna degli handle di contesto per la comprensione del funzionamento ottimale del contesto.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC (Remote Procedure Call), procedure consigliate, gestione dello stato tra le chiamate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707186"
---
# <a name="maintaining-state-on-the-server-between-calls"></a><span data-ttu-id="72c4b-105">Gestione dello stato sul server tra le chiamate</span><span class="sxs-lookup"><span data-stu-id="72c4b-105">Maintaining State on the Server Between Calls</span></span>

<span data-ttu-id="72c4b-106">Spesso è necessario mantenere lo stato sul server tra chiamate RPC separate, usando gli handle di contesto è il modo migliore per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="72c4b-106">It is often necessary to maintain state on the server between separate RPC calls—using context handles is the best way to do so.</span></span> <span data-ttu-id="72c4b-107">Di seguito sono riportate alcune parole sulla modalità di funzionamento interna degli handle di contesto per la comprensione del funzionamento ottimale del contesto.</span><span class="sxs-lookup"><span data-stu-id="72c4b-107">A few words about how context handles operate internally helps in understanding when context handles work best.</span></span>

<span data-ttu-id="72c4b-108">Il client non riceve mai lo stato mantenuto nel server.</span><span class="sxs-lookup"><span data-stu-id="72c4b-108">The client never receives the state kept on the server.</span></span> <span data-ttu-id="72c4b-109">La maggior parte delle volte lo stato sul server è un puntatore a un blocco di memoria e il client non ha informazioni su di esso.</span><span class="sxs-lookup"><span data-stu-id="72c4b-109">Most often the state on the server is a pointer to a memory block, and the client has no information about it.</span></span> <span data-ttu-id="72c4b-110">Tutte le ricevute del client sono un numero univoco di grandi dimensioni, con altre informazioni associate, che il server invia al client e che rappresenta il punto di gestione del contesto in tutte le operazioni successive.</span><span class="sxs-lookup"><span data-stu-id="72c4b-110">All the client receives is a large unique number, with other information associated with it, that the server sends to the client and which represents the context handle in all subsequent operations.</span></span> <span data-ttu-id="72c4b-111">Ogni volta che il client fa riferimento a un handle aperto, invia il numero elevato ricevuto dal server al momento dell'apertura dell'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="72c4b-111">Whenever the client refers to an opened handle, it sends the large number it received from the server when that context handle was opened.</span></span>

<span data-ttu-id="72c4b-112">Il server tiene traccia di tutti i numeri elevati inviati a un client.</span><span class="sxs-lookup"><span data-stu-id="72c4b-112">The server keeps track of all large numbers it sends to a client.</span></span> <span data-ttu-id="72c4b-113">Quando il server riceve un numero elevato che rappresenta un handle di contesto, Cerca il numero nell'insieme di handle di contesto validi e in attesa per il client e trova il contesto lato server corrispondente a un numero elevato specificato.</span><span class="sxs-lookup"><span data-stu-id="72c4b-113">When the server receives a large number representing a context handle, it looks up the number in the collection of valid, outstanding context handles for that client, and finds the server-side context corresponding to a given large number.</span></span> <span data-ttu-id="72c4b-114">Viene passato alla routine del server.</span><span class="sxs-lookup"><span data-stu-id="72c4b-114">This is passed to the server routine.</span></span> <span data-ttu-id="72c4b-115">Se il numero elevato non viene trovato, \_ \_ \_ \_ viene generata un'eccezione di mancata corrispondenza del contesto RPC X SS e propagata al client.</span><span class="sxs-lookup"><span data-stu-id="72c4b-115">If the large number is not found, an RPC\_X\_SS\_CONTEXT\_MISMATCH exception is raised and propagated to the client.</span></span>

<span data-ttu-id="72c4b-116">Il corollari di questa progettazione è il seguente:</span><span class="sxs-lookup"><span data-stu-id="72c4b-116">The corollaries of this design are as follows:</span></span>

-   <span data-ttu-id="72c4b-117">Un handle di contesto è valido solo nel contesto della sessione client/server esistente.</span><span class="sxs-lookup"><span data-stu-id="72c4b-117">A context handle is valid only in the context of the existing client/server session.</span></span> <span data-ttu-id="72c4b-118">Non può essere passato a un altro client.</span><span class="sxs-lookup"><span data-stu-id="72c4b-118">It cannot be passed to another client.</span></span>
-   <span data-ttu-id="72c4b-119">Un handle di contesto diventa non valido se il server viene riavviato o perde la connessione al client.</span><span class="sxs-lookup"><span data-stu-id="72c4b-119">A context handle becomes invalid if the server is rebooted, or otherwise loses its connection to the client.</span></span>
-   <span data-ttu-id="72c4b-120">Il client non è in grado di interpretare il punto di gestione del contesto rappresentato nel server.</span><span class="sxs-lookup"><span data-stu-id="72c4b-120">The client cannot interpret what the context handle represents on the server.</span></span> <span data-ttu-id="72c4b-121">Per un client, tutti gli handle di contesto sono semplicemente numeri elevati.</span><span class="sxs-lookup"><span data-stu-id="72c4b-121">To a client, all context handles are simply large numbers.</span></span>

<span data-ttu-id="72c4b-122">Se il client ha esito negativo, il server riceve una notifica e pulisce i relativi handle di contesto usando il meccanismo di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="72c4b-122">If the client fails, the server will get a notification and will clean up its context handles using the run-down mechanism.</span></span>

 

 




