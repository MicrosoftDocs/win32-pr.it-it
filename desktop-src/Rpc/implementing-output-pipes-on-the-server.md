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
# <a name="implementing-output-pipes-on-the-server"></a>Implementazione di pipe di output nel server

Per iniziare a ricevere dati da un server, un client chiama una delle procedure remote del server. Questa procedura deve chiamare ripetutamente la procedura push nello stub del server. Il compilatore MIDL usa il file IDL dell'applicazione per generare automaticamente la procedura push del server.

La routine del server remoto deve riempire il buffer della pipe di output con i dati prima di chiamare la procedura di push. Ogni volta che il programma server richiama la procedura push nello stub, la procedura push esegue il marshalling dei dati e li trasmette al client. Il ciclo continua fino a quando il server non invia un buffer di lunghezza zero.

Nell'esempio seguente viene utilizzato il programma Pipedemo contenuto negli esempi forniti con il Windows SDK. Viene illustrata una procedura server remota che utilizza una pipe per eseguire il push dei dati dal server al client.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[inviare tramite pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/OI**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 