---
description: 'Le chiamate semisincrono sono le modalità consigliate per chiamare i metodi WMI, ad esempio IWbemServices:: ExecMethod e i metodi del provider, ad esempio il metodo CHKDSK della \_ classe disco logico Win32.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Esecuzione di una chiamata semisincrono con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529616"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Esecuzione di una chiamata semisincrono con C++

Le chiamate semisincrono sono le modalità consigliate per chiamare i metodi WMI, ad esempio [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) e i metodi del provider, ad esempio il [**metodo CHKDSK della \_ classe disco logico Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

Uno svantaggio dell'elaborazione sincrona è che il thread chiamante viene bloccato fino al completamento della chiamata. Il blocco può causare un ritardo nel tempo di elaborazione. Al contrario, una chiamata asincrona deve implementare [**SWbemSink**](swbemsink.md) nello script. In C++, il codice asincrono deve implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) , usare più thread e controllare il flusso di informazioni al chiamante. I set di risultati di grandi dimensioni delle query, ad esempio, possono richiedere una quantità di tempo considerevole per il recapito e forzare il chiamante a spendere risorse di sistema significative per gestire il recapito.

L'elaborazione semisincrono risolve sia il blocco del thread che i problemi di recapito non controllato eseguendo il polling di un oggetto di stato speciale che implementa l'interfaccia [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) . Tramite **IWbemCallResult** è possibile migliorare la velocità e l'efficienza di query, enumerazioni e notifiche degli eventi.

Nella procedura seguente viene descritto come eseguire una chiamata semisincrono con l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

**Per eseguire una chiamata semisincrono con l'interfaccia IWbemServices**

1.  Rendere la chiamata normale, ma con il **flag WBEM \_ \_ restituire \_ immediatamente** il flag impostato nel parametro *iFlags* .

    È possibile combinare **\_ \_ \_ immediatamente la restituzione del flag WBEM** con altri flag validi per il metodo specifico. Usare, ad esempio, il flag **WBEM di \_ \_ \_ sola trasmissione** per tutte le chiamate che restituiscono enumeratori. L'impostazione di questi flag in combinazione consente di risparmiare tempo e spazio e di migliorare la velocità di risposta.

2.  Eseguire il polling dei risultati.

    Se si chiama un metodo che restituisce un enumeratore, ad esempio [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) o [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), è possibile eseguire il polling degli enumeratori con i metodi [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) . La chiamata **IEnumWbemClassObject:: NextAsync** non blocca e restituisce immediatamente un risultato. In background, WMI inizia a recapitare il numero richiesto di oggetti chiamando [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). WMI arresta quindi e attende un'altra chiamata **NextAsync** .

    Se si chiama un metodo che non restituisce un enumeratore, ad esempio [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), è necessario impostare il parametro *ppCallResult* su un puntatore valido. Usare [**IWbemCallResult:: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) sul puntatore restituito per recuperare l' **\_ \_ \_ Errore WBEM**.

3.  Terminare la chiamata.

    Per una chiamata che restituisce un enumeratore, WMI chiama [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) per segnalare il completamento dell'operazione. Se non è necessario l'intero risultato, rilasciare l'enumeratore chiamando il metodo [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . La chiamata della **versione** restituisce in WMI l'annullamento del recapito di tutti gli oggetti che rimangono.

    Per una chiamata che non usa un enumeratore, recuperare l'oggetto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) tramite il parametro *plStatus* del metodo.

Nell'esempio di codice C++ in questo argomento sono necessarie le \# istruzioni include seguenti per la compilazione corretta.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come eseguire una chiamata semisincrono a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 
