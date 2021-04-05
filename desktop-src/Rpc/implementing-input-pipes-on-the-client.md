---
title: Implementazione di pipe di input nel client
description: Quando si utilizza una pipe di input per trasferire i dati dal client al server, è necessario implementare una procedura pull.
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810caa31c4932294797a5ed502c6f93d8613ea0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872777"
---
# <a name="implementing-input-pipes-on-the-client"></a><span data-ttu-id="53c1f-103">Implementazione di pipe di input nel client</span><span class="sxs-lookup"><span data-stu-id="53c1f-103">Implementing Input Pipes on the Client</span></span>

<span data-ttu-id="53c1f-104">Quando si utilizza una pipe di input per trasferire i dati dal client al server, è necessario implementare una procedura pull.</span><span class="sxs-lookup"><span data-stu-id="53c1f-104">When using an input pipe to transfer data from the client to the server, you must implement a pull procedure.</span></span> <span data-ttu-id="53c1f-105">La procedura pull deve trovare i dati da trasferire, leggere i dati nel buffer e impostare il numero di elementi da inviare.</span><span class="sxs-lookup"><span data-stu-id="53c1f-105">The pull procedure must find the data to be transferred, read the data into the buffer, and set the number of elements to send.</span></span> <span data-ttu-id="53c1f-106">Non tutti i dati devono trovarsi nel buffer quando il server inizia a eseguire il pull dei dati a se stesso.</span><span class="sxs-lookup"><span data-stu-id="53c1f-106">Not all of the data has to be in the buffer when the server begins to pull data to itself.</span></span> <span data-ttu-id="53c1f-107">La procedura pull può riempire il buffer in modo incrementale.</span><span class="sxs-lookup"><span data-stu-id="53c1f-107">The pull procedure can fill the buffer incrementally.</span></span>

<span data-ttu-id="53c1f-108">Quando non sono più presenti dati da inviare, la routine imposta l'ultimo argomento su zero.</span><span class="sxs-lookup"><span data-stu-id="53c1f-108">When there is no more data to send, the procedure sets its last argument to zero.</span></span> <span data-ttu-id="53c1f-109">Quando vengono inviati tutti i dati, la procedura pull deve eseguire tutte le operazioni di pulizia necessarie prima di restituire.</span><span class="sxs-lookup"><span data-stu-id="53c1f-109">When all the data is sent, the pull procedure should do any needed cleanup before returning.</span></span> <span data-ttu-id="53c1f-110">Per un parametro che è un \[ in, out \] pipe, la procedura pull deve reimpostare la variabile di stato del client dopo che tutti i dati sono stati trasmessi, in modo che la procedura push possa usarla per ricevere i dati.</span><span class="sxs-lookup"><span data-stu-id="53c1f-110">For a parameter that is an \[in, out\] pipe, the pull procedure must reset the client's state variable after all the data has been transmitted, so that the push procedure can use it to receive data.</span></span>

<span data-ttu-id="53c1f-111">L'esempio seguente viene estratto dal programma Pipedemo incluso nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="53c1f-111">The following example is extracted from the Pipedemo program included with the Platform Software Development Kit (SDK).</span></span>


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
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
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



<span data-ttu-id="53c1f-112">Questo esempio include il file di intestazione generato dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="53c1f-112">This example includes the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="53c1f-113">Per informazioni dettagliate, vedere [definizione di pipe nei file IDL](defining-pipes-in-idl-files.md).</span><span class="sxs-lookup"><span data-stu-id="53c1f-113">For details see [Defining Pipes in IDL Files](defining-pipes-in-idl-files.md).</span></span> <span data-ttu-id="53c1f-114">Viene inoltre dichiarata una variabile utilizzata come origine dati denominata globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="53c1f-114">It also declares a variable it uses as the data source called globalPipeData.</span></span> <span data-ttu-id="53c1f-115">La variabile globalBuffer è un buffer usato dalla procedura pull per inviare i blocchi di dati ottenuti da globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="53c1f-115">The variable globalBuffer is a buffer that the pull procedure uses to send the blocks of data it obtains from globalPipeData.</span></span>

<span data-ttu-id="53c1f-116">La funzione SendLongs dichiara la pipe di input e alloca memoria per la variabile dell'origine dati globalPipeData.</span><span class="sxs-lookup"><span data-stu-id="53c1f-116">The SendLongs function declares the input pipe, and allocates memory for the data source variable globalPipeData.</span></span> <span data-ttu-id="53c1f-117">Nel programma client/server, l'origine dati può essere un file o una struttura creata dal client.</span><span class="sxs-lookup"><span data-stu-id="53c1f-117">In your client/server program, the data source can be a file or structure that the client creates.</span></span> <span data-ttu-id="53c1f-118">È anche possibile fare in modo che il programma client ottenga dati dal server, li elabori e li restituisca al server usando una pipe di input.</span><span class="sxs-lookup"><span data-stu-id="53c1f-118">You can also have your client program obtain data from the server, process it, and return it to the server using an input pipe.</span></span> <span data-ttu-id="53c1f-119">In questo semplice esempio l'origine dati è un buffer allocato in modo dinamico di valori long integer.</span><span class="sxs-lookup"><span data-stu-id="53c1f-119">In this simple example, the data source is a dynamically allocated buffer of long integers.</span></span>

<span data-ttu-id="53c1f-120">Prima che il trasferimento possa iniziare, il client deve impostare i puntatori sulla variabile di stato, sulla procedura pull e sulla procedura di allocazione.</span><span class="sxs-lookup"><span data-stu-id="53c1f-120">Before the transfer can begin, the client must set pointers to the state variable, the pull procedure, and the alloc procedure.</span></span> <span data-ttu-id="53c1f-121">Questi puntatori vengono conservati nella variabile pipe dichiarata dal client.</span><span class="sxs-lookup"><span data-stu-id="53c1f-121">These pointers are kept in the pipe variable the client declares.</span></span> <span data-ttu-id="53c1f-122">In questo caso, SendLongs dichiara inpipe.</span><span class="sxs-lookup"><span data-stu-id="53c1f-122">In this case, SendLongs declares inPipe.</span></span> <span data-ttu-id="53c1f-123">È possibile utilizzare qualsiasi tipo di dati appropriato per la variabile di stato.</span><span class="sxs-lookup"><span data-stu-id="53c1f-123">You can use any appropriate data type for your state variable.</span></span>

<span data-ttu-id="53c1f-124">I client avviano i trasferimenti di dati attraverso una pipe richiamando una procedura remota sul server.</span><span class="sxs-lookup"><span data-stu-id="53c1f-124">Clients initiate data transfers across a pipe by invoking a remote procedure on the server.</span></span> <span data-ttu-id="53c1f-125">La chiamata della procedura remota indica al programma server che il client è pronto per la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="53c1f-125">Calling the remote procedure tells the server program that the client is ready to transmit.</span></span> <span data-ttu-id="53c1f-126">Il server può quindi effettuare il pull dei dati a se stesso.</span><span class="sxs-lookup"><span data-stu-id="53c1f-126">The server can then pull the data to itself.</span></span> <span data-ttu-id="53c1f-127">In questo esempio viene richiamata una procedura remota denominata inpipe.</span><span class="sxs-lookup"><span data-stu-id="53c1f-127">This example invokes a remote procedure called InPipe.</span></span> <span data-ttu-id="53c1f-128">Una volta trasferiti i dati al server, la funzione SendLongs libera il buffer allocato in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="53c1f-128">After the data is transferred to the server, the SendLongs function frees the dynamically allocated buffer.</span></span>

<span data-ttu-id="53c1f-129">Anziché allocare memoria ogni volta che è necessario un buffer.</span><span class="sxs-lookup"><span data-stu-id="53c1f-129">Rather than allocate memory each time a buffer is needed.</span></span> <span data-ttu-id="53c1f-130">la procedura di allocazione in questo esempio imposta semplicemente un puntatore sulla variabile globalBuffer.</span><span class="sxs-lookup"><span data-stu-id="53c1f-130">the alloc procedure in this example simply sets a pointer to the variable globalBuffer.</span></span> <span data-ttu-id="53c1f-131">La procedura pull riutilizza questo buffer ogni volta che trasferisce i dati.</span><span class="sxs-lookup"><span data-stu-id="53c1f-131">The pull procedure reuses this buffer each time it transfers data.</span></span> <span data-ttu-id="53c1f-132">Per i programmi client più complessi potrebbe essere necessario allocare un nuovo buffer ogni volta che il server estrae i dati dal client.</span><span class="sxs-lookup"><span data-stu-id="53c1f-132">More complex client programs may need to allocate a new buffer each time the server pulls data from the client.</span></span>

<span data-ttu-id="53c1f-133">Lo stub client chiama la procedura pull.</span><span class="sxs-lookup"><span data-stu-id="53c1f-133">The client stub calls the pull procedure.</span></span> <span data-ttu-id="53c1f-134">La procedura pull in questo esempio usa la variabile di stato per tenere traccia della posizione successiva nel buffer dell'origine dati globale da cui leggere.</span><span class="sxs-lookup"><span data-stu-id="53c1f-134">The pull procedure in this example uses the state variable to track the next position in the global data source buffer to read from.</span></span> <span data-ttu-id="53c1f-135">Legge i dati dal buffer di origine nel buffer di pipe.</span><span class="sxs-lookup"><span data-stu-id="53c1f-135">It reads data from the source buffer into the pipe buffer.</span></span> <span data-ttu-id="53c1f-136">Lo stub client trasmette i dati al server.</span><span class="sxs-lookup"><span data-stu-id="53c1f-136">The client stub transmits the data to the server.</span></span> <span data-ttu-id="53c1f-137">Quando tutti i dati sono stati inviati, la procedura pull imposta la dimensione del buffer su zero.</span><span class="sxs-lookup"><span data-stu-id="53c1f-137">When all the data has been sent, the pull procedure sets the buffer size to zero.</span></span> <span data-ttu-id="53c1f-138">In questo modo si indica al server di arrestare il pull dei dati.</span><span class="sxs-lookup"><span data-stu-id="53c1f-138">This tells the server to stop pulling data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53c1f-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53c1f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c1f-140">inviare tramite pipe</span><span class="sxs-lookup"><span data-stu-id="53c1f-140">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="53c1f-141">**/OI**</span><span class="sxs-lookup"><span data-stu-id="53c1f-141">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 