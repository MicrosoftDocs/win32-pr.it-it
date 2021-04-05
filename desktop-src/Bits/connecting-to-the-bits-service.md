---
title: Connessione al servizio BITS
description: Per connettersi al servizio BITS, creare un'istanza dell'oggetto BackgroundCopyManager, come illustrato nell'esempio seguente.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117971"
---
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="9b714-103">Connessione al servizio BITS</span><span class="sxs-lookup"><span data-stu-id="9b714-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="9b714-104">Per connettersi al servizio di sistema BITS, creare un'istanza dell'oggetto BackgroundCopyManager, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9b714-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="9b714-105">Il servizio di sistema BITS è il servizio di sistema Windows in esecuzione sul computer client che implementa la funzionalità di trasferimento in background.</span><span class="sxs-lookup"><span data-stu-id="9b714-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



<span data-ttu-id="9b714-106">Per verificare la presenza di una versione specifica di BITS, usare un identificatore di classe simbolico per BackgroundCopyManager in base alla versione che si vuole controllare.</span><span class="sxs-lookup"><span data-stu-id="9b714-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="9b714-107">Ad esempio, per testare BITS 10,2, usare CLSID \_ BackgroundCopyManager10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="9b714-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="9b714-108">Nell'esempio seguente viene illustrato come utilizzare uno degli identificatori di classe simbolici.</span><span class="sxs-lookup"><span data-stu-id="9b714-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



<span data-ttu-id="9b714-109">Usare i metodi dell'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) per [creare processi di trasferimento](creating-a-job.md), [enumerare i processi](enumerating-jobs-in-the-transfer-queue.md) nella coda e [recuperare i processi](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="9b714-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="9b714-110">BITS richiede che i proxy di interfaccia del client usino il livello di rappresentazione o di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="9b714-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="9b714-111">Se l'applicazione non chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com utilizza l'opzione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9b714-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="9b714-112">BITS ha esito negativo con E \_ AccessDenied se il livello di rappresentazione corretto non è impostato.</span><span class="sxs-lookup"><span data-stu-id="9b714-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="9b714-113">Se si fornisce una libreria che esercita le interfacce BITS e un'applicazione che chiama la libreria imposta il livello di rappresentazione seguente, sarà necessario chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare il livello di rappresentazione corretto per ogni interfaccia bits chiamata.</span><span class="sxs-lookup"><span data-stu-id="9b714-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="9b714-114">Prima di uscire dall'applicazione, rilasciare la copia del puntatore all'interfaccia [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="9b714-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="9b714-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b714-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9b714-116">[Chiamata a BITS da .NET e C#](/windows/desktop/Bits/bits-dot-net) per BITS</span><span class="sxs-lookup"><span data-stu-id="9b714-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 