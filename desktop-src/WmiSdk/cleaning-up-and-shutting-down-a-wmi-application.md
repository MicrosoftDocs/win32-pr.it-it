---
description: Dopo aver impostato i livelli di sicurezza per il puntatore IWbemServices, è possibile accedere alle varie funzionalità di WMI. Al termine dell'utilizzo di WMI, è necessario arrestare l'applicazione.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Pulizia e arresto di un'applicazione WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967975"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a>Pulizia e arresto di un'applicazione WMI

Dopo aver impostato i livelli di sicurezza per il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , è possibile accedere alle varie funzionalità di WMI. Al termine dell'utilizzo di WMI, è necessario arrestare l'applicazione.

Nella procedura riportata di seguito viene descritto come eseguire la pulizia e l'arresto di un'applicazione WMI.

**Per pulire e arrestare un'applicazione WMI**

1.  Rilascia le interfacce COM aperte.

    Le due interfacce primarie che è necessario ricordare di rilasciare sono [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

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
    > La `pSvc` variabile è di tipo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* e la variabile PLoc è di tipo [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .

     

A questo punto è stato inizializzato correttamente COM, si è eseguito l'accesso a WMI ed è stata chiusa l'applicazione. Per ulteriori informazioni, vedere [esempio: creazione di un'applicazione WMI](example-creating-a-wmi-application.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
