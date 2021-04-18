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
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="63bf4-103">Interfaccia IWbemObjectSink</span><span class="sxs-lookup"><span data-stu-id="63bf4-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="63bf4-104">L'interfaccia **IWbemObjectSink** crea un'interfaccia di sink che può ricevere tutti i tipi di notifiche all'interno del modello di programmazione WMI.</span><span class="sxs-lookup"><span data-stu-id="63bf4-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="63bf4-105">I client devono implementare questa interfaccia per ricevere i risultati dei [metodi asincroni](making-an-asynchronous-call-with-c--.md) di [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)e i tipi specifici di notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="63bf4-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="63bf4-106">I provider utilizzano, ma non implementano questa interfaccia per fornire eventi e oggetti a WMI.</span><span class="sxs-lookup"><span data-stu-id="63bf4-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="63bf4-107">In genere, i provider chiamano un'implementazione fornita da WMI.</span><span class="sxs-lookup"><span data-stu-id="63bf4-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="63bf4-108">In questi casi, la chiamata a [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) di fornire oggetti al servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="63bf4-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="63bf4-109">Successivamente, chiamare [**sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) per indicare la fine della sequenza di notifica.</span><span class="sxs-lookup"><span data-stu-id="63bf4-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="63bf4-110">È inoltre possibile chiamare **sestatus** per indicare errori quando il sink non dispone di alcun oggetto.</span><span class="sxs-lookup"><span data-stu-id="63bf4-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="63bf4-111">Quando si programmano client asincroni di WMI, l'utente fornisce l'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="63bf4-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="63bf4-112">WMI chiama i metodi per fornire oggetti e impostare lo stato del risultato.</span><span class="sxs-lookup"><span data-stu-id="63bf4-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="63bf4-113">Se un'applicazione client passa la stessa interfaccia di sink in due diverse chiamate asincrone sovrapposte, WMI non garantisce l'ordine di callback.</span><span class="sxs-lookup"><span data-stu-id="63bf4-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="63bf4-114">Le applicazioni client che effettuano chiamate asincrone sovrapposte devono passare oggetti sink diversi o serializzare le chiamate.</span><span class="sxs-lookup"><span data-stu-id="63bf4-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="63bf4-115">Poiché è possibile che la chiamata al sink non venga restituita allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="63bf4-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="63bf4-116">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="63bf4-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="63bf4-117">Membri</span><span class="sxs-lookup"><span data-stu-id="63bf4-117">Members</span></span>

<span data-ttu-id="63bf4-118">L'interfaccia **IWbemObjectSink** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="63bf4-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="63bf4-119">Metodi</span><span class="sxs-lookup"><span data-stu-id="63bf4-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="63bf4-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="63bf4-120">Methods</span></span>

<span data-ttu-id="63bf4-121">L'interfaccia **IWbemObjectSink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="63bf4-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="63bf4-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="63bf4-122">Method</span></span>                                         | <span data-ttu-id="63bf4-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63bf4-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63bf4-124">**Indicare**</span><span class="sxs-lookup"><span data-stu-id="63bf4-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="63bf4-125">Riceve oggetti notifica.</span><span class="sxs-lookup"><span data-stu-id="63bf4-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="63bf4-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="63bf4-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="63bf4-127">Chiamato dalle origini per indicare la fine di una sequenza di notifica o per inviare altri codici di stato al sink.</span><span class="sxs-lookup"><span data-stu-id="63bf4-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63bf4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="63bf4-128">Remarks</span></span>

<span data-ttu-id="63bf4-129">Quando si implementa un sink di sottoscrizione di eventi (**IWbemObjectSink** o [**IWbemEventSink**](iwbemeventsink.md)), non eseguire chiamate in WMI dall'interno dei metodi di [**indicazione**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) o di [**stato**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) dell'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="63bf4-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="63bf4-130">Ad esempio, la chiamata di [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) per annullare il sink dall'interno di un'implementazione di [**indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) può interferire con lo stato WMI.</span><span class="sxs-lookup"><span data-stu-id="63bf4-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="63bf4-131">Per annullare una sottoscrizione di eventi, impostare un flag e chiamare **IWbemServices:: CancelAsyncCall** da un altro thread o oggetto.</span><span class="sxs-lookup"><span data-stu-id="63bf4-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="63bf4-132">Per le implementazioni non correlate a un sink di evento, ad esempio il recupero di oggetti, enum e query, è possibile richiamarlo in WMI.</span><span class="sxs-lookup"><span data-stu-id="63bf4-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="63bf4-133">Le implementazioni di sink devono elaborare la notifica degli eventi entro 100 MSEC perché il thread WMI che recapita la notifica degli eventi non può eseguire altre operazioni finché l'oggetto sink non ha completato l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="63bf4-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="63bf4-134">Se la notifica richiede una grande quantità di elaborazione, il sink può utilizzare una coda interna per gestire l'elaborazione da parte di un altro thread.</span><span class="sxs-lookup"><span data-stu-id="63bf4-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="63bf4-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="63bf4-135">Examples</span></span>

<span data-ttu-id="63bf4-136">L'esempio di codice seguente è un'implementazione semplice di un sink di oggetti.</span><span class="sxs-lookup"><span data-stu-id="63bf4-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="63bf4-137">Questo esempio può essere usato con [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) per ricevere le istanze restituite:</span><span class="sxs-lookup"><span data-stu-id="63bf4-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="63bf4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63bf4-138">Requirements</span></span>



| <span data-ttu-id="63bf4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="63bf4-139">Requirement</span></span> | <span data-ttu-id="63bf4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="63bf4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63bf4-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63bf4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="63bf4-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63bf4-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="63bf4-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63bf4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="63bf4-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63bf4-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="63bf4-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63bf4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="63bf4-146"><dt>Wbemcli. h (include Wbemidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63bf4-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="63bf4-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="63bf4-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="63bf4-148"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63bf4-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="63bf4-149">DLL</span><span class="sxs-lookup"><span data-stu-id="63bf4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63bf4-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63bf4-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="63bf4-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63bf4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63bf4-152">API COM per WMI</span><span class="sxs-lookup"><span data-stu-id="63bf4-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="63bf4-153">Esecuzione di una chiamata asincrona con C++</span><span class="sxs-lookup"><span data-stu-id="63bf4-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="63bf4-154">Impostazione della sicurezza per una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="63bf4-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="63bf4-155">Ricezione di eventi per la durata dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="63bf4-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




