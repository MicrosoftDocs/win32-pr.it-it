---
description: 'Dopo aver impostato le chiamate standard a COM, è necessario connettersi a WMI tramite una chiamata al metodo IWbemLocator:: ConnectServer.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Creazione di una connessione a uno spazio dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485741"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="9d27a-103">Creazione di una connessione a uno spazio dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="9d27a-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="9d27a-104">Dopo aver impostato le chiamate standard a COM, è necessario connettersi a WMI tramite una chiamata al metodo [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="9d27a-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="9d27a-105">Il metodo **ConnectServer** restituisce un proxy di un'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="9d27a-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="9d27a-106">Tramite **IWbemServices** è possibile accedere alle diverse funzionalità di WMI.</span><span class="sxs-lookup"><span data-stu-id="9d27a-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="9d27a-107">Negli esempi di codice di questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="9d27a-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="9d27a-108">Nella procedura riportata di seguito viene descritto come creare una connessione a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="9d27a-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="9d27a-109">**Per creare una connessione a uno spazio dei nomi WMI**</span><span class="sxs-lookup"><span data-stu-id="9d27a-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="9d27a-110">Inizializzare l'interfaccia [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) tramite una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="9d27a-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="9d27a-111">WMI non richiede l'esecuzione di procedure aggiuntive quando si chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="9d27a-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="9d27a-112">Nell'esempio di codice seguente viene descritto come inizializzare [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="9d27a-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   <span data-ttu-id="9d27a-113">Connettersi a WMI tramite una chiamata al metodo [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="9d27a-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="9d27a-114">Il metodo [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) restituisce un proxy a un'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che usa per accedere allo spazio dei nomi WMI locale o remoto specificato nella chiamata a **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="9d27a-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="9d27a-115">Nell'esempio di codice riportato di seguito viene descritto come chiamare [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="9d27a-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

<span data-ttu-id="9d27a-116">Dopo aver ricevuto un puntatore al proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , è necessario impostare la sicurezza sul proxy per accedere a WMI.</span><span class="sxs-lookup"><span data-stu-id="9d27a-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="9d27a-117">Per ulteriori informazioni, vedere [impostazione dei livelli di sicurezza in una connessione WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9d27a-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d27a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d27a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d27a-119">Creazione di un'applicazione WMI con C++</span><span class="sxs-lookup"><span data-stu-id="9d27a-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="9d27a-120">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="9d27a-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
