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
# <a name="loading-vds"></a>Caricamento di VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

**Per caricare e inizializzare VDS**

1.  Rilascia interfacce non null.
2.  Chiamare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)o [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) per ottenere un puntatore all'oggetto del caricatore del servizio.

    **CLSCTX \_ Non \_** è possibile specificare disable AAA in questa chiamata. Se viene chiamato [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , non è possibile specificare **EOAC \_ disabilitare \_ AAA** nel parametro *dwCapabilities* .

3.  Chiamare il metodo [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) per caricare VDS.

    Il passaggio di **null** come primo parametro consente di caricare e inizializzare VDS nell'host locale.

4.  Chiamare il metodo [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) per attendere il completamento dell'inizializzazione VDS.

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

[Oggetti installazione e servizio](startup-and-service-objects.md)
</dt> </dl>

 

 
