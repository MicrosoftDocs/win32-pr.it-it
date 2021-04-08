---
description: Un programma di configurazione del servizio usa la funzione OpenService per ottenere un handle \_ con \_ accesso alla configurazione della query di servizio a un oggetto del servizio installato.
ms.assetid: e6633dc9-c9b6-457d-8adc-e751ec9cf71d
title: Esecuzione di query su una configurazione dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efddea6ca590aa07b0c523588295d5f87ffefa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885041"
---
# <a name="querying-a-services-configuration"></a><span data-ttu-id="a76cf-103">Esecuzione di query sulla configurazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="a76cf-103">Querying a Service's Configuration</span></span>

<span data-ttu-id="a76cf-104">Un [programma di configurazione del servizio](service-configuration-programs.md) usa la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) per ottenere un handle \_ con \_ accesso alla configurazione della query di servizio a un oggetto del servizio installato.</span><span class="sxs-lookup"><span data-stu-id="a76cf-104">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle with SERVICE\_QUERY\_CONFIG access to an installed service object.</span></span> <span data-ttu-id="a76cf-105">Il programma può quindi utilizzare l'handle dell'oggetto servizio nelle funzioni [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per recuperare la configurazione corrente del servizio.</span><span class="sxs-lookup"><span data-stu-id="a76cf-105">The program can then use the service object handle in the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to retrieve the current configuration of the service.</span></span>

<span data-ttu-id="a76cf-106">Nell'esempio seguente, la funzione DoQuerySvc USA [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per recuperare le informazioni di configurazione, quindi scrive le informazioni selezionate nella console.</span><span class="sxs-lookup"><span data-stu-id="a76cf-106">In the following example, the DoQuerySvc function uses [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) to retrieve configuration information, then writes selected information to the console.</span></span> <span data-ttu-id="a76cf-107">La variabile szSvcName è una variabile globale che contiene il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="a76cf-107">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="a76cf-108">Per l'esempio completo che imposta questa variabile, vedere [SvcConfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="a76cf-108">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Retrieves and displays the current service configuration.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoQuerySvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    LPQUERY_SERVICE_CONFIG lpsc; 
    LPSERVICE_DESCRIPTION lpsd;
    DWORD dwBytesNeeded, cbBufSize, dwError; 

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
        schSCManager,          // SCM database 
        szSvcName,             // name of service 
        SERVICE_QUERY_CONFIG); // need query config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Get the configuration information.
 
    if( !QueryServiceConfig( 
        schService, 
        NULL, 
        0, 
        &dwBytesNeeded))
    {
        dwError = GetLastError();
        if( ERROR_INSUFFICIENT_BUFFER == dwError )
        {
            cbBufSize = dwBytesNeeded;
            lpsc = (LPQUERY_SERVICE_CONFIG) LocalAlloc(LMEM_FIXED, cbBufSize);
        }
        else
        {
            printf("QueryServiceConfig failed (%d)", dwError);
            goto cleanup; 
        }
    }
  
    if( !QueryServiceConfig( 
        schService, 
        lpsc, 
        cbBufSize, 
        &dwBytesNeeded) ) 
    {
        printf("QueryServiceConfig failed (%d)", GetLastError());
        goto cleanup;
    }

    if( !QueryServiceConfig2( 
        schService, 
        SERVICE_CONFIG_DESCRIPTION,
        NULL, 
        0, 
        &dwBytesNeeded))
    {
        dwError = GetLastError();
        if( ERROR_INSUFFICIENT_BUFFER == dwError )
        {
            cbBufSize = dwBytesNeeded;
            lpsd = (LPSERVICE_DESCRIPTION) LocalAlloc(LMEM_FIXED, cbBufSize);
        }
        else
        {
            printf("QueryServiceConfig2 failed (%d)", dwError);
            goto cleanup; 
        }
    }
 
    if (! QueryServiceConfig2( 
        schService, 
        SERVICE_CONFIG_DESCRIPTION,
        (LPBYTE) lpsd, 
        cbBufSize, 
        &dwBytesNeeded) ) 
    {
        printf("QueryServiceConfig2 failed (%d)", GetLastError());
        goto cleanup;
    }
 
    // Print the configuration information.
 
    _tprintf(TEXT("%s configuration: \n"), szSvcName);
    _tprintf(TEXT("  Type: 0x%x\n"), lpsc->dwServiceType);
    _tprintf(TEXT("  Start Type: 0x%x\n"), lpsc->dwStartType);
    _tprintf(TEXT("  Error Control: 0x%x\n"), lpsc->dwErrorControl);
    _tprintf(TEXT("  Binary path: %s\n"), lpsc->lpBinaryPathName);
    _tprintf(TEXT("  Account: %s\n"), lpsc->lpServiceStartName);

    if (lpsd->lpDescription != NULL && lstrcmp(lpsd->lpDescription, TEXT("")) != 0)
        _tprintf(TEXT("  Description: %s\n"), lpsd->lpDescription);
    if (lpsc->lpLoadOrderGroup != NULL && lstrcmp(lpsc->lpLoadOrderGroup, TEXT("")) != 0)
        _tprintf(TEXT("  Load order group: %s\n"), lpsc->lpLoadOrderGroup);
    if (lpsc->dwTagId != 0)
        _tprintf(TEXT("  Tag ID: %d\n"), lpsc->dwTagId);
    if (lpsc->lpDependencies != NULL && lstrcmp(lpsc->lpDependencies, TEXT("")) != 0)
        _tprintf(TEXT("  Dependencies: %s\n"), lpsc->lpDependencies);
 
    LocalFree(lpsc); 
    LocalFree(lpsd);

cleanup:
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="a76cf-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a76cf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a76cf-110">Configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="a76cf-110">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="a76cf-111">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="a76cf-111">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



