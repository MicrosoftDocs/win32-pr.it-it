---
title: Arresto e pulizia
description: Per terminare correttamente un'applicazione, è necessario eseguire le operazioni di pulizia seguenti.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a551ad57ddbf63c6ff598814794bc5837da646e98169d8250e543575abd013a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950691"
---
# <a name="shutdown-and-cleanup"></a>Arresto e pulizia

Per terminare correttamente un'applicazione, è necessario eseguire le operazioni di pulizia seguenti:

-   Rimuovere tutti gli URL registrati dal gruppo di URL chiamando la funzione [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) per annullare la registrazione degli URL registrati in precedenza nella chiamata a [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Chiudere il gruppo di URL chiamando la [**funzione HttpCloseUrlGroup.**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) Tutti i gruppi di URL creati in una sessione del server devono essere chiusi prima di chiudere la sessione del server.
-   Chiudere la sessione del server chiamando [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Chiudere l'handle per la coda di richieste chiamando [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Terminare le risorse create dall'API server HTTP chiamando la funzione [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) con le impostazioni del flag corrispondenti per ogni chiamata dell'applicazione originariamente effettuata a [**HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize) Ognuna di queste chiamate termina tutte le risorse create nella chiamata a [**HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize)

 

 




