---
description: Dopo aver impostato i livelli di sicurezza per il puntatore IWbemServices, è possibile accedere alle varie funzionalità di WMI. Al termine dell'utilizzo di WMI, è necessario arrestare l'applicazione.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Pulizia e arresto di un'applicazione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967975"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="9e628-104">Pulizia e arresto di un'applicazione WMI</span><span class="sxs-lookup"><span data-stu-id="9e628-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="9e628-105">Dopo aver impostato i livelli di sicurezza per il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , è possibile accedere alle varie funzionalità di WMI.</span><span class="sxs-lookup"><span data-stu-id="9e628-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="9e628-106">Al termine dell'utilizzo di WMI, è necessario arrestare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e628-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="9e628-107">Nella procedura riportata di seguito viene descritto come eseguire la pulizia e l'arresto di un'applicazione WMI.</span><span class="sxs-lookup"><span data-stu-id="9e628-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="9e628-108">**Per pulire e arrestare un'applicazione WMI**</span><span class="sxs-lookup"><span data-stu-id="9e628-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="9e628-109">Rilascia le interfacce COM aperte.</span><span class="sxs-lookup"><span data-stu-id="9e628-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="9e628-110">Le due interfacce primarie che è necessario ricordare di rilasciare sono [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="9e628-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="9e628-111">Chiamare [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="9e628-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="9e628-112">Come per tutte le applicazioni COM, è necessario chiamare [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) alla fine dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e628-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="9e628-113">Uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e628-113">Exit your application.</span></span>

    <span data-ttu-id="9e628-114">Nell'esempio di codice seguente viene illustrato come uscire da un'applicazione client WMI.</span><span class="sxs-lookup"><span data-stu-id="9e628-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="9e628-115">La `pSvc` variabile è di tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* e la variabile PLoc è di tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .</span><span class="sxs-lookup"><span data-stu-id="9e628-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="9e628-116">A questo punto è stato inizializzato correttamente COM, si è eseguito l'accesso a WMI ed è stata chiusa l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e628-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="9e628-117">Per ulteriori informazioni, vedere [esempio: creazione di un'applicazione WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="9e628-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e628-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e628-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e628-119">Creazione di un'applicazione WMI con C++</span><span class="sxs-lookup"><span data-stu-id="9e628-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
