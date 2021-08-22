---
title: Funzioni hook out-of-context
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Altre informazioni su: Funzioni hook out-of-context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e41e9a6bba1f705c3c5dc8781b2663be22086955f5dee45f07022504d0ccbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133744"
---
# <a name="out-of-context-hook-functions"></a>Funzioni hook out-of-context

L'elenco seguente illustra gli aspetti chiave delle funzioni hook out-of-context:

-   Le funzioni hook out-of-context si trovano nello spazio degli indirizzi del client, sia nel corpo del codice che in una DLL.
-   Le funzioni hook out-of-context non vengono mappate nello spazio degli indirizzi del server.
-   Quando viene attivato un evento, viene effettuato il marshalling dei parametri per la funzione hook attraverso i limiti del processo.
-   Le funzioni hook out-of-context sono notevolmente più lente rispetto alle funzioni hook nel contesto a causa del marshalling.
-   Il sistema accoda le notifiche degli eventi in modo che arrivino in modo asincrono (a causa del tempo necessario per eseguire il marshalling).

Anche se le notifiche degli eventi sono asincrone, Microsoft Active Accessibility garantisce che la funzione di callback riceva tutti gli eventi nell'ordine in cui vengono generati.

Il componente USER del sistema operativo alloca memoria per gli eventi gestiti dalle funzioni hook fuori contesto. La memoria viene liberata quando vengono restituite le funzioni hook. Se una funzione hook non elabora gli eventi abbastanza rapidamente, le risorse UTENTE vengono abbassate, causando un errore o tempi di risposta estremamente lenti. Questi problemi possono verificarsi se:

-   Gli eventi vengono generati molto rapidamente.
-   Il sistema è lento.
-   La funzione hook elabora lentamente gli eventi.
-   Il client è in esecuzione Windows 9x.

 

 




