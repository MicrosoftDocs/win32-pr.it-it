---
description: Un programma di configurazione del servizio usa la funzione OpenService per ottenere un handle con accesso SERVICE \_ QUERY CONFIG a un oggetto servizio \_ installato.
ms.assetid: e6633dc9-c9b6-457d-8adc-e751ec9cf71d
title: Esecuzione di query su una configurazione dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8eb8abd0792107c4c10757db22d2d96253837623138c9c5d6d000c25d4d39eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889317"
---
# <a name="querying-a-services-configuration"></a>Esecuzione di query sulla configurazione di un servizio

Un [programma di configurazione del](service-configuration-programs.md) servizio usa la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) per ottenere un handle con accesso SERVICE \_ QUERY CONFIG a un oggetto servizio \_ installato. Il programma può quindi usare l'handle dell'oggetto servizio nelle funzioni [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per recuperare la configurazione corrente del servizio.

Nell'esempio seguente la funzione DoQuerySvc usa [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per recuperare le informazioni di configurazione, quindi scrive le informazioni selezionate nella console. La variabile szSvcName è una variabile globale che contiene il nome del servizio. Per l'esempio completo che imposta questa variabile, vedere [SvcConfig.cpp](svcconfig-cpp.md).


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Service Configuration](service-configuration.md)
</dt> <dt>

[Esempio di servizio completo](the-complete-service-sample.md)
</dt> </dl>

 

 



