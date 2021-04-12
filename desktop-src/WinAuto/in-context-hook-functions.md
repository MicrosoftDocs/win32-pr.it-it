---
title: Funzioni hook In-Context
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Altre informazioni su: funzioni hook In-Context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233997"
---
# <a name="in-context-hook-functions"></a>Funzioni hook In-Context

Nell'elenco seguente vengono descritti gli aspetti chiave delle funzioni hook nel contesto:

-   Le funzioni hook nel contesto devono trovarsi in una libreria di collegamento dinamico (DLL) di cui il sistema esegue il mapping nello spazio degli indirizzi del server.
-   Le funzioni hook nel contesto condividono lo spazio degli indirizzi con il server.
-   Quando il server attiva un evento, il sistema chiama una funzione hook senza marshalling (creazione di pacchetti e invio di parametri di interfaccia tra i limiti del processo).
-   Le funzioni hook nel contesto tendono a essere molto veloci e a ricevere notifiche di eventi in modo sincrono perché non è presente alcun marshalling.
-   Alcuni eventi possono essere recapitati out-of-process, anche se si richiede che vengano recapitati in-process (usando il \_ flag INCONTEXT WINEVENT). Questa situazione può verificarsi con problemi di interoperabilità delle applicazioni a 64 bit e a 32 bit e con eventi della console di Windows.

 

 




