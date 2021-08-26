---
description: L'interfaccia IWbemObjectSink crea un'interfaccia sink in grado di ricevere tutti i tipi di notifiche all'interno del modello di programmazione WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interfaccia IWbemObjectSink (Wbemcli.h)
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
ms.openlocfilehash: 6bfce21edca92c95276f382d16007f8b319b9f3b80fc5c3c721f7232ea0b4618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996541"
---
# <a name="iwbemobjectsink-interface"></a>Interfaccia IWbemObjectSink

**L'interfaccia IWbemObjectSink** crea un'interfaccia sink in grado di ricevere tutti i tipi di notifiche all'interno del modello di programmazione WMI. I client devono implementare questa interfaccia per ricevere sia i risultati dei metodi [asincroni](making-an-asynchronous-call-with-c--.md) di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)sia tipi specifici di notifiche degli eventi. I provider utilizzano, ma non implementano questa interfaccia per fornire eventi e oggetti a WMI.

In genere, i provider chiamano un'implementazione fornita da WMI. In questi casi, chiamare [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) per fornire oggetti al servizio WMI. Successivamente, chiamare [**SetStatus per**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) indicare la fine della sequenza di notifica. È anche possibile chiamare **SetStatus** per indicare errori quando il sink non ha oggetti.

Durante la programmazione di client asincroni di WMI, l'utente fornisce l'implementazione di . WMI chiama i metodi per recapitare oggetti e impostare lo stato del risultato.

> [!Note]  
> Se un'applicazione client passa la stessa interfaccia sink in due diverse chiamate asincrone sovrapposte, WMI non garantisce l'ordine del callback. Le applicazioni client che effettuano chiamate asincrone sovrapposte devono passare oggetti sink diversi o serializzare le chiamate.

 

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrono anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

## <a name="members"></a>Membri

**L'interfaccia IWbemObjectSink** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWbemObjectSink** include questi metodi.



| Metodo                                         | Descrizione                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Indicare**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Riceve gli oggetti di notifica.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Chiamato dalle origini per indicare la fine di una sequenza di notifica o per inviare altri codici di stato al sink.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si implementa un sink della sottoscrizione di eventi (**IWbemObjectSink** o [**IWbemEventSink**](iwbemeventsink.md)), non chiamare wmi dall'interno dei metodi [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) o [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) nell'oggetto sink. Ad esempio, la chiamata [**di IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) per annullare il sink dall'interno di un'implementazione di [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) può interferire con lo stato WMI. Per annullare una sottoscrizione di eventi, impostare un flag e chiamare **IWbemServices::CancelAsyncCall** da un altro thread o oggetto. Per le implementazioni non correlate a un sink di evento, ad esempio il recupero di oggetti, enumerazioni e query, è possibile richiamare WMI.

Le implementazioni del sink devono elaborare la notifica degli eventi entro 100 MSEC perché il thread WMI che recapita la notifica degli eventi non può eseguire altre operazioni fino al completamento dell'elaborazione dell'oggetto sink. Se la notifica richiede una grande quantità di elaborazione, il sink può usare una coda interna per un altro thread per gestire l'elaborazione.

## <a name="examples"></a>Esempio

L'esempio di codice seguente è una semplice implementazione di un sink di oggetto. Questo esempio può essere usato con [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) o [**IWbemServices::CreateInstanceEnumAsync per**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) ricevere le istanze restituite:


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
| Intestazione<br/>                   | <dl> <dt>Wbemcli.h (includere Wbemidl.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API COM per WMI](com-api-for-wmi.md)
</dt> <dt>

[Esecuzione di una chiamata asincrona con C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




