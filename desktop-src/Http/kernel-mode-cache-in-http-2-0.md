---
title: Cache in modalità kernel
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045254"
---
# <a name="kernel-mode-cache"></a>Cache in modalità kernel

L'API server HTTP versione 2,0 consente alle applicazioni di memorizzare nella cache le risposte con contenuto statico in modalità kernel. Si ottengono prestazioni migliori quando le richieste vengono gestite dalla cache del kernel senza passare alla modalità utente.

L'API server HTTP applica le configurazioni di proprietà appropriate a tutte le richieste gestite dalla cache del kernel, incluse le risposte di registrazione. Le richieste che richiedono l'autenticazione, tuttavia, non verranno gestite dalla cache.

L'API server HTTP limita la cache in modalità kernel alle richieste che soddisfano le condizioni seguenti:

-   Il verbo della richiesta è GET e viene ricevuta l'intera richiesta.
-   La richiesta non deve avere un corpo entità.
-   Il protocollo HTTP è la versione 1,0 o successiva.
-   L'intestazione "translate: f" non è presente.
-   Si prevede che le intestazioni diverse da "Expect: 100-continue" non siano presenti.
-   L'intestazione dell'autorizzazione non è presente.
-   Le intestazioni Range e If-Range non sono presenti.

Oltre alle limitazioni per la richiesta, la risposta deve soddisfare anche le condizioni seguenti:

-   Per impostazione predefinita, le dimensioni della risposta sono limitate a 256 KB. Per modificare le dimensioni della risposta memorizzata nella cache, impostare il valore del registro di sistema **UriMaxUriBytes** sul numero di byte richiesto.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   L'intera risposta deve essere fornita in una singola chiamata a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).
-   L'intestazione della data nella risposta non deve essere evitata.
-   Se è presente l'intestazione Last-modified, il valore dell'intestazione deve avere la sintassi corretta. Il valore di ora in questa intestazione viene usato per la verifica del controllo della cache.
-   Lo spazio disponibile nella cache in modalità kernel è sufficiente per archiviare la risposta.

Per impostazione predefinita, la cache di risposta in modalità kernel è abilitata. Se una o più condizioni per la richiesta o la risposta elencate in precedenza non vengono soddisfatte, la risposta verrà inviata, ma non verrà memorizzata nella cache. Nell'API del server HTTP versione 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) include un parametro facoltativo *pCachePolicy* per passare la struttura dei [**\_ \_ criteri della cache HTTP**](/windows/desktop/api/Http/ns-http-http_cache_policy) . Per configurare la cache, le applicazioni utilizzano la struttura dei criteri di cache.

 

 




