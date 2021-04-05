---
title: Terminologia di associazione RPC essenziale
description: Per semplificare la discussione del processo di connessione client/server, è utile comprendere i termini seguenti.
ms.assetid: 05aca325-87ee-4581-9152-a8a2ff7fb490
keywords:
- RPC (Remote Procedure Call) RPC, descritta, associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18b8d3872c830d90079ad740505fead14c1b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047194"
---
# <a name="essential-rpc-binding-terminology"></a><span data-ttu-id="6818c-104">Terminologia di associazione RPC essenziale</span><span class="sxs-lookup"><span data-stu-id="6818c-104">Essential RPC Binding Terminology</span></span>

<span data-ttu-id="6818c-105">Per semplificare la discussione del processo di connessione client/server, è utile comprendere i termini seguenti.</span><span class="sxs-lookup"><span data-stu-id="6818c-105">To better aid in a discussion of the client/server connection process, it is helpful to know the following terms.</span></span>

## <a name="parameters"></a><span data-ttu-id="6818c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6818c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6818c-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Sequenza di protocollo</span><span class="sxs-lookup"><span data-stu-id="6818c-107"><span id="Protocol_Sequence"></span><span id="protocol_sequence"></span><span id="PROTOCOL_SEQUENCE"></span>Protocol Sequence</span></span>
</dt> <dd>

<span data-ttu-id="6818c-108">Quando i sistemi operativi di rete comunicano tra loro, devono restare in ascolto e parlare della stessa lingua.</span><span class="sxs-lookup"><span data-stu-id="6818c-108">When network operating systems communicate with each other, they must listen and speak the same language.</span></span> <span data-ttu-id="6818c-109">Queste lingue sono denominate *sequenze di protocollo*.</span><span class="sxs-lookup"><span data-stu-id="6818c-109">These languages are called *protocol sequences*.</span></span> <span data-ttu-id="6818c-110">I programmi client e server devono usare le sequenze di protocollo supportate dalla rete che li connette.</span><span class="sxs-lookup"><span data-stu-id="6818c-110">Client and server programs must use protocol sequences that the network connecting them supports.</span></span> <span data-ttu-id="6818c-111">Microsoft RPC supporta un'ampia gamma di sequenze di protocolli.</span><span class="sxs-lookup"><span data-stu-id="6818c-111">Microsoft RPC supports a variety of protocol sequences.</span></span> <span data-ttu-id="6818c-112">Per informazioni dettagliate, vedere [selezione di una sequenza di protocollo](selecting-a-protocol-sequence.md), [specifica di sequenze di protocollo](specifying-protocol-sequences.md)ed [**endpoint**](/windows/desktop/Midl/endpoint).</span><span class="sxs-lookup"><span data-stu-id="6818c-112">For details, see [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md), [Specifying Protocol Sequences](specifying-protocol-sequences.md), and [**endpoint**](/windows/desktop/Midl/endpoint).</span></span>

</dd> <dt>

<span data-ttu-id="6818c-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Computer host server o sistema host server</span><span class="sxs-lookup"><span data-stu-id="6818c-113"><span id="Server_Host_Computer_or_Server_Host_System"></span><span id="server_host_computer_or_server_host_system"></span><span id="SERVER_HOST_COMPUTER_OR_SERVER_HOST_SYSTEM"></span>Server Host Computer or Server Host System</span></span>
</dt> <dd>

<span data-ttu-id="6818c-114">Il programma server viene eseguito nel computer host server.</span><span class="sxs-lookup"><span data-stu-id="6818c-114">The server program runs on the server host computer.</span></span> <span data-ttu-id="6818c-115">Tuttavia, la maggior parte della letteratura sull'elaborazione client/server si riferisce sia al programma server sia al computer host server come "Server".</span><span class="sxs-lookup"><span data-stu-id="6818c-115">However, much literature on client/server computing refers to both the server program and the server host computer as the "server."</span></span> <span data-ttu-id="6818c-116">Il risultato è che non è sempre chiaro che verrà discusso.</span><span class="sxs-lookup"><span data-stu-id="6818c-116">The result is that it is not always clear which is being discussed.</span></span>

</dd> <dt>

<span data-ttu-id="6818c-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span><span class="sxs-lookup"><span data-stu-id="6818c-117"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span>
</dt> <dd>

<span data-ttu-id="6818c-118">I programmi server restano in attesa di una porta o di un gruppo di porte nel computer host server per le richieste client.</span><span class="sxs-lookup"><span data-stu-id="6818c-118">Server programs listen to a port or a group of ports on the server host computer for client requests.</span></span> <span data-ttu-id="6818c-119">I sistemi host server gestiscono un database di queste porte, denominate endpoint in RPC.</span><span class="sxs-lookup"><span data-stu-id="6818c-119">Server host systems maintain a database of these ports, which are called endpoints in RPC.</span></span> <span data-ttu-id="6818c-120">Il database è denominato mappa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6818c-120">The database is called the endpoint map.</span></span>

</dd> <dt>

<span data-ttu-id="6818c-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Associazione</span><span class="sxs-lookup"><span data-stu-id="6818c-121"><span id="Binding"></span><span id="binding"></span><span id="BINDING"></span>Binding</span></span>
</dt> <dd>

<span data-ttu-id="6818c-122">I programmi client creano un'associazione al server per stabilire una sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="6818c-122">Client programs create a binding to the server to establish a communication session.</span></span> <span data-ttu-id="6818c-123">Un'associazione contiene tutte le informazioni necessarie per la creazione della sessione da parte delle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="6818c-123">A binding contains all of the information the client applications needs to create the session.</span></span>

</dd> </dl>

 

 