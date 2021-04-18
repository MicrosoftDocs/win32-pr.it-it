---
description: Strategie per la comunicazione con più client pipe e la manutenzione di più istanze di pipe.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Istanze named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b7d1ec591996e83853ae6faede899ecd4e4ea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315599"
---
# <a name="named-pipe-instances"></a>Istanze named pipe

Il server pipe più semplice crea una singola istanza di una pipe, si connette a un singolo client, comunica con il client, si disconnette dal client, chiude l'handle della pipe e termina. Tuttavia, è più comune che un server pipe comunichi con più client pipe. Un server pipe può utilizzare una singola istanza di pipe per connettersi a più client pipe connettendosi a e disconnettendosi da ogni client in sequenza, ma le prestazioni potrebbero essere insufficienti. Il server pipe deve creare più istanze di pipe per gestire in modo efficiente più client simultaneamente.

Sono disponibili tre strategie di base per la manutenzione di più istanze di pipe.

-   Creare un thread separato per ogni istanza della pipe. Per un esempio di server pipe multithreading, vedere [server pipe multithreading](multithreaded-pipe-server.md).
-   Utilizzare operazioni sovrapposte specificando una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) nelle funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Per un esempio, vedere [named pipe server con I/O sovrapposti](named-pipe-server-using-overlapped-i-o.md).
-   Usare le operazioni sovrapposte usando le funzioni [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) , che specificano una routine di completamento da eseguire al termine dell'operazione. Per un esempio, vedere [named pipe server usando le routine di completamento](named-pipe-server-using-completion-routines.md).

Il server pipe multithreading è più facile da scrivere, perché il thread per ogni istanza gestisce le comunicazioni per un singolo client pipe. Il sistema alloca il tempo del processore a ogni thread in base alle esigenze. Tuttavia, ogni thread utilizza risorse di sistema, uno svantaggio per un server pipe che gestisce un numero elevato di client.

Con un server a thread singolo, è più semplice coordinare le operazioni che interessano più client ed è più facile proteggere le risorse condivise dall'accesso simultaneo da parte di più client. La sfida di un server a thread singolo è la necessità di coordinare le operazioni sovrapposte per allocazione del tempo del processore per la gestione delle esigenze simultanee dei client.

 

 
