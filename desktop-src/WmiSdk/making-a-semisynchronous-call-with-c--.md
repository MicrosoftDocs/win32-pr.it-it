---
description: Le chiamate semisincronose sono il metodo consigliato per chiamare metodi WMI, ad esempio IWbemServices::ExecMethod e metodi provider, ad esempio il metodo Chkdsk della classe \_ LogicalDisk Win32.
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Esecuzione di una chiamata semisincrona con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a550c5ad659ab9b640a1fcb3060b5f6cc7671f80c209d238cd859ad0ef6f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050699"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Esecuzione di una chiamata semisincrona con C++

Le chiamate semisincronose sono il metodo consigliato per chiamare metodi WMI, ad esempio [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) e metodi provider, ad esempio il metodo Chkdsk della classe [**\_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk)

Uno svantaggio dell'elaborazione sincrona è che il thread chiamante viene bloccato fino al completamento della chiamata. Il blocco può causare un ritardo nel tempo di elaborazione. Al contrario, una chiamata asincrona deve [**implementare SWbemSink**](swbemsink.md) nello script. In C++, il codice asincrono deve implementare [**l'interfaccia IWbemObjectSink,**](iwbemobjectsink.md) usare più thread e controllare il flusso di informazioni al chiamante. I set di risultati di grandi dimensioni delle query, ad esempio, possono richiedere una notevole quantità di tempo per recapitare e forzare il chiamante a impiegare risorse di sistema significative per gestire il recapito.

L'elaborazione semisincrona risolve sia i problemi di blocco del thread che di recapito non controllato tramite il polling di un oggetto di stato speciale che implementa [**l'interfaccia IWbemCallResult.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) Tramite **IWbemCallResult** è possibile migliorare la velocità e l'efficienza di query, enumerazioni e notifiche degli eventi.

La procedura seguente descrive come effettuare una chiamata semisincrona con [**l'interfaccia IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

**Per effettuare una chiamata semisincrona con l'interfaccia IWbemServices**

1.  Effettuare la chiamata come di consueto, ma con il flag **WBEM \_ FLAG \_ RETURN \_ IMMEDIATELY** impostato nel *parametro IFlags.*

    È possibile combinare **WBEM \_ FLAG \_ RETURN \_ IMMEDIATELY** con altri flag validi per il metodo specifico. Ad esempio, usare il flag **WBEM \_ FLAG \_ FORWARD \_ ONLY** per tutte le chiamate che restituiscono enumeratori. L'impostazione di questi flag in combinazione consente di risparmiare tempo e spazio e migliora la velocità di risposta.

2.  Eseguire il polling dei risultati.

    Se si chiama un metodo che restituisce un enumeratore, ad esempio [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) o [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), è possibile eseguire il polling degli enumeratori con i metodi [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject::NextAsync.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) La **chiamata IEnumWbemClassObject::NextAsync** non è bloccante e restituisce immediatamente . In background, WMI inizia a recapitare il numero richiesto di oggetti chiamando [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). WMI si arresta e attende **un'altra chiamata NextAsync.**

    Se si chiama un metodo che non restituisce un enumeratore, ad esempio [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), è necessario impostare il *parametro ppCallResult* su un puntatore valido. Usare [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) sul puntatore restituito per recuperare **WBEM \_ S NO \_ \_ ERROR**.

3.  Completare la chiamata.

    Per una chiamata che restituisce un enumeratore, WMI chiama [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) per segnalare il completamento dell'operazione. Se non è necessario l'intero risultato, rilasciare l'enumeratore chiamando il metodo [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) La **chiamata a Release** comporta l'annullamento del recapito di tutti gli oggetti che rimangono in WMI.

    Per una chiamata che non usa un enumeratore, recuperare [**l'oggetto GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) tramite il *parametro plStatus* del metodo.

L'esempio di codice C++ in questo argomento richiede che le istruzioni \# include seguenti vengano compilate correttamente.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come effettuare una chiamata semisincronosa a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


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

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

 
