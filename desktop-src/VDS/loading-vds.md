---
description: Caricamento di VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Caricamento di VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314617"
---
# <a name="loading-vds"></a><span data-ttu-id="f1f1f-103">Caricamento di VDS</span><span class="sxs-lookup"><span data-stu-id="f1f1f-103">Loading VDS</span></span>

<span data-ttu-id="f1f1f-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f1f1f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f1f1f-105">**Per caricare e inizializzare VDS**</span><span class="sxs-lookup"><span data-stu-id="f1f1f-105">**To load and initialize VDS**</span></span>

1.  <span data-ttu-id="f1f1f-106">Rilascia interfacce non null.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-106">Release non-null interfaces.</span></span>
2.  <span data-ttu-id="f1f1f-107">Chiamare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)o [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) per ottenere un puntatore all'oggetto del caricatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-107">Call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex), or [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) function to obtain a pointer to the service loader object.</span></span>

    <span data-ttu-id="f1f1f-108">**CLSCTX \_ Non \_** è possibile specificare disable AAA in questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-108">**CLSCTX\_DISABLE\_AAA** cannot be specified in this call.</span></span> <span data-ttu-id="f1f1f-109">Se viene chiamato [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , non è possibile specificare **EOAC \_ disabilitare \_ AAA** nel parametro *dwCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="f1f1f-109">If [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is called, **EOAC\_DISABLE\_AAA** cannot be specified in the *dwCapabilities* parameter.</span></span>

3.  <span data-ttu-id="f1f1f-110">Chiamare il metodo [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) per caricare VDS.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-110">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load VDS.</span></span>

    <span data-ttu-id="f1f1f-111">Il passaggio di **null** come primo parametro consente di caricare e inizializzare VDS nell'host locale.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-111">Passing **NULL** as the first parameter loads and initializes VDS on the local host.</span></span>

4.  <span data-ttu-id="f1f1f-112">Chiamare il metodo [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) per attendere il completamento dell'inizializzazione VDS.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-112">Call the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to wait for VDS initialization to complete.</span></span>

<span data-ttu-id="f1f1f-113">Nell'esempio di codice seguente viene inizializzato il servizio che restituisce un puntatore all'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="f1f1f-113">The following code example initializes the service that returns a pointer to the service object.</span></span>


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="f1f1f-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1f1f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1f1f-115">Uso di VDS</span><span class="sxs-lookup"><span data-stu-id="f1f1f-115">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="f1f1f-116">**IVdsService::WaitForServiceReady**</span><span class="sxs-lookup"><span data-stu-id="f1f1f-116">**IVdsService::WaitForServiceReady**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[<span data-ttu-id="f1f1f-117">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="f1f1f-117">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="f1f1f-118">Oggetti installazione e servizio</span><span class="sxs-lookup"><span data-stu-id="f1f1f-118">Setup and Service Objects</span></span>](startup-and-service-objects.md)
</dt> </dl>

 

 
