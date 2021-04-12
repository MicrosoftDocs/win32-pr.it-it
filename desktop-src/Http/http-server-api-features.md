---
title: Funzionalità dell'API del server HTTP
description: In questo argomento sono supportate e non supportate le funzionalità dell'API del server HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Funzionalità dell'API del server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331916"
---
# <a name="http-server-api-features"></a>Funzionalità dell'API del server HTTP

Negli elenchi seguenti vengono descritte le funzionalità supportate e non supportate dell'API del server HTTP.

## <a name="features-supported"></a>Funzionalità supportate

HTTP supporta le funzionalità seguenti:

-   Funzionalità server HTTP v 1.0 e v 1.1.
-   Secure Sockets Layer 3,0 (SSL) con supporto per i certificati client e server.
-   Memorizzazione nella cache dei frammenti di dati da utilizzare nelle risposte successive.
-   Supporto per indirizzi IPv6 e IPv4.
-   Prenotazioni degli spazi dei nomi URL per la sicurezza dell'applicazione.
-   Handle true per tutti gli oggetti.
-   Modelli I/O sincroni e asincroni.
-   Supporto per WOW64 in computer che eseguono Windows a 64 bit a partire da Windows Server 2003 con Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Funzionalità non supportate

L'API server HTTP non supporta le funzionalità seguenti:

-   L'API server HTTP non esegue l'autenticazione client o server in base al contenuto delle intestazioni della richiesta HTTP. Qualsiasi autenticazione necessaria deve essere implementata dall'applicazione.
-   WOW64 nei computer che eseguono Windows a 64 bit non è supportato in Windows Server 2003 e Windows XP con Service Pack 2 (SP2) e versioni precedenti.
-   L'API server HTTP non supporta la registrazione di richieste e risposte HTTP.
-   L'API server HTTP non suddivide le risposte HTTP in uscita. Se necessario, l'applicazione deve implementare la suddivisione in blocchi della risposta.

 

 




