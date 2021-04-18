---
description: Un programma di configurazione del servizio utilizza la funzione CreateService per installare un servizio nel database SCM.
ms.assetid: b94bf94e-1b07-4686-be5c-306e7cf13f39
title: Installazione di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e72953b2d3fc3ce549f614a035c9614c4d895a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306336"
---
# <a name="installing-a-service"></a><span data-ttu-id="ddda2-103">Installazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="ddda2-103">Installing a Service</span></span>

<span data-ttu-id="ddda2-104">Un [programma di configurazione del servizio](service-configuration-programs.md) utilizza la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per installare un servizio nel database SCM.</span><span class="sxs-lookup"><span data-stu-id="ddda2-104">A [service configuration program](service-configuration-programs.md) uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a service in the SCM database.</span></span>

<span data-ttu-id="ddda2-105">La funzione SvcInstall nell'esempio seguente illustra come installare un servizio dal programma del servizio stesso.</span><span class="sxs-lookup"><span data-stu-id="ddda2-105">The SvcInstall function in the following example shows how to install a service from the service program itself.</span></span> <span data-ttu-id="ddda2-106">Per l'esempio completo, vedere [svc. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="ddda2-106">For the complete example, see [Svc.cpp](svc-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Installs a service in the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID SvcInstall()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    TCHAR szPath[MAX_PATH];

    if( !GetModuleFileName( "", szPath, MAX_PATH ) )
    {
        printf("Cannot install service (%d)\n", GetLastError());
        return;
    }

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

    // Create the service

    schService = CreateService( 
        schSCManager,              // SCM database 
        SVCNAME,                   // name of service 
        SVCNAME,                   // service name to display 
        SERVICE_ALL_ACCESS,        // desired access 
        SERVICE_WIN32_OWN_PROCESS, // service type 
        SERVICE_DEMAND_START,      // start type 
        SERVICE_ERROR_NORMAL,      // error control type 
        szPath,                    // path to service's binary 
        NULL,                      // no load ordering group 
        NULL,                      // no tag identifier 
        NULL,                      // no dependencies 
        NULL,                      // LocalSystem account 
        NULL);                     // no password 
 
    if (schService == NULL) 
    {
        printf("CreateService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }
    else printf("Service installed successfully\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="ddda2-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddda2-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddda2-108">Installazione, rimozione ed enumerazione del servizio</span><span class="sxs-lookup"><span data-stu-id="ddda2-108">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="ddda2-109">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="ddda2-109">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



