---
title: Nozioni fondamentali sulle applicazioni
description: Nozioni fondamentali sulle applicazioni
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media Format SDK, nozioni fondamentali sulle applicazioni DRM
- Digital Rights Management (DRM), nozioni fondamentali sulle applicazioni
- DRM (Digital Rights Management), nozioni fondamentali sulle applicazioni
- Digital Rights Management (DRM), funzione WMDRMStartup
- DRM (Digital Rights Management), funzione WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220981"
---
# <a name="application-basics"></a><span data-ttu-id="aee3d-109">Nozioni fondamentali sulle applicazioni</span><span class="sxs-lookup"><span data-stu-id="aee3d-109">Application Basics</span></span>

<span data-ttu-id="aee3d-110">È necessario eseguire alcune operazioni di elaborazione aggiuntive per tutte le applicazioni che usano le API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="aee3d-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="aee3d-111">In questo argomento vengono descritti i requisiti per una semplice applicazione.</span><span class="sxs-lookup"><span data-stu-id="aee3d-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="aee3d-112">Per prima cosa, è necessario inizializzare le API estese del client Windows Media DRM chiamando la funzione [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="aee3d-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="aee3d-113">Gli oggetti dell'SDK sono oggetti COM, ma non è necessario chiamare **CoIntialize**, perché la funzione **WMDRMStatup** Inizializza com.</span><span class="sxs-lookup"><span data-stu-id="aee3d-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="aee3d-114">Windows Media Format SDK utilizza solo un subset di COM, pertanto se si utilizzano oggetti COM diversi da quelli nell'API Windows Media DRM client Extended, è comunque necessario chiamare **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="aee3d-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="aee3d-115">Tutti gli oggetti delle API estese del client Windows Media DRM vengono creati usando funzioni e metodi helper.</span><span class="sxs-lookup"><span data-stu-id="aee3d-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="aee3d-116">Non è mai necessario chiamare **CoCreateInstance** per creare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="aee3d-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="aee3d-117">La prima interfaccia di cui creare un'istanza per qualsiasi applicazione che usa l'SDK è [**IWMDRMProvider**](iwmdrmprovider.md), che è possibile usare per creare un'istanza di tutte le altre interfacce di base.</span><span class="sxs-lookup"><span data-stu-id="aee3d-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="aee3d-118">Per ottenere un'istanza di **IWMDRMProvider**, è necessario chiamare [**WMDRMCreateProvider**](wmdrmcreateprovider.md) o [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span><span class="sxs-lookup"><span data-stu-id="aee3d-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="aee3d-119">La differenza tra queste funzioni è che **WMDRMCreateProvider** crea un oggetto che può a sua volta creare solo oggetti che non supportano metodi che richiedono la libreria stub.</span><span class="sxs-lookup"><span data-stu-id="aee3d-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="aee3d-120">Dopo avere creato un'istanza di **IWMDRMProvider**, è possibile creare gli altri oggetti necessari chiamando [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="aee3d-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="aee3d-121">Quando si è pronti per uscire dall'applicazione, è necessario rilasciare le risorse del sottosistema DRM chiamando la funzione [**WMDRMShutdown**](wmdrmshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="aee3d-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="aee3d-122">Questa funzione arresta anche COM.</span><span class="sxs-lookup"><span data-stu-id="aee3d-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="aee3d-123">Nell'esempio di codice riportato di seguito viene illustrato come inizializzare e concludere un'applicazione che utilizza le API estese del client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="aee3d-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a><span data-ttu-id="aee3d-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aee3d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aee3d-125">**Introduzione**</span><span class="sxs-lookup"><span data-stu-id="aee3d-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




