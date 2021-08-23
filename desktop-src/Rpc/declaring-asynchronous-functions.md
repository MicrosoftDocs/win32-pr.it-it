---
title: Dichiarazione di funzioni asincrone
description: Per dichiarare una funzione RPC come asincrona, dichiarare prima di tutto la funzione come parte di una definizione di interfaccia in un file IDL (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Chiamata di procedura remota RPC, attività, dichiarazione di funzioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc0978156fe91291b91937082690258550b7f02f1d7b6e5334dd0741a9f0211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931049"
---
# <a name="declaring-asynchronous-functions"></a>Dichiarazione di funzioni asincrone

Per dichiarare una funzione RPC come asincrona, dichiarare prima di tutto la funzione come parte di una definizione di interfaccia in un file IDL (Interface Definition Language). L'uso di funzioni RPC asincrone non richiede modifiche speciali al file IDL. L'esempio seguente illustra un file IDL per un'applicazione che usa una funzione asincrona.

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

Per tutte le funzioni RPC asincrone utilizzate dall'applicazione, è necessario modificare la dichiarazione delle funzioni asincrone all'interno del file ACF dell'applicazione. Applicare [**\[ l'attributo async \]**](../midl/async.md) a ogni nome di funzione asincrona, come illustrato nell'esempio seguente:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Quando si applica **\[ l'attributo \] asincrono** nel file ACF, il compilatore MIDL genera automaticamente un parametro handle asincrono aggiuntivo nel codice stub.

 

 