---
description: Dopo aver impostato i livelli di sicurezza per il puntatore IWbemServices, è possibile accedere alle varie funzionalità di WMI. Al termine dell'uso di WMI, è necessario arrestare l'applicazione.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Pulizia e arresto di un'applicazione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 296d2093b16491bcb600438d781fa833a09754fdc5d0cc8cc83feb710a6d2727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120911"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Pulizia e arresto di un'applicazione WMI

Dopo aver impostato i livelli di sicurezza per il puntatore [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è possibile accedere alle varie funzionalità di WMI. Al termine dell'uso di WMI, è necessario arrestare l'applicazione.

La procedura seguente descrive come pulire e arrestare un'applicazione WMI.

**Per pulire e arrestare un'applicazione WMI**

1.  Rilasciare tutte le interfacce COM aperte.

    Le due interfacce principali da ricordare per il rilascio sono [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

2.  Chiamare [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

    Come per tutte le applicazioni COM, è necessario chiamare [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) alla fine dell'applicazione.

3.  Uscire dall'applicazione.

    Nell'esempio di codice seguente viene illustrato come uscire da un'applicazione client WMI.

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > La `pSvc` variabile è di tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)e la \* variabile pLoc è di tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

L'inizializzazione di COM, l'accesso a WMI e la chiusura dell'applicazione sono stati completati. Per altre informazioni, vedere [Esempio: Creazione di un'applicazione WMI.](example-creating-a-wmi-application.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
