---
description: Il primo passaggio per la connessione a WMI consiste nella configurazione delle chiamate COM a CoInitializeEx e CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Inizializzazione di COM per un'applicazione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968549"
---
# <a name="initializing-com-for-a-wmi-application"></a>Inizializzazione di COM per un'applicazione WMI

Il primo passaggio per la connessione a WMI consiste nella configurazione delle chiamate COM a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Negli esempi di codice di questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Nella procedura seguente viene descritto come inizializzare COM da un'applicazione client.

**Per inizializzare COM da un'applicazione client**

1.  Inizializzare COM con una chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    La chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) è una procedura standard per la configurazione di un'interfaccia com. WMI non richiede pertanto di osservare eventuali procedure aggiuntive quando si chiama **CoInitializeEx**. Per ulteriori informazioni, vedere [com](../com/component-object-model--com--portal.md).

    Nell'esempio di codice riportato di seguito viene descritto come chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Impostare i livelli di sicurezza COM generali con una chiamata all'interfaccia [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) è una funzione standard che è necessario chiamare quando si configura un'interfaccia com per un processo. Chiamare **CoInitializeSecurity** se si desidera impostare le impostazioni di sicurezza predefinite per l'autenticazione, la rappresentazione o il servizio di autenticazione per un intero processo. Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md). Se si desidera impostare o modificare la sicurezza per un proxy specifico, è necessario chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Utilizzare **CoSetProxyBlanket** ogni volta che è necessario impostare o modificare la sicurezza com quando si esegue in un altro processo in cui non è possibile controllare le impostazioni di sicurezza predefinite per l'autenticazione, la rappresentazione o il servizio di autenticazione. Per ulteriori informazioni, vedere [impostazione dei livelli di sicurezza in una connessione WMI](setting-the-security-levels-on-a-wmi-connection.md) e [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

    WMI presenta diversi problemi di sicurezza che è opportuno tenere presente durante la programmazione di un'applicazione client WMI. Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md).

    Nell'esempio di codice seguente viene descritto come chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza com nel processo.

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

    

Dopo l'inizializzazione di COM, il passaggio successivo consiste nel creare una connessione a uno spazio dei nomi WMI. Per ulteriori informazioni, vedere [creazione di una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
