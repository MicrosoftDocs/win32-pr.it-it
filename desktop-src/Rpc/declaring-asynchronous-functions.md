---
title: Dichiarazione di funzioni asincrone
description: Per dichiarare una funzione RPC come asincrona, dichiarare prima la funzione come parte di una definizione di interfaccia in un file IDL (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- RPC (Remote Procedure Call), attività, dichiarazione di funzioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963531"
---
# <a name="declaring-asynchronous-functions"></a>Dichiarazione di funzioni asincrone

Per dichiarare una funzione RPC come asincrona, dichiarare prima la funzione come parte di una definizione di interfaccia in un file IDL (Interface Definition Language). L'utilizzo di funzioni RPC asincrone non richiede alcuna modifica speciale al file IDL. Nell'esempio seguente viene illustrato un file IDL per un'applicazione che utilizza una funzione asincrona.

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

Per tutte le funzioni RPC asincrone utilizzate dall'applicazione, sarà necessario modificare la dichiarazione delle funzioni asincrone all'interno del file ACF dell'applicazione. Applicare l'attributo [**\[ Async \]**](../midl/async.md) a ogni nome di funzione asincrona, come illustrato nell'esempio seguente:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Quando si applica l'attributo **\[ Async \]** nel file ACF, il compilatore MIDL genera automaticamente un parametro di handle asincrono aggiuntivo nel codice stub.

 

 