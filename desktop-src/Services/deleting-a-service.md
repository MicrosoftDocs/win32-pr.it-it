---
description: Un programma di configurazione del servizio usa la funzione OpenService per ottenere un handle per un oggetto servizio installato. Il programma può quindi utilizzare l'handle dell'oggetto servizio nella funzione DeleteService per eliminare il servizio dal database SCM.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Eliminazione di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968194"
---
# <a name="deleting-a-service"></a><span data-ttu-id="3e66c-104">Eliminazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="3e66c-104">Deleting a Service</span></span>

<span data-ttu-id="3e66c-105">Un [programma di configurazione del servizio](service-configuration-programs.md) usa la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) per ottenere un handle per un oggetto servizio installato.</span><span class="sxs-lookup"><span data-stu-id="3e66c-105">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle to an installed service object.</span></span> <span data-ttu-id="3e66c-106">Il programma può quindi utilizzare l'handle dell'oggetto servizio nella funzione [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) per eliminare il servizio dal database SCM.</span><span class="sxs-lookup"><span data-stu-id="3e66c-106">The program can then use the service object handle in the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service from the SCM database.</span></span>

<span data-ttu-id="3e66c-107">La funzione DoDeleteSvc nell'esempio seguente illustra come eliminare un servizio dal database SCM.</span><span class="sxs-lookup"><span data-stu-id="3e66c-107">The DoDeleteSvc function in the following example shows how to delete a service from the SCM database.</span></span> <span data-ttu-id="3e66c-108">La variabile szSvcName è una variabile globale che contiene il nome del servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3e66c-108">The szSvcName variable is a global variable that contains the name of the service to be deleted.</span></span> <span data-ttu-id="3e66c-109">Per l'esempio completo che imposta questa variabile, vedere [SvcConfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="3e66c-109">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Deletes a service from the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDeleteSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_STATUS ssStatus; 

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,       // SCM database 
        szSvcName,          // name of service 
        DELETE);            // need delete access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Delete the service.
 
    if (! DeleteService(schService) ) 
    {
        printf("DeleteService failed (%d)\n", GetLastError()); 
    }
    else printf("Service deleted successfully\n"); 
 
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="3e66c-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e66c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e66c-111">Installazione, rimozione ed enumerazione del servizio</span><span class="sxs-lookup"><span data-stu-id="3e66c-111">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="3e66c-112">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="3e66c-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



