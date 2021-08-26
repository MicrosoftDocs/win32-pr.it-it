---
title: Implementazione di pipe di input nel server
description: Per iniziare a inviare dati a un server, un client chiama una delle procedure remote del server.
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf133fce019328b9fa7d6b2a03e47d516de5ca74310d611ecea1686c0b9a3a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020521"
---
# <a name="implementing-input-pipes-on-the-server"></a>Implementazione di pipe di input nel server

Per iniziare a inviare dati a un server, un client chiama una delle procedure remote del server. Questa procedura deve chiamare ripetutamente la procedura pull nello stub del server. Il compilatore MIDL usa il file IDL dell'applicazione per generare automaticamente la procedura pull del server.

Ogni volta che il programma server richiama la procedura pull nello stub, la procedura pull riceve blocchi di dati dal client. Annulla ilmarshaling dei dati nel buffer del server. La procedura remota del server può quindi elaborare questi dati in qualsiasi modo necessario. Il ciclo continua fino a quando il server non riceve un buffer di lunghezza zero.

L'esempio seguente deriva dal programma Pipedemo contenuto negli esempi forniti con Platform Software Development Kit (SDK). Viene illustrata una procedura del server remoto che usa una pipe per eseguire il pull dei dati dal client al server.

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

 

 




