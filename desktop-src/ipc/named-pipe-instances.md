---
description: Strategie per la comunicazione con più client pipe e la manutenzione di più istanze pipe.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Istanze di named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 188ec90912132e5cdd972ac2b0a4ab3f4c1f97ebbb7bc35e20b75b04eebbfa15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481962"
---
# <a name="named-pipe-instances"></a>Istanze di named pipe

Il server pipe più semplice crea una singola istanza di una pipe, si connette a un singolo client, comunica con il client, si disconnette dal client, chiude l'handle della pipe e termina. Tuttavia, è più comune per un server pipe comunicare con più client pipe. Un server pipe potrebbe usare una singola istanza pipe per connettersi a più client pipe connettendosi e disconnettendosi da ogni client in sequenza, ma le prestazioni sarebbero scarse. Il server pipe deve creare più istanze pipe per gestire in modo efficiente più client contemporaneamente.

Esistono tre strategie di base per la manutenzione di più istanze di pipe.

-   Creare un thread separato per ogni istanza della pipe. Per un esempio di server pipe multithreading, vedere Server pipe [multithreading](multithreaded-pipe-server.md).
-   Usare operazioni sovrapposte specificando una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) nelle [**funzioni ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) Per un esempio, vedere [Server named pipe con I/O sovrapposto.](named-pipe-server-using-overlapped-i-o.md)
-   Usare operazioni sovrapposte usando le [**funzioni ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx,**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) che specificano una routine di completamento da eseguire al termine dell'operazione. Per un esempio, vedere [Server named pipe con routine di completamento](named-pipe-server-using-completion-routines.md).

Il server pipe multithreading è più semplice da scrivere, perché il thread per ogni istanza gestisce le comunicazioni per un singolo client pipe. Il sistema alloca il tempo del processore a ogni thread in base alle esigenze. Ogni thread usa tuttavia le risorse di sistema, uno svantaggio per un server pipe che gestisce un numero elevato di client.

Con un server a thread singolo, è più semplice coordinare le operazioni che interessano più client ed è più semplice proteggere le risorse condivise dall'accesso simultaneo da più client. La sfida di un server a thread singolo è che richiede il coordinamento delle operazioni sovrapposte per allocare il tempo del processore per gestire le esigenze simultanee dei client.

 

 
