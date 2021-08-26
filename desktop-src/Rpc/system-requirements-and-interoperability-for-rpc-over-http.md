---
title: Requisiti di sistema rpc su HTTP, interoperabilità
description: Rpc Microsoft supporta RPC su HTTP, come illustrato nella tabella seguente.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc9019789821499168a76d4d2e02ef485529e08b99c5f0759a19bfb4a46f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017311"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Requisiti di sistema rpc su HTTP, interoperabilità

Rpc Microsoft supporta RPC su HTTP, come illustrato nella tabella seguente.



| Piattaforma                             | Supporti                       | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Client, server e proxy RPC | Supporta RPC su HTTP v1 e RPC su client e server HTTP v2. Il proxy RPC supporta RPC su HTTP v2 quando IIS è in esecuzione in modalità IIS 6.0. Il proxy RPC supporta RPC su HTTP v1 e RPC su HTTP v2 quando IIS è in esecuzione in modalità IIS 5.0. Tuttavia, l'esecuzione in modalità IIS 5.0 non è consigliata. Per [altre informazioni, vedere Consigli](rpc-over-http-deployment-recommendations.md) distribuzione RPC su HTTP. IL server RPC su HTTP e il proxy RPC possono essere in computer diversi. |
| Windows XP con Service Pack 1 (SP1) | Client e server            | Supporta RPC su HTTP v1 e RPC su client e server HTTP v2. Non supporta il proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Client e server            | Supporta solo client e server RPC su HTTP v1. Non supporta il proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Client, server e proxy RPC | Il programma server RPC su HTTP e il proxy RPC possono essere in esecuzione in computer diversi. RPC su client HTTP, server e proxy RPC supportano RPC solo su HTTP v1.                                                                                                                                                                                                                                                                                                                   |



 

Si applicano anche i requisiti seguenti:

-   Windows 2000 e versioni successive richiede l'uso di IIS 4.0 o versione successiva.
-   Il proxy RPC su HTTP viene eseguito solo Windows server.
-   Se IIS è in esecuzione in una versione server di Windows, il programma server RPC su HTTP può essere eseguito in qualsiasi computer in cui il proxy RPC è configurato per inoltrare il traffico. Pertanto, può essere eseguito nello stesso computer del proxy RPC o in un computer diverso.

Per stabilire una connessione RPC su HTTP, tutti i client RPC su HTTP, IL server RPC su HTTP e il proxy RPC devono accettare la versione di RPC su HTTP usata. Se non esiste una versione comune di RPC su HTTP supportata da tutti e tre (client, server e proxy RPC), non è possibile stabilire una connessione RPC su HTTP. La tabella seguente riepiloga questa interoperabilità per le diverse versioni di RPC su HTTP.



| Client RPC su HTTP | RPC Proxy      | RPC su server HTTP | Funziona?                                      | Versione usata     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| Solo v1              | Solo v1        | Solo v1              | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Solo v1              | Solo v1        | Sia v1 che v2       | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Solo v1              | Sia v1 che v2 | Solo v1              | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Solo v1              | Sia v1 che v2 | Sia v1 che v2       | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Solo v1              | Solo v2        | Solo v1              | No                                          |                  |
| Solo v1              | Solo v2        | Sia v1 che v2       | No                                          |                  |
| Sia v1 che v2       | Solo v1        | Solo v1              | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Sia v1 che v2       | Solo v1        | Sia v1 che v2       | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Sia v1 che v2       | Sia v1 che v2 | Solo v1              | Sì, con limitazioni v1                    | RPC su HTTP v1 |
| Sia v1 che v2       | Sia v1 che v2 | Sia v1 che v2       | Sì                                         | RPC su HTTP v2 |
| Sia v1 che v2       | Solo v2        | Solo v1              | No                                          |                  |
| Sia v1 che v2       | Solo v2        | Sia v1 che v2       | Sì. Si tratta della configurazione consigliata. | RPC su HTTP v2 |



 

Si supponga ad esempio un client Windows 2000, un proxy Windows Server 2003 con IIS in esecuzione in modalità IIS 6.0 e un Windows Server 2003 RPC su server HTTP. La prima tabella in questa pagina di riferimento mostra che Windows 2000 supporta solo RPC su HTTP v1. La stessa tabella rivela che un Windows Server 2003 con IIS in esecuzione in modalità IIS 6.0 supporta solo RPC su HTTP v2 e che un server RPC su HTTP di Windows Server 2003 supporta sia RPC su HTTP v1 che RPC su HTTP v2. Questo scenario è descritto nella riga 6 della seconda tabella di questa pagina di riferimento, in cui indica che non è possibile stabilire una connessione RPC su HTTP. Inoltre, la seconda tabella rivela che esistono due opzioni per questo scenario:

-   Se la sicurezza e l'affidabilità non sono da considerare, IIS può passare alla modalità IIS 5.0 in cui supporta sia RPC su HTTP v1 che RPC su HTTP v2. In questo modo sarebbe possibile stabilire una connessione RPC su HTTP v1.
-   Aggiornare il client Windows 98 a Windows XP con SP1 e ottenere la potenza, la sicurezza e l'affidabilità di una connessione RPC su HTTP v2.

 

 




