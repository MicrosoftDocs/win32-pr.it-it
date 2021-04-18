---
description: Dopo aver recuperato un puntatore a un proxy IWbemServices, è necessario impostare la sicurezza sul proxy per accedere a WMI tramite il proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Impostazione dei livelli di sicurezza in una connessione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318522"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="34db4-103">Impostazione dei livelli di sicurezza in una connessione WMI</span><span class="sxs-lookup"><span data-stu-id="34db4-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="34db4-104">Dopo aver recuperato un puntatore a un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , è necessario impostare la sicurezza sul proxy per accedere a WMI tramite il proxy.</span><span class="sxs-lookup"><span data-stu-id="34db4-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="34db4-105">È necessario impostare la sicurezza perché il proxy **IWbemServices** concede l'accesso a un oggetto out-of-process.</span><span class="sxs-lookup"><span data-stu-id="34db4-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="34db4-106">In generale, la sicurezza COM non consente a un processo di accedere a un altro processo se non si impostano le proprietà di sicurezza appropriate.</span><span class="sxs-lookup"><span data-stu-id="34db4-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="34db4-107">Per ulteriori informazioni, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="34db4-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="34db4-108">Per le connessioni a sistemi operativi diversi sono necessari diversi livelli di autenticazione e rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="34db4-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="34db4-109">Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="34db4-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="34db4-110">Negli esempi di codice di questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="34db4-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="34db4-111">Nella procedura riportata di seguito viene descritto come impostare i livelli di sicurezza in una connessione WMI.</span><span class="sxs-lookup"><span data-stu-id="34db4-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="34db4-112">**Per impostare i livelli di sicurezza in una connessione WMI**</span><span class="sxs-lookup"><span data-stu-id="34db4-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="34db4-113">Impostare i livelli di sicurezza sul proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="34db4-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="34db4-114">Nell'esempio di codice riportato di seguito viene descritto un modo comune per chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="34db4-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

<span data-ttu-id="34db4-115">Dopo aver impostato i livelli di sicurezza per il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , è possibile accedere alle varie funzionalità di WMI.</span><span class="sxs-lookup"><span data-stu-id="34db4-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="34db4-116">Al termine dell'utilizzo di WMI, è necessario arrestare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="34db4-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="34db4-117">Per ulteriori informazioni, vedere [pulizia e arresto di un'applicazione WMI](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="34db4-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
