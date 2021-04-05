---
title: Chiusura e pulizia
description: Per terminare correttamente un'applicazione, è necessario eseguire le operazioni di pulitura seguenti.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044819"
---
# <a name="shutdown-and-cleanup"></a>Chiusura e pulizia

Per terminare correttamente un'applicazione, è necessario eseguire le operazioni di pulizia seguenti:

-   Rimuovere tutti gli URL registrati dal gruppo di URL chiamando la funzione [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) per annullare la registrazione degli URL registrati in precedenza nella chiamata a [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Chiudere il gruppo di URL chiamando la funzione [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) . Tutti i gruppi di URL creati in una sessione del server devono essere chiusi prima di chiudere la sessione del server.
-   Chiudere la sessione del server chiamando [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Chiudere l'handle per la coda delle richieste chiamando [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Terminare le risorse create dall'API del server HTTP chiamando la funzione [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) con le impostazioni dei flag corrispondenti per ogni chiamata effettuata originariamente dall'applicazione a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Ognuna di queste chiamate termina tutte le risorse create nella chiamata a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




