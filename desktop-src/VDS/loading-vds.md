---
description: Caricamento di VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Caricamento di VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec6a757b57c8e06e53862b3d36b9d54f291e4b07693dff008ecc2bbbb961c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125941"
---
# <a name="loading-vds"></a>Caricamento di VDS

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

**Per caricare e inizializzare VDS**

1.  Rilasciare interfacce non Null.
2.  Chiamare la [**funzione CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)o [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) per ottenere un puntatore all'oggetto caricatore del servizio.

    **CLSCTX \_ Disable \_ AAA** non può essere specificato in questa chiamata. Se [**viene chiamato CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) non è possibile specificare **DISABLE \_ \_ AAA EOAC** nel *parametro dwCapabilities.*

3.  Chiamare il [**metodo IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) per caricare VDS.

    Il **passaggio di NULL** come primo parametro carica e inizializza VDS nell'host locale.

4.  Chiamare il [**metodo IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) per attendere il completamento dell'inizializzazione di VDS.

Nell'esempio di codice seguente viene inizializzato il servizio che restituisce un puntatore all'oggetto servizio.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Oggetti di installazione e di servizio](startup-and-service-objects.md)
</dt> </dl>

 

 
