---
description: Il primo passaggio per la connessione a WMI è la configurazione delle chiamate COM a CoInitializeEx e CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Inizializzazione di COM per un'applicazione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723188602e440cd3ba49d78d8efb3c28ddae30f35dd0d4361a4fdb5ced026ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318575"
---
# <a name="initializing-com-for-a-wmi-application"></a>Inizializzazione di COM per un'applicazione WMI

Il primo passaggio per la connessione a WMI è la configurazione delle chiamate COM a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

Gli esempi di codice in questo argomento richiedono i riferimenti seguenti e \# le istruzioni include per la corretta compilazione.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Nella procedura seguente viene descritto come inizializzare COM da un'applicazione client.

**Per inizializzare COM da un'applicazione client**

1.  Inizializzare COM con una chiamata a [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    La [**chiamata a CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) è una procedura standard per la configurazione di un'interfaccia COM. Wmi non richiede pertanto l'osservazione di procedure aggiuntive quando si chiama **CoInitializeEx.** Per altre informazioni, vedere [COM.](../com/component-object-model--com--portal.md)

    Nell'esempio di codice seguente viene descritto come chiamare [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Impostare i livelli di sicurezza COM generali con una chiamata [**all'interfaccia CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    [**CoInitializeSecurity è**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) una funzione standard che è necessario chiamare quando si configura un'interfaccia COM per un processo. Chiamare **CoInitializeSecurity se** si desidera impostare le impostazioni di sicurezza predefinite per l'autenticazione, la rappresentazione o il servizio di autenticazione per un intero processo. Per altre informazioni, vedere [Impostazione della sicurezza del processo dell'applicazione client.](setting-client-application-process-security.md) Se si vuole impostare o modificare la sicurezza per un proxy specifico, è necessario chiamare [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Usare **CoSetProxyBlanket** ogni volta che è necessario impostare o modificare la sicurezza COM durante l'esecuzione all'interno di un altro processo in cui non è possibile controllare le impostazioni di sicurezza predefinite per l'autenticazione, la rappresentazione o il servizio di autenticazione. Per altre informazioni, vedere [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) e Setting the Security on [IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

    WMI presenta diversi problemi di sicurezza che è necessario tenere presenti durante la programmazione di un'applicazione client WMI. Per altre informazioni, vedere [Impostazione della sicurezza del processo dell'applicazione client.](setting-client-application-process-security.md)

    Nell'esempio di codice seguente viene descritto come chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza COM nel processo.

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

Dopo l'inizializzazione di COM, il passaggio successivo consiste nel creare una connessione a uno spazio dei nomi WMI. Per altre informazioni, vedere [Creazione di una connessione a uno spazio dei nomi WMI.](creating-a-connection-to-a-wmi-namespace.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
