---
title: Funzionalità dell'API del server HTTP
description: In questo argomento sono supportate e non supportate le funzionalità dell'API del server HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Funzionalità dell'API del server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf567d4576618b07ef5ad8dec91b360f37ab46eb820ff52e2bca896ca91a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014779"
---
# <a name="http-server-api-features"></a>Funzionalità dell'API del server HTTP

Gli elenchi seguenti descrivono le funzionalità supportate e non supportate dell'API del server HTTP.

## <a name="features-supported"></a>Funzionalità supportate

HTTP supporta le funzionalità seguenti:

-   Funzionalità server HTTP v1.0 e v1.1.
-   Secure Sockets Layer 3.0 (SSL) con supporto per i certificati client e server.
-   Caching di frammenti di dati da usare nelle risposte successive.
-   Supporto per gli indirizzi IPv6 e IPv4.
-   Prenotazioni dello spazio dei nomi URL per la sicurezza delle applicazioni.
-   Handle True per tutti gli oggetti.
-   Modelli di I/O sincroni e asincroni.
-   Supporto per WOW64 nei computer che eseguono Windows a 64 bit a partire da Windows Server 2003 con Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Funzionalità non supportate

L'API server HTTP non supporta le funzionalità seguenti:

-   L'API del server HTTP non esegue l'autenticazione client o server in base al contenuto delle intestazioni della richiesta HTTP. Qualsiasi autenticazione richiesta deve essere implementata dall'applicazione.
-   WOW64 nei computer che eseguono Windows a 64 bit non è supportato in Windows Server 2003 e Windows XP con Service Pack 2 (SP2) e versioni precedenti.
-   L'API del server HTTP non supporta la registrazione di richieste e risposte HTTP.
-   L'API del server HTTP non esegue il blocco delle risposte HTTP in uscita. Se necessario, l'applicazione deve implementare la suddivisione in blocchi delle risposte.

 

 




