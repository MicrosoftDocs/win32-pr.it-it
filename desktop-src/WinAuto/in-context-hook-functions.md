---
title: In-Context Funzioni Hook
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Altre informazioni su: In-Context Hook Functions'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbeb6340642d63700901d9306aea5dca20b26ce46790d900e26e42875571379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565562"
---
# <a name="in-context-hook-functions"></a>In-Context Funzioni Hook

L'elenco seguente illustra gli aspetti chiave delle funzioni hook nel contesto:

-   Le funzioni hook nel contesto devono trovarsi in una libreria a collegamento dinamico (DLL) mappata dal sistema nello spazio indirizzi del server.
-   Le funzioni hook nel contesto condividono lo spazio indirizzi con il server.
-   Quando il server attiva un evento, il sistema chiama una funzione hook senza effettuare il marshalling (creazione di pacchetti e invio di parametri di interfaccia tra i limiti del processo).
-   Le funzioni hook nel contesto tendono a essere molto veloci e ricevono notifiche degli eventi in modo sincrono perché non è presente alcun marshalling.
-   Alcuni eventi possono essere recapitati out-of-process, anche se si richiede che siano recapitati in-process (usando il \_ flag WINEVENT INCONTEXT). Questa situazione può verificarsi con problemi di interoperabilità delle applicazioni a 64 e 32 bit e con Windows eventi della console.

 

 




