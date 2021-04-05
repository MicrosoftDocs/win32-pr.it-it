---
description: Una named pipe è una pipe denominata, unidirezionale o duplex per la comunicazione tra il server pipe e uno o più client pipe.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Named Pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967640"
---
# <a name="named-pipes"></a>Named Pipe

Una *named pipe* è una pipe denominata, unidirezionale o duplex per la comunicazione tra il server pipe e uno o più client pipe. Tutte le istanze di un named pipe condividono lo stesso nome di pipe, ma ogni istanza ha i propri buffer e handle e fornisce un canale separato per la comunicazione client/server. L'utilizzo delle istanze consente a più client pipe di utilizzare contemporaneamente lo stesso named pipe.

Qualsiasi processo può accedere a named pipe, in base ai controlli di sicurezza, rendendo le named pipe una semplice forma di comunicazione tra processi correlati o non correlati.

Qualsiasi processo può fungere sia da server che da client, rendendo possibile la comunicazione peer-to-peer. Come usato in questo caso, il termine pipe server fa riferimento a un processo che crea un named pipe e il termine client pipe fa riferimento a un processo che si connette a un'istanza di un named pipe. La funzione lato server per la creazione di un'istanza di un named pipe è [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). La funzione lato server per l'accettazione di una connessione è [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe). Un processo client si connette a un named pipe tramite la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .

È possibile utilizzare le named pipe per fornire la comunicazione tra processi nello stesso computer o tra processi in computer diversi in una rete. Se il servizio Server è in esecuzione, tutte le named pipe sono accessibili in remoto. Se si intende utilizzare un named pipe solo localmente, negare l'accesso alla rete NT AUTHORITY \\ o passare alla RPC locale.

Per altre informazioni, vedere i seguenti argomenti:

-   [Nomi pipe](pipe-names.md)
-   [Modalità di apertura named pipe](named-pipe-open-modes.md)
-   [Tipo di named pipe, modalità lettura e attesa](named-pipe-type-read-and-wait-modes.md)
-   [Istanze named pipe](named-pipe-instances.md)
-   [Operazioni named pipe](named-pipe-operations.md)
-   [Input e output sincroni e sovrapposti](synchronous-and-overlapped-input-and-output.md)
-   [Diritti di accesso e sicurezza della named pipe](named-pipe-security-and-access-rights.md)
-   [Rappresentazione di un client named pipe](impersonating-a-named-pipe-client.md)
-   [Uso di pipe](using-pipes.md)

 

 
