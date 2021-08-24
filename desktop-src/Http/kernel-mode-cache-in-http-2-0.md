---
title: Cache in modalità kernel
description: Cache in modalità kernel
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34296ae6d0bca81988437478eb5893f1a7cb1b3c8a0dc2ae461356499bbfe10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340501"
---
# <a name="kernel-mode-cache"></a>Cache in modalità kernel

L'API server HTTP versione 2.0 consente alle applicazioni di memorizzare nella cache le risposte con contenuto statico in modalità kernel. Si ottiene un miglioramento delle prestazioni quando le richieste vengono servite dalla cache del kernel senza passare alla modalità utente.

L'API del server HTTP applica le configurazioni delle proprietà appropriate a tutte le richieste servite dalla cache del kernel, incluse le risposte di registrazione. Le richieste che richiedono l'autenticazione, tuttavia, non verranno servite dalla cache.

L'API del server HTTP limita la cache in modalità kernel alle richieste che soddisfano le condizioni seguenti:

-   Il verbo della richiesta è GET e viene ricevuta l'intera richiesta.
-   La richiesta non deve avere un corpo dell'entità.
-   Il protocollo HTTP è versione 1.0 o successiva.
-   L'intestazione "Translate: f" non è presente.
-   Le intestazioni previste diverse da "Expect: 100-Continue" non sono presenti.
-   L'intestazione dell'autorizzazione non è presente.
-   Le intestazioni Range e If-Range non sono presenti.

Oltre alle restrizioni relative alla richiesta, la risposta deve soddisfare anche le condizioni seguenti:

-   Per impostazione predefinita, le dimensioni della risposta sono limitate a 256 KB. Per modificare le dimensioni della risposta memorizzata nella cache, impostare il valore del Registro di sistema **UriMaxUriBytes** sul numero di byte richiesto.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   L'intera risposta deve essere fornita in una singola chiamata a [**HttpSendHttpResponse.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)
-   L'intestazione della data nella risposta non deve essere eliminata.
-   Se è presente l'ultima intestazione modificata, il valore dell'intestazione deve avere la sintassi corretta. Il valore dell'ora in questa intestazione viene usato per la verifica del controllo della cache.
-   La cache in modalità kernel ha spazio sufficiente per archiviare la risposta.

Per impostazione predefinita, la cache delle risposte in modalità kernel è abilitata. Se una delle condizioni per la richiesta o la risposta elencata sopra non viene soddisfatta, la risposta verrà inviata, ma non verrà memorizzata nella cache. Nell'API del server HTTP versione 2.0 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) include un parametro *pCachePolicy* facoltativo per passare la [**struttura HTTP CACHE \_ \_ POLICY.**](/windows/desktop/api/Http/ns-http-http_cache_policy) Le applicazioni usano la struttura dei criteri della cache per configurare la cache.

 

 




