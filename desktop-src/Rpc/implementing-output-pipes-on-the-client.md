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
# <a name="implementing-output-pipes-on-the-client"></a>Implementazione di pipe di output nel client

Quando si usa una pipe di output per trasferire i dati dal server al client, è necessario implementare una procedura push nel client. La procedura push accetta un puntatore a un buffer e un numero di elementi dallo stub client e, se il conteggio degli elementi è maggiore di 0, elabora i dati. Ad esempio, è possibile copiare i dati dal buffer dello stub alla propria memoria. In alternativa, è possibile elaborare i dati nel buffer dello stub e salvarli in un file. Quando il numero di elementi è uguale a zero, la procedura push completa tutte le attività di pulizia necessarie prima di restituire.

Nell'esempio seguente la funzione client ReceiveLongs alloca una struttura di pipe e un buffer di memoria globale. Inizializza la struttura, effettua la chiamata di procedura remota e quindi libera la memoria.

## <a name="example"></a>Esempio


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



Questo esempio include il file di intestazione generato dal compilatore MIDL. Per informazioni dettagliate, vedere [definizione di pipe nel file IDL](defining-pipes-in-idl-files.md). Viene inoltre dichiarata una variabile, globalPipeData, che utilizza come sink di dati. La variabile globalBuffer è un buffer usato dalla procedura push per ricevere i blocchi di dati archiviati in globalPipeData.

La funzione ReceiveLongs dichiara una pipe e alloca lo spazio di memoria per la variabile globale di sink di dati. Nel programma client/server, il sink dei dati può essere un file o una struttura di dati creato dal client. In questo semplice esempio l'origine dati è un buffer allocato in modo dinamico di valori long integer.

Prima di poter iniziare il trasferimento dei dati, è necessario che il programma client Inizializza la struttura della pipe di output. È necessario impostare i puntatori sulla variabile di stato, sulla procedura di push e sulla procedura di allocazione. In questo esempio, la variabile di pipe di output è denominata outputPipe.

I client segnalano i server che sono pronti a ricevere i dati richiamando una procedura remota sul server. In questo esempio, la procedura remota viene chiamata outpipe. Quando il client chiama la procedura remota, il server avvia il trasferimento dei dati. Ogni volta che arrivano i dati, lo stub client chiama le procedure di allocazione e push del client secondo necessità.

Anziché allocare memoria ogni volta che è necessario un buffer, la procedura di allocazione in questo esempio imposta semplicemente un puntatore sulla variabile globalBuffer. La procedura pull riutilizza quindi questo buffer ogni volta che trasferisce i dati. Per i programmi client più complessi potrebbe essere necessario allocare un nuovo buffer ogni volta che il server estrae i dati dal client.

La procedura push in questo esempio usa la variabile di stato per tenere traccia della posizione successiva in cui archivia i dati nel buffer di sink di dati globali. Scrive i dati dal buffer della pipe nel buffer di sink. Lo stub del client riceve quindi il blocco di dati successivo dal server e lo archivia nel buffer della pipe. Quando tutti i dati sono stati inviati, il server trasmette un buffer di dimensioni zero. Viene così indicata la procedura push per arrestare la ricezione dei dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[inviare tramite pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 