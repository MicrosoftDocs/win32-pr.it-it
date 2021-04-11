---
description: Un programma di configurazione del servizio usa le funzioni ChangeServiceConfig e ChangeServiceConfig2 per modificare i parametri di configurazione di un servizio installato.
ms.assetid: 79aa4ad5-87ee-4f5d-9c8e-4e788f4c7182
title: Modifica della configurazione di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7afffcb896e7732536ad308ccd54f0ae1f0a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346526"
---
# <a name="changing-a-services-configuration"></a><span data-ttu-id="03d9a-103">Modifica della configurazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="03d9a-103">Changing a Service's Configuration</span></span>

<span data-ttu-id="03d9a-104">Un [programma di configurazione del servizio](service-configuration-programs.md) usa le funzioni [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) e [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) per modificare i parametri di configurazione di un servizio installato.</span><span class="sxs-lookup"><span data-stu-id="03d9a-104">A [service configuration program](service-configuration-programs.md) uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) and [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) functions to change the configuration parameters of an installed service.</span></span> <span data-ttu-id="03d9a-105">Il programma apre un handle per l'oggetto servizio, ne modifica la configurazione e quindi chiude l'handle dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="03d9a-105">The program opens a handle to the service object, modifies its configuration, and then closes the service object handle.</span></span>

<span data-ttu-id="03d9a-106">Nell'esempio seguente, la funzione DoDisableSvc utilizza [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) per impostare il tipo di avvio del servizio su "disabled", la funzione DoEnableSvc utilizza **ChangeServiceConfig** per impostare il tipo di avvio del servizio su "Enabled" e la funzione DoUpdateSvcDesc utilizza [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) per impostare la descrizione del servizio su "Questa è una descrizione del test".</span><span class="sxs-lookup"><span data-stu-id="03d9a-106">In the following example, the DoDisableSvc function uses [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) to change the service start type to "Disabled", the DoEnableSvc function uses **ChangeServiceConfig** to change the service start type to "Enabled", and the DoUpdateSvcDesc function uses [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) to set the service description to "This is a test description".</span></span> <span data-ttu-id="03d9a-107">La variabile szSvcName è una variabile globale che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="03d9a-107">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="03d9a-108">Per l'esempio completo che imposta questa variabile, vedere [SvcConfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="03d9a-108">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Disables the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDisableSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;

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
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service start type.

    if (! ChangeServiceConfig( 
        schService,        // handle of service 
        SERVICE_NO_CHANGE, // service type: no change 
        SERVICE_DISABLED,  // service start type 
        SERVICE_NO_CHANGE, // error control: no change 
        NULL,              // binary path: no change 
        NULL,              // load order group: no change 
        NULL,              // tag ID: no change 
        NULL,              // dependencies: no change 
        NULL,              // account name: no change 
        NULL,              // password: no change 
        NULL) )            // display name: no change
    {
        printf("ChangeServiceConfig failed (%d)\n", GetLastError()); 
    }
    else printf("Service disabled successfully.\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

//
// Purpose: 
//   Enables the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoEnableSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;

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
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service start type.

    if (! ChangeServiceConfig( 
        schService,            // handle of service 
        SERVICE_NO_CHANGE,     // service type: no change 
        SERVICE_DEMAND_START,  // service start type 
        SERVICE_NO_CHANGE,     // error control: no change 
        NULL,                  // binary path: no change 
        NULL,                  // load order group: no change 
        NULL,                  // tag ID: no change 
        NULL,                  // dependencies: no change 
        NULL,                  // account name: no change 
        NULL,                  // password: no change 
        NULL) )                // display name: no change
    {
        printf("ChangeServiceConfig failed (%d)\n", GetLastError()); 
    }
    else printf("Service enabled successfully.\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

//
// Purpose: 
//   Updates the service description to "This is a test description".
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDesc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_DESCRIPTION sd;
    LPTSTR szDesc = TEXT("This is a test description");

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
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service description.

    sd.lpDescription = szDesc;

    if( !ChangeServiceConfig2(
        schService,                 // handle to service
        SERVICE_CONFIG_DESCRIPTION, // change: description
        &sd) )                      // new description
    {
        printf("ChangeServiceConfig2 failed\n");
    }
    else printf("Service description updated successfully.\n");

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="03d9a-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03d9a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d9a-110">Configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="03d9a-110">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="03d9a-111">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="03d9a-111">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



