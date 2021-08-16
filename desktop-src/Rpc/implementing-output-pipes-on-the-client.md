---
title: Implementazione di pipe di output nel client
description: Quando si usa una pipe di output per trasferire i dati dal server al client, è necessario implementare una procedura push nel client.
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e959db9e505bb7dfe570552fe0385251485591fecb1f818ab4d5de402c2297b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929130"
---
# <a name="implementing-output-pipes-on-the-client"></a>Implementazione di pipe di output nel client

Quando si usa una pipe di output per trasferire i dati dal server al client, è necessario implementare una procedura push nel client. La procedura push accetta un puntatore a un buffer e un numero di elementi dallo stub client e, se il numero di elementi è maggiore di 0, elabora i dati. Ad esempio, potrebbe copiare i dati dal buffer dello stub nella propria memoria. In alternativa, potrebbe elaborare i dati nel buffer dello stub e salvarli in un file. Quando il numero di elementi è uguale a zero, la procedura push completa tutte le attività di pulizia necessarie prima della restituzione.

Nell'esempio seguente la funzione client ReceiveLongs alloca una struttura di pipe e un buffer di memoria globale. Inizializza la struttura , effettua la chiamata di procedura remota e quindi libera la memoria.

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



Questo esempio include il file di intestazione generato dal compilatore MIDL. Per informazioni [dettagliate, vedere Definizione di pipe nel file IDL.](defining-pipes-in-idl-files.md) Dichiara anche una variabile, globalPipeData, che usa come sink di dati. La variabile globalBuffer è un buffer utilizzato dalla procedura push per ricevere blocchi di dati archiviati in globalPipeData.

La funzione ReceiveLongs dichiara una pipe e alloca spazio di memoria per la variabile sink di dati globale. Nel programma client/server il sink di dati può essere un file o una struttura di dati creata dal client. In questo semplice esempio, l'origine dati è un buffer allocato dinamicamente di valori long integer.

Prima di iniziare il trasferimento dei dati, il programma client deve inizializzare la struttura della pipe di output. Deve impostare puntatori alla variabile di stato, alla procedura push e alla routine alloc. In questo esempio la variabile della pipe di output è denominata outputPipe.

I client segnalano ai server che sono pronti per ricevere dati richiamando una procedura remota sul server. In questo esempio la procedura remota è denominata OutPipe. Quando il client chiama la procedura remota, il server avvia il trasferimento dei dati. Ogni volta che arrivano i dati, lo stub client chiama le procedure di allocazione e push del client in base alle esigenze.

Anziché allocare memoria ogni volta che è necessario un buffer, la procedura di allocazione in questo esempio imposta semplicemente un puntatore alla variabile globalBuffer. La procedura pull riutilizza quindi questo buffer ogni volta che trasferisce i dati. I programmi client più complessi potrebbero dover allocare un nuovo buffer ogni volta che il server esegue il pull dei dati dal client.

La procedura push in questo esempio usa la variabile di stato per tenere traccia della posizione successiva in cui verranno archiviati i dati nel buffer del sink di dati globale. Scrive i dati dal buffer della pipe nel buffer sink. Lo stub client riceve quindi il blocco di dati successivo dal server e li archivia nel buffer della pipe. Dopo l'invio di tutti i dati, il server trasmette un buffer di dimensioni zero. In questo modo viene eseguita la procedura push per arrestare la ricezione dei dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[inviare tramite pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 