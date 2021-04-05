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
# <a name="implementing-input-pipes-on-the-client"></a>Implementazione di pipe di input nel client

Quando si utilizza una pipe di input per trasferire i dati dal client al server, è necessario implementare una procedura pull. La procedura pull deve trovare i dati da trasferire, leggere i dati nel buffer e impostare il numero di elementi da inviare. Non tutti i dati devono trovarsi nel buffer quando il server inizia a eseguire il pull dei dati a se stesso. La procedura pull può riempire il buffer in modo incrementale.

Quando non sono più presenti dati da inviare, la routine imposta l'ultimo argomento su zero. Quando vengono inviati tutti i dati, la procedura pull deve eseguire tutte le operazioni di pulizia necessarie prima di restituire. Per un parametro che è un \[ in, out \] pipe, la procedura pull deve reimpostare la variabile di stato del client dopo che tutti i dati sono stati trasmessi, in modo che la procedura push possa usarla per ricevere i dati.

L'esempio seguente viene estratto dal programma Pipedemo incluso nel Software Development Kit (SDK) della piattaforma.


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



Questo esempio include il file di intestazione generato dal compilatore MIDL. Per informazioni dettagliate, vedere [definizione di pipe nei file IDL](defining-pipes-in-idl-files.md). Viene inoltre dichiarata una variabile utilizzata come origine dati denominata globalPipeData. La variabile globalBuffer è un buffer usato dalla procedura pull per inviare i blocchi di dati ottenuti da globalPipeData.

La funzione SendLongs dichiara la pipe di input e alloca memoria per la variabile dell'origine dati globalPipeData. Nel programma client/server, l'origine dati può essere un file o una struttura creata dal client. È anche possibile fare in modo che il programma client ottenga dati dal server, li elabori e li restituisca al server usando una pipe di input. In questo semplice esempio l'origine dati è un buffer allocato in modo dinamico di valori long integer.

Prima che il trasferimento possa iniziare, il client deve impostare i puntatori sulla variabile di stato, sulla procedura pull e sulla procedura di allocazione. Questi puntatori vengono conservati nella variabile pipe dichiarata dal client. In questo caso, SendLongs dichiara inpipe. È possibile utilizzare qualsiasi tipo di dati appropriato per la variabile di stato.

I client avviano i trasferimenti di dati attraverso una pipe richiamando una procedura remota sul server. La chiamata della procedura remota indica al programma server che il client è pronto per la trasmissione. Il server può quindi effettuare il pull dei dati a se stesso. In questo esempio viene richiamata una procedura remota denominata inpipe. Una volta trasferiti i dati al server, la funzione SendLongs libera il buffer allocato in modo dinamico.

Anziché allocare memoria ogni volta che è necessario un buffer. la procedura di allocazione in questo esempio imposta semplicemente un puntatore sulla variabile globalBuffer. La procedura pull riutilizza questo buffer ogni volta che trasferisce i dati. Per i programmi client più complessi potrebbe essere necessario allocare un nuovo buffer ogni volta che il server estrae i dati dal client.

Lo stub client chiama la procedura pull. La procedura pull in questo esempio usa la variabile di stato per tenere traccia della posizione successiva nel buffer dell'origine dati globale da cui leggere. Legge i dati dal buffer di origine nel buffer di pipe. Lo stub client trasmette i dati al server. Quando tutti i dati sono stati inviati, la procedura pull imposta la dimensione del buffer su zero. In questo modo si indica al server di arrestare il pull dei dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[inviare tramite pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 