---
title: Implementazione di pipe di output nel server
description: Per iniziare a ricevere dati da un server, un client chiama una delle procedure remote del server.
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047246"
---
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="a5db0-103">Implementazione di pipe di output nel server</span><span class="sxs-lookup"><span data-stu-id="a5db0-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="a5db0-104">Per iniziare a ricevere dati da un server, un client chiama una delle procedure remote del server.</span><span class="sxs-lookup"><span data-stu-id="a5db0-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="a5db0-105">Questa procedura deve chiamare ripetutamente la procedura push nello stub del server.</span><span class="sxs-lookup"><span data-stu-id="a5db0-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="a5db0-106">Il compilatore MIDL usa il file IDL dell'applicazione per generare automaticamente la procedura push del server.</span><span class="sxs-lookup"><span data-stu-id="a5db0-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="a5db0-107">La routine del server remoto deve riempire il buffer della pipe di output con i dati prima di chiamare la procedura di push.</span><span class="sxs-lookup"><span data-stu-id="a5db0-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="a5db0-108">Ogni volta che il programma server richiama la procedura push nello stub, la procedura push esegue il marshalling dei dati e li trasmette al client.</span><span class="sxs-lookup"><span data-stu-id="a5db0-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="a5db0-109">Il ciclo continua fino a quando il server non invia un buffer di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="a5db0-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="a5db0-110">Nell'esempio seguente viene utilizzato il programma Pipedemo contenuto negli esempi forniti con il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a5db0-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="a5db0-111">Viene illustrata una procedura server remota che utilizza una pipe per eseguire il push dei dati dal server al client.</span><span class="sxs-lookup"><span data-stu-id="a5db0-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a><span data-ttu-id="a5db0-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5db0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5db0-113">inviare tramite pipe</span><span class="sxs-lookup"><span data-stu-id="a5db0-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="a5db0-114">**/OI**</span><span class="sxs-lookup"><span data-stu-id="a5db0-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 