---
description: L'interfaccia IWbemObjectSink crea un'interfaccia di sink che può ricevere tutti i tipi di notifiche all'interno del modello di programmazione WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interfaccia IWbemObjectSink (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310351"
---
# <a name="iwbemobjectsink-interface"></a>Interfaccia IWbemObjectSink

L'interfaccia **IWbemObjectSink** crea un'interfaccia di sink che può ricevere tutti i tipi di notifiche all'interno del modello di programmazione WMI. I client devono implementare questa interfaccia per ricevere i risultati dei [metodi asincroni](making-an-asynchronous-call-with-c--.md) di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)e i tipi specifici di notifiche degli eventi. I provider utilizzano, ma non implementano questa interfaccia per fornire eventi e oggetti a WMI.

In genere, i provider chiamano un'implementazione fornita da WMI. In questi casi, la chiamata a [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) di fornire oggetti al servizio WMI. Successivamente, chiamare [**sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) per indicare la fine della sequenza di notifica. È inoltre possibile chiamare **sestatus** per indicare errori quando il sink non dispone di alcun oggetto.

Quando si programmano client asincroni di WMI, l'utente fornisce l'implementazione di. WMI chiama i metodi per fornire oggetti e impostare lo stato del risultato.

> [!Note]  
> Se un'applicazione client passa la stessa interfaccia di sink in due diverse chiamate asincrone sovrapposte, WMI non garantisce l'ordine di callback. Le applicazioni client che effettuano chiamate asincrone sovrapposte devono passare oggetti sink diversi o serializzare le chiamate.

 

> [!Note]  
> Poiché è possibile che la chiamata al sink non venga restituita allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

## <a name="members"></a>Membri

L'interfaccia **IWbemObjectSink** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWbemObjectSink** dispone di questi metodi.



| Metodo                                         | Descrizione                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Indicare**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Riceve oggetti notifica.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Chiamato dalle origini per indicare la fine di una sequenza di notifica o per inviare altri codici di stato al sink.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si implementa un sink di sottoscrizione di eventi (**IWbemObjectSink** o [**IWbemEventSink**](iwbemeventsink.md)), non eseguire chiamate in WMI dall'interno dei metodi di [**indicazione**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) o di [**stato**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) dell'oggetto sink. Ad esempio, la chiamata di [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) per annullare il sink dall'interno di un'implementazione di [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) può interferire con lo stato WMI. Per annullare una sottoscrizione di eventi, impostare un flag e chiamare **IWbemServices:: CancelAsyncCall** da un altro thread o oggetto. Per le implementazioni non correlate a un sink di evento, ad esempio il recupero di oggetti, enum e query, è possibile richiamarlo in WMI.

Le implementazioni di sink devono elaborare la notifica degli eventi entro 100 MSEC perché il thread WMI che recapita la notifica degli eventi non può eseguire altre operazioni finché l'oggetto sink non ha completato l'elaborazione. Se la notifica richiede una grande quantità di elaborazione, il sink può utilizzare una coda interna per gestire l'elaborazione da parte di un altro thread.

## <a name="examples"></a>Esempio

L'esempio di codice seguente è un'implementazione semplice di un sink di oggetti. Questo esempio può essere usato con [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) per ricevere le istanze restituite:


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                           |
| Intestazione<br/>                   | <dl> <dt>Wbemcli. h (include Wbemidl. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API COM per WMI](com-api-for-wmi.md)
</dt> <dt>

[Esecuzione di una chiamata asincrona con C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




