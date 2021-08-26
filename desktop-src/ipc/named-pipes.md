---
description: Un named pipe è una pipe denominata, unidirezionale o duplex per la comunicazione tra il server pipe e uno o più client pipe.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Named Pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06e7f291776e2ecba3b9da93a94d235d4fbe7df151353a7c3d379eb4d50fdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014901"
---
# <a name="named-pipes"></a>Named Pipe

Un *named pipe* è una pipe denominata, unidirezionale o duplex per la comunicazione tra il server pipe e uno o più client pipe. Tutte le istanze di un named pipe condividono lo stesso nome di pipe, ma ogni istanza ha i propri buffer e handle e fornisce un canale separato per la comunicazione client/server. L'uso di istanze consente a più client pipe di usare lo stesso named pipe contemporaneamente.

Qualsiasi processo può accedere alle named pipe, soggette a controlli di sicurezza, rendendo le named pipe una semplice forma di comunicazione tra processi correlati o non correlati.

Qualsiasi processo può fungere sia da server che da client, rendendo possibile la comunicazione peer-to-peer. Come usato in questo caso, il termine server pipe si riferisce a un processo che crea un named pipe e il termine client pipe fa riferimento a un processo che si connette a un'istanza di un named pipe. La funzione lato server per creare un'istanza di un named pipe è [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). La funzione lato server per accettare una connessione è [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe). Un processo client si connette a un named pipe usando la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**o CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)

Le named pipe possono essere usate per fornire la comunicazione tra processi nello stesso computer o tra processi in computer diversi in una rete. Se il servizio server è in esecuzione, tutte le named pipe sono accessibili in modalità remota. Se si prevede di usare un named pipe solo localmente, negare l'accesso a NT AUTHORITY \\ NETWORK o passare a RPC locale.

Per altre informazioni, vedere i seguenti argomenti:

-   [Nomi di pipe](pipe-names.md)
-   [Modalità di apertura named pipe](named-pipe-open-modes.md)
-   [Modalità di attesa, lettura e tipo di named pipe](named-pipe-type-read-and-wait-modes.md)
-   [Istanze di named pipe](named-pipe-instances.md)
-   [Operazioni named pipe](named-pipe-operations.md)
-   [Input e output sincroni e sovrapposti](synchronous-and-overlapped-input-and-output.md)
-   [Sicurezza e diritti di accesso delle named pipe](named-pipe-security-and-access-rights.md)
-   [Rappresentazione di un client named pipe](impersonating-a-named-pipe-client.md)
-   [Uso di pipe](using-pipes.md)

 

 
