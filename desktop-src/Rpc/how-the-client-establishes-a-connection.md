---
title: Come il client stabilisce una connessione
description: Per stabilire una sessione di comunicazione client/server con un programma server, è necessario che le applicazioni client con handle espliciti creino un handle di associazione.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044831"
---
# <a name="how-the-client-establishes-a-connection"></a><span data-ttu-id="474f1-103">Come il client stabilisce una connessione</span><span class="sxs-lookup"><span data-stu-id="474f1-103">How the Client Establishes a Connection</span></span>

<span data-ttu-id="474f1-104">Per stabilire una sessione di comunicazione client/server con un programma server, è necessario che le applicazioni client con handle espliciti creino un handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="474f1-104">To establish a client/server communication session with a server program, client applications with explicit handles need to create a binding handle.</span></span> <span data-ttu-id="474f1-105">Una volta eseguita questa operazione, la libreria di runtime RPC trova il computer che ospita il programma server.</span><span class="sxs-lookup"><span data-stu-id="474f1-105">After they do, the RPC run-time library finds the computer that hosts the server program.</span></span> <span data-ttu-id="474f1-106">Trova quindi l'endpoint su cui il programma server è in ascolto e indirizza la chiamata.</span><span class="sxs-lookup"><span data-stu-id="474f1-106">It then finds the endpoint that the server program is listening to and directs the call to it.</span></span> <span data-ttu-id="474f1-107">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="474f1-107">The following diagram illustrates this process.</span></span>

![un client RPC stabilisce una connessione con un server RPC](images/clntcon.png)

<span data-ttu-id="474f1-109">In questa sezione vengono fornite informazioni sul modo in cui il client si connette al programma server ed esegue le procedure remote che offre.</span><span class="sxs-lookup"><span data-stu-id="474f1-109">This section presents information about how the client connects to the server program and executes remote procedures that it offers.</span></span> <span data-ttu-id="474f1-110">Sono disponibili molti approcci per completare questi passaggi. a seconda della progettazione scelta, un'applicazione può scegliere una serie diversa di passaggi.</span><span class="sxs-lookup"><span data-stu-id="474f1-110">There are many approaches to completing these steps; depending on the design chosen, an application may choose a different set of steps.</span></span> <span data-ttu-id="474f1-111">Questo esempio è semplicemente un modo per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="474f1-111">This example is simply one way of doing so.</span></span>

<span data-ttu-id="474f1-112">La discussione è divisa nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="474f1-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="474f1-113">Creazione di un handle di associazione</span><span class="sxs-lookup"><span data-stu-id="474f1-113">Creating a Binding Handle</span></span>](creating-a-binding-handle.md)
-   [<span data-ttu-id="474f1-114">Esecuzione di una chiamata di procedura remota</span><span class="sxs-lookup"><span data-stu-id="474f1-114">Making a Remote Procedure Call</span></span>](making-a-remote-procedure-call.md)
-   [<span data-ttu-id="474f1-115">Ricerca del programma server</span><span class="sxs-lookup"><span data-stu-id="474f1-115">Finding the Server Program</span></span>](finding-the-server-program.md)
-   [<span data-ttu-id="474f1-116">Invio della chiamata al programma server</span><span class="sxs-lookup"><span data-stu-id="474f1-116">Sending the Call to the Server Program</span></span>](sending-the-call-to-the-server-program.md)

 

 




