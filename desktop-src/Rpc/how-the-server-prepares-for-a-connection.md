---
title: Preparazione del server per una connessione
description: Quando un programma server inizia l'esecuzione, deve prima registrare l'interfaccia o le interfacce che contiene con la libreria di runtime RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330623"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="21114-103">Preparazione del server per una connessione</span><span class="sxs-lookup"><span data-stu-id="21114-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="21114-104">Quando un programma server inizia l'esecuzione, deve prima registrare l'interfaccia o le interfacce che contiene con la libreria di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="21114-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="21114-105">Vengono quindi create le informazioni di binding necessarie.</span><span class="sxs-lookup"><span data-stu-id="21114-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="21114-106">Il programma server deve inoltre registrare l'endpoint o gli endpoint su cui è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="21114-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="21114-107">Può quindi iniziare ad ascoltare le chiamate del client.</span><span class="sxs-lookup"><span data-stu-id="21114-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="21114-108">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="21114-108">This process is illustrated in the following diagram.</span></span>

![un'applicazione server RPC si prepara per le connessioni client](images/srvrcon.png)

<span data-ttu-id="21114-110">A seconda della progettazione scelta, un'applicazione server può scegliere un set di passaggi diverso; Nell'esempio precedente viene illustrato un approccio.</span><span class="sxs-lookup"><span data-stu-id="21114-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="21114-111">In questa sezione vengono presentate informazioni sui passaggi che un processo server deve eseguire per preparare la connessione.</span><span class="sxs-lookup"><span data-stu-id="21114-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="21114-112">La discussione è divisa nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="21114-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="21114-113">Registrazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="21114-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="21114-114">Rendere disponibile il server in rete</span><span class="sxs-lookup"><span data-stu-id="21114-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="21114-115">Registrazione degli endpoint</span><span class="sxs-lookup"><span data-stu-id="21114-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="21114-116">Ascolto delle chiamate client</span><span class="sxs-lookup"><span data-stu-id="21114-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




