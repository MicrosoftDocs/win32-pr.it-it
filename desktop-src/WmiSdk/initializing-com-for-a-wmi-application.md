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
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="925db-103">Inizializzazione di COM per un'applicazione WMI</span><span class="sxs-lookup"><span data-stu-id="925db-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="925db-104">Il primo passaggio per la connessione a WMI consiste nella configurazione delle chiamate COM a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="925db-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="925db-105">Negli esempi di codice di questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="925db-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="925db-106">Nella procedura seguente viene descritto come inizializzare COM da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="925db-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="925db-107">**Per inizializzare COM da un'applicazione client**</span><span class="sxs-lookup"><span data-stu-id="925db-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="925db-108">Inizializzare COM con una chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="925db-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="925db-109">La chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) è una procedura standard per la configurazione di un'interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="925db-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="925db-110">WMI non richiede pertanto di osservare eventuali procedure aggiuntive quando si chiama **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="925db-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="925db-111">Per ulteriori informazioni, vedere [com](../com/component-object-model--com--portal.md).</span><span class="sxs-lookup"><span data-stu-id="925db-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="925db-112">Nell'esempio di codice riportato di seguito viene descritto come chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="925db-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="925db-113">Impostare i livelli di sicurezza COM generali con una chiamata all'interfaccia [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="925db-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="925db-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) è una funzione standard che è necessario chiamare quando si configura un'interfaccia com per un processo.</span><span class="sxs-lookup"><span data-stu-id="925db-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="925db-115">Chiamare **CoInitializeSecurity** se si desidera impostare le impostazioni di sicurezza predefinite per l'autenticazione, la rappresentazione o il servizio di autenticazione per un intero processo.</span><span class="sxs-lookup"><span data-stu-id="925db-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="925db-116">Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="925db-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="925db-117">Se si desidera impostare o modificare la sicurezza per un proxy specifico, è necessario chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="925db-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="925db-118">Utilizzare **CoSetProxyBlanket** ogni volta che è necessario impostare o modificare la sicurezza com quando si esegue in un altro processo in cui non è possibile controllare le impostazioni di sicurezza predefinite per l'autenticazione, la rappresentazione o il servizio di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="925db-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="925db-119">Per ulteriori informazioni, vedere [impostazione dei livelli di sicurezza in una connessione WMI](setting-the-security-levels-on-a-wmi-connection.md) e [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="925db-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="925db-120">WMI presenta diversi problemi di sicurezza che è opportuno tenere presente durante la programmazione di un'applicazione client WMI.</span><span class="sxs-lookup"><span data-stu-id="925db-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="925db-121">Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="925db-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="925db-122">Nell'esempio di codice seguente viene descritto come chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza com nel processo.</span><span class="sxs-lookup"><span data-stu-id="925db-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

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

    

<span data-ttu-id="925db-123">Dopo l'inizializzazione di COM, il passaggio successivo consiste nel creare una connessione a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="925db-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="925db-124">Per ulteriori informazioni, vedere [creazione di una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="925db-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="925db-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="925db-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="925db-126">Creazione di un'applicazione WMI con C++</span><span class="sxs-lookup"><span data-stu-id="925db-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="925db-127">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="925db-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
