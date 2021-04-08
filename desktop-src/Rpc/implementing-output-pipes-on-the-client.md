---
title: Implementazione di pipe di output nel client
description: Quando si usa una pipe di output per trasferire i dati dal server al client, è necessario implementare una procedura push nel client.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff274491e2b665d86b550853d07c3ff6a4b2a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727791"
---
# <a name="implementing-output-pipes-on-the-client"></a><span data-ttu-id="ff783-103">Implementazione di pipe di output nel client</span><span class="sxs-lookup"><span data-stu-id="ff783-103">Implementing Output Pipes on the Client</span></span>

<span data-ttu-id="ff783-104">Quando si usa una pipe di output per trasferire i dati dal server al client, è necessario implementare una procedura push nel client.</span><span class="sxs-lookup"><span data-stu-id="ff783-104">When using an output pipe to transfer data from the server to the client, you must implement a push procedure in your client.</span></span> <span data-ttu-id="ff783-105">La procedura push accetta un puntatore a un buffer e un numero di elementi dallo stub client e, se il conteggio degli elementi è maggiore di 0, elabora i dati.</span><span class="sxs-lookup"><span data-stu-id="ff783-105">The push procedure takes a pointer to a buffer and an element count from the client stub and, if the element count is greater than 0, processes the data.</span></span> <span data-ttu-id="ff783-106">Ad esempio, è possibile copiare i dati dal buffer dello stub alla propria memoria.</span><span class="sxs-lookup"><span data-stu-id="ff783-106">For example, it could copy the data from the stub's buffer to its own memory.</span></span> <span data-ttu-id="ff783-107">In alternativa, è possibile elaborare i dati nel buffer dello stub e salvarli in un file.</span><span class="sxs-lookup"><span data-stu-id="ff783-107">Alternately, it could process the data in the stub's buffer and save it to a file.</span></span> <span data-ttu-id="ff783-108">Quando il numero di elementi è uguale a zero, la procedura push completa tutte le attività di pulizia necessarie prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="ff783-108">When the element count equals zero, the push procedure completes any needed cleanup tasks before returning.</span></span>

<span data-ttu-id="ff783-109">Nell'esempio seguente la funzione client ReceiveLongs alloca una struttura di pipe e un buffer di memoria globale.</span><span class="sxs-lookup"><span data-stu-id="ff783-109">In the following example, the client function ReceiveLongs allocates a pipe structure and a global memory buffer.</span></span> <span data-ttu-id="ff783-110">Inizializza la struttura, effettua la chiamata di procedura remota e quindi libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="ff783-110">It initializes the structure, makes the remote procedure call, and then frees the memory.</span></span>

## <a name="example"></a><span data-ttu-id="ff783-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff783-111">Example</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



<span data-ttu-id="ff783-112">Questo esempio include il file di intestazione generato dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="ff783-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="ff783-113">Per informazioni dettagliate, vedere [definizione di pipe nel file IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff783-113">For details see [Defining Pipes in IDL File](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="ff783-114">Viene inoltre dichiarata una variabile, globalPipeData, che utilizza come sink di dati.</span><span class="sxs-lookup"><span data-stu-id="ff783-114">It also declares a variable, globalPipeData, that it uses as the data sink.</span></span> <span data-ttu-id="ff783-115">La variabile globalBuffer è un buffer usato dalla procedura push per ricevere i blocchi di dati archiviati in globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="ff783-115">The variable globalBuffer is a buffer that the push procedure uses to receive blocks of data it stores in globalPipeData.</span></span>

<span data-ttu-id="ff783-116">La funzione ReceiveLongs dichiara una pipe e alloca lo spazio di memoria per la variabile globale di sink di dati.</span><span class="sxs-lookup"><span data-stu-id="ff783-116">The ReceiveLongs function declares a pipe and allocates memory space for the global data sink variable.</span></span> <span data-ttu-id="ff783-117">Nel programma client/server, il sink dei dati può essere un file o una struttura di dati creato dal client.</span><span class="sxs-lookup"><span data-stu-id="ff783-117">In your client/server program, the data sink can be a file or data structure the client creates.</span></span> <span data-ttu-id="ff783-118">In questo semplice esempio l'origine dati è un buffer allocato in modo dinamico di valori long integer.</span><span class="sxs-lookup"><span data-stu-id="ff783-118">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="ff783-119">Prima di poter iniziare il trasferimento dei dati, è necessario che il programma client Inizializza la struttura della pipe di output.</span><span class="sxs-lookup"><span data-stu-id="ff783-119">Before the data transfer can begin, your client program must initialize the output pipe structure.</span></span> <span data-ttu-id="ff783-120">È necessario impostare i puntatori sulla variabile di stato, sulla procedura di push e sulla procedura di allocazione.</span><span class="sxs-lookup"><span data-stu-id="ff783-120">It must set pointers to the state variable, the push procedure, and the alloc procedure.</span></span> <span data-ttu-id="ff783-121">In questo esempio, la variabile di pipe di output è denominata outputPipe.</span><span class="sxs-lookup"><span data-stu-id="ff783-121">In this example, the output pipe variable is called outputPipe.</span></span>

<span data-ttu-id="ff783-122">I client segnalano i server che sono pronti a ricevere i dati richiamando una procedura remota sul server.</span><span class="sxs-lookup"><span data-stu-id="ff783-122">Clients signal servers that they are ready to receive data by invoking a remote procedure on the server.</span></span> <span data-ttu-id="ff783-123">In questo esempio, la procedura remota viene chiamata outpipe.</span><span class="sxs-lookup"><span data-stu-id="ff783-123">In this example, the remote procedure is called OutPipe.</span></span> <span data-ttu-id="ff783-124">Quando il client chiama la procedura remota, il server avvia il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="ff783-124">When the client calls the remote procedure, the server begins the data transfer.</span></span> <span data-ttu-id="ff783-125">Ogni volta che arrivano i dati, lo stub client chiama le procedure di allocazione e push del client secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="ff783-125">Each time data arrives, the client stub calls the client's alloc and push procedures as needed.</span></span>

<span data-ttu-id="ff783-126">Anziché allocare memoria ogni volta che è necessario un buffer, la procedura di allocazione in questo esempio imposta semplicemente un puntatore sulla variabile globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="ff783-126">Rather than allocate memory each time a buffer is needed, the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="ff783-127">La procedura pull riutilizza quindi questo buffer ogni volta che trasferisce i dati.</span><span class="sxs-lookup"><span data-stu-id="ff783-127">The pull procedure then reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="ff783-128">Per i programmi client più complessi potrebbe essere necessario allocare un nuovo buffer ogni volta che il server estrae i dati dal client.</span><span class="sxs-lookup"><span data-stu-id="ff783-128">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="ff783-129">La procedura push in questo esempio usa la variabile di stato per tenere traccia della posizione successiva in cui archivia i dati nel buffer di sink di dati globali.</span><span class="sxs-lookup"><span data-stu-id="ff783-129">The push procedure in this example uses the state variable to track the next position where it will store data in the global data sink buffer.</span></span> <span data-ttu-id="ff783-130">Scrive i dati dal buffer della pipe nel buffer di sink.</span><span class="sxs-lookup"><span data-stu-id="ff783-130">It writes data from the pipe buffer into sink buffer.</span></span> <span data-ttu-id="ff783-131">Lo stub del client riceve quindi il blocco di dati successivo dal server e lo archivia nel buffer della pipe.</span><span class="sxs-lookup"><span data-stu-id="ff783-131">The client stub then receives the next block of data from the server and stores it in the pipe buffer.</span></span> <span data-ttu-id="ff783-132">Quando tutti i dati sono stati inviati, il server trasmette un buffer di dimensioni zero.</span><span class="sxs-lookup"><span data-stu-id="ff783-132">When all the data has been sent, the server transmits a zero-sized buffer.</span></span> <span data-ttu-id="ff783-133">Viene così indicata la procedura push per arrestare la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ff783-133">This cues the push procedure to stop receiving data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff783-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff783-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff783-135">inviare tramite pipe</span><span class="sxs-lookup"><span data-stu-id="ff783-135">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="ff783-136">**/OI**</span><span class="sxs-lookup"><span data-stu-id="ff783-136">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 