---
title: Requisiti di sistema RPC su HTTP, interoperabilità
description: Microsoft RPC supporta RPC su HTTP, come illustrato nella tabella seguente.
ms.assetid: 1815315c-1286-4e60-b3a2-a02cb3016fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880f078ea481be59448612b5024bbec4d2f54fa5
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104046156"
---
# <a name="rpc-over-http-system-requirements-interoperability"></a>Requisiti di sistema RPC su HTTP, interoperabilità

Microsoft RPC supporta RPC su HTTP, come illustrato nella tabella seguente.



| Piattaforma                             | Supporti                       | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Server 2003                  | Client, server e proxy RPC | Supporta RPC su HTTP V1 e RPC su HTTP v2 client e server. Il proxy RPC supporta RPC su HTTP v2 Quando IIS viene eseguito in modalità IIS 6,0. Il proxy RPC supporta RPC su HTTP V1 e RPC su HTTP v2 Quando IIS viene eseguito in modalità IIS 5,0. Tuttavia, l'esecuzione in modalità IIS 5,0 non è consigliata. Per ulteriori informazioni, vedere la pagina relativa ai [consigli sulla distribuzione RPC su http](rpc-over-http-deployment-recommendations.md) . Il server RPC su HTTP e il proxy RPC possono trovarsi in computer diversi. |
| Windows XP con Service Pack 1 (SP1) | Client e server            | Supporta RPC su HTTP V1 e RPC su HTTP v2 client e server. Non supporta il proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows XP                           | Client e server            | Supporta solo RPC su HTTP V1 client e server. Non supporta il proxy RPC.                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows 2000                         | Client, server e proxy RPC | Il programma server RPC su HTTP e il proxy RPC possono essere eseguiti in computer diversi. Il client RPC su HTTP, il server e il proxy RPC supportano solo RPC su HTTP V1.                                                                                                                                                                                                                                                                                                                   |



 

Inoltre, si applicano i requisiti seguenti:

-   Windows 2000 e versioni successive richiedono l'uso di IIS 4,0 o versione successiva.
-   Il proxy RPC su HTTP viene eseguito solo nelle edizioni di Windows Server.
-   Se IIS viene eseguito in una versione server di Windows, il programma server RPC su HTTP può essere eseguito in qualsiasi computer in cui è configurato il proxy RPC per l'inoltro del traffico. Pertanto, può essere eseguito sullo stesso computer del proxy RPC o su un computer diverso.

Per stabilire una connessione RPC su HTTP, è necessario che il client RPC su http, il server RPC su HTTP e il proxy RPC accettino la versione di RPC su HTTP. Se non è presente alcuna versione comune di RPC su HTTP che tutti e tre supportano (client, server e proxy RPC), non è possibile stabilire una connessione RPC su HTTP. Nella tabella seguente viene riepilogata questa interoperabilità per versioni diverse di RPC su HTTP.



| Client RPC su HTTP | Proxy RPC      | Server RPC su HTTP | Funziona?                                      | Versione utilizzata     |
|----------------------|----------------|----------------------|---------------------------------------------|------------------|
| solo V1              | solo V1        | solo V1              | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| solo V1              | solo V1        | Sia V1 che v2       | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| solo V1              | Sia V1 che v2 | solo V1              | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| solo V1              | Sia V1 che v2 | Sia V1 che v2       | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| solo V1              | solo V2        | solo V1              | No                                          |                  |
| solo V1              | solo V2        | Sia V1 che v2       | No                                          |                  |
| Sia V1 che v2       | solo V1        | solo V1              | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| Sia V1 che v2       | solo V1        | Sia V1 che v2       | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| Sia V1 che v2       | Sia V1 che v2 | solo V1              | Sì, con limitazioni V1                    | RPC su HTTP V1 |
| Sia V1 che v2       | Sia V1 che v2 | Sia V1 che v2       | Sì                                         | RPC su HTTP V2 |
| Sia V1 che v2       | solo V2        | solo V1              | No                                          |                  |
| Sia V1 che v2       | solo V2        | Sia V1 che v2       | Sì. Si tratta della configurazione consigliata. | RPC su HTTP V2 |



 

Si supponga, ad esempio, un client Windows 2000, un proxy di Windows Server 2003 con IIS in esecuzione in modalità IIS 6,0 e un server Windows Server 2003 RPC su HTTP. Nella prima tabella di questa pagina di riferimento viene indicato che Windows 2000 supporta solo RPC su HTTP V1. La stessa tabella rivela che Windows Server 2003 con IIS in esecuzione in modalità IIS 6,0 supporta solo RPC su HTTP V2 e che un server RPC su HTTP di Windows Server 2003 supporta sia RPC su HTTP V1 che RPC su http V2. Questo scenario è descritto nella riga 6 della seconda tabella di questa pagina di riferimento, in cui viene indicato che non è possibile stabilire una connessione RPC su HTTP. Inoltre, la seconda tabella rivela che esistono due scelte per lo scenario:

-   Se non si tiene conto della sicurezza e della robustezza, è possibile passare alla modalità IIS 5,0, in cui è supportata la RPC su HTTP V1 e RPC su HTTP V2. Questa operazione consente di stabilire una connessione RPC su HTTP V1.
-   Aggiornare il client Windows 98 a Windows XP con SP1 e ottenere la potenza, la sicurezza e l'affidabilità di una connessione RPC su HTTP V2.

 

 




