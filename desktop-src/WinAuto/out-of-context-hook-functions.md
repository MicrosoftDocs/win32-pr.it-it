---
title: Funzioni hook fuori contesto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Altre informazioni su: funzioni hook fuori contesto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883798"
---
# <a name="out-of-context-hook-functions"></a>Funzioni hook fuori contesto

Nell'elenco seguente vengono illustrati gli aspetti chiave delle funzioni hook fuori contesto:

-   Le funzioni hook fuori contesto si trovano nello spazio degli indirizzi del client, se si trova nel corpo del codice o in una DLL.
-   Non è stato eseguito il mapping delle funzioni hook out-of-Context nello spazio degli indirizzi del server.
-   Quando viene attivato un evento, i parametri per la funzione hook vengono sottoposti a marshalling tra i limiti del processo.
-   Le funzioni hook fuori contesto sono notevolmente più lente rispetto alle funzioni hook nel contesto a causa del marshalling.
-   Il sistema accoda le notifiche degli eventi in modo che arrivino in modo asincrono (a causa del tempo necessario per eseguire il marshalling).

Sebbene le notifiche degli eventi siano asincrone, Microsoft Active Accessibility garantisce che la funzione di callback riceva tutti gli eventi nell'ordine in cui vengono generati.

Il componente utente del sistema operativo alloca memoria per gli eventi gestiti da funzioni hook fuori contesto. La memoria viene liberata quando le funzioni hook restituiscono. Se una funzione hook non elabora gli eventi in modo sufficientemente rapido, le risorse utente vengono ridotte, causando un errore o tempi di risposta estremamente lenti. Questi problemi possono verificarsi se:

-   Gli eventi vengono generati molto rapidamente.
-   Il sistema è lento.
-   La funzione hook elabora gli eventi lentamente.
-   Il client è in esecuzione in Windows 9x.

 

 




