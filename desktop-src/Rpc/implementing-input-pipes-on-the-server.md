---
title: Implementazione di pipe di input nel server
description: Per iniziare a inviare dati a un server, un client chiama una delle procedure remote del server.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856330"
---
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="9481b-103">Implementazione di pipe di input nel server</span><span class="sxs-lookup"><span data-stu-id="9481b-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="9481b-104">Per iniziare a inviare dati a un server, un client chiama una delle procedure remote del server.</span><span class="sxs-lookup"><span data-stu-id="9481b-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="9481b-105">Questa procedura deve chiamare ripetutamente la procedura pull nello stub del server.</span><span class="sxs-lookup"><span data-stu-id="9481b-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="9481b-106">Il compilatore MIDL usa il file IDL dell'applicazione per generare automaticamente la procedura pull del server.</span><span class="sxs-lookup"><span data-stu-id="9481b-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="9481b-107">Ogni volta che il programma server richiama la procedura pull nello stub, la procedura pull riceve i blocchi di dati dal client.</span><span class="sxs-lookup"><span data-stu-id="9481b-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="9481b-108">Esegue l'unmarshalling dei dati nel buffer del server.</span><span class="sxs-lookup"><span data-stu-id="9481b-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="9481b-109">La procedura remota del server può quindi elaborare questi dati in qualsiasi modo necessario.</span><span class="sxs-lookup"><span data-stu-id="9481b-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="9481b-110">Il ciclo continua fino a quando il server non riceve un buffer di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="9481b-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="9481b-111">Nell'esempio seguente viene utilizzato il programma Pipedemo contenuto negli esempi forniti con Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9481b-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="9481b-112">Viene illustrata una procedura server remota che utilizza una pipe per eseguire il pull dei dati dal client al server.</span><span class="sxs-lookup"><span data-stu-id="9481b-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




