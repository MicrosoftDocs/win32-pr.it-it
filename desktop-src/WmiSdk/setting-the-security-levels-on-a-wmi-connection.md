---
description: Dopo aver recuperato un puntatore a un proxy IWbemServices, è necessario impostare la sicurezza sul proxy per accedere a WMI tramite il proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Impostazione dei livelli di sicurezza in una connessione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c2c4a492d4b40410b42fd9a94f22d346617a84d3baaa0679db325452a69c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315325"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Impostazione dei livelli di sicurezza in una connessione WMI

Dopo aver recuperato un puntatore a un proxy [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è necessario impostare la sicurezza sul proxy per accedere a WMI tramite il proxy. È necessario impostare la sicurezza perché il proxy **IWbemServices** concede l'accesso a un oggetto out-of-process. In generale, la sicurezza COM non consente a un processo di accedere a un altro processo se non si impostano le proprietà di sicurezza appropriate. Per altre informazioni, vedere [Impostazione della sicurezza in IWbemServices e altri proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md) Le connessioni a sistemi operativi diversi richiedono diversi livelli di autenticazione e rappresentazione. Per altre informazioni, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

Gli esempi di codice in questo argomento richiedono i riferimenti seguenti e includono \# istruzioni per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procedura seguente descrive come impostare i livelli di sicurezza in una connessione WMI.

**Per impostare i livelli di sicurezza in una connessione WMI**

-   Impostare i livelli di sicurezza nel proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Nell'esempio di codice seguente viene descritto un modo comune per chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

Dopo aver impostato i livelli di sicurezza per il puntatore [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è possibile accedere alle varie funzionalità di WMI. Al termine dell'uso di WMI, è necessario arrestare l'applicazione. Per altre informazioni, vedere [Pulizia e arresto di un'applicazione WMI.](cleaning-up-and-shutting-down-a-wmi-application.md)

 

 
