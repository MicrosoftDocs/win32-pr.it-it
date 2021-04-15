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
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="35502-103">Esecuzione di una chiamata semisincrono con C++</span><span class="sxs-lookup"><span data-stu-id="35502-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="35502-104">Le chiamate semisincrono sono le modalità consigliate per chiamare i metodi WMI, ad esempio [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) e i metodi del provider, ad esempio il [**metodo CHKDSK della \_ classe disco logico Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="35502-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="35502-105">Uno svantaggio dell'elaborazione sincrona è che il thread chiamante viene bloccato fino al completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="35502-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="35502-106">Il blocco può causare un ritardo nel tempo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="35502-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="35502-107">Al contrario, una chiamata asincrona deve implementare [**SWbemSink**](swbemsink.md) nello script.</span><span class="sxs-lookup"><span data-stu-id="35502-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="35502-108">In C++, il codice asincrono deve implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) , usare più thread e controllare il flusso di informazioni al chiamante.</span><span class="sxs-lookup"><span data-stu-id="35502-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="35502-109">I set di risultati di grandi dimensioni delle query, ad esempio, possono richiedere una quantità di tempo considerevole per il recapito e forzare il chiamante a spendere risorse di sistema significative per gestire il recapito.</span><span class="sxs-lookup"><span data-stu-id="35502-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="35502-110">L'elaborazione semisincrono risolve sia il blocco del thread che i problemi di recapito non controllato eseguendo il polling di un oggetto di stato speciale che implementa l'interfaccia [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .</span><span class="sxs-lookup"><span data-stu-id="35502-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="35502-111">Tramite **IWbemCallResult** è possibile migliorare la velocità e l'efficienza di query, enumerazioni e notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="35502-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="35502-112">Nella procedura seguente viene descritto come eseguire una chiamata semisincrono con l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="35502-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="35502-113">**Per eseguire una chiamata semisincrono con l'interfaccia IWbemServices**</span><span class="sxs-lookup"><span data-stu-id="35502-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="35502-114">Rendere la chiamata normale, ma con il **flag WBEM \_ \_ restituire \_ immediatamente** il flag impostato nel parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="35502-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="35502-115">È possibile combinare **\_ \_ \_ immediatamente la restituzione del flag WBEM** con altri flag validi per il metodo specifico.</span><span class="sxs-lookup"><span data-stu-id="35502-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="35502-116">Usare, ad esempio, il flag **WBEM di \_ \_ \_ sola trasmissione** per tutte le chiamate che restituiscono enumeratori.</span><span class="sxs-lookup"><span data-stu-id="35502-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="35502-117">L'impostazione di questi flag in combinazione consente di risparmiare tempo e spazio e di migliorare la velocità di risposta.</span><span class="sxs-lookup"><span data-stu-id="35502-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="35502-118">Eseguire il polling dei risultati.</span><span class="sxs-lookup"><span data-stu-id="35502-118">Poll for your results.</span></span>

    <span data-ttu-id="35502-119">Se si chiama un metodo che restituisce un enumeratore, ad esempio [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) o [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), è possibile eseguire il polling degli enumeratori con i metodi [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) .</span><span class="sxs-lookup"><span data-stu-id="35502-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="35502-120">La chiamata **IEnumWbemClassObject:: NextAsync** non blocca e restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="35502-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="35502-121">In background, WMI inizia a recapitare il numero richiesto di oggetti chiamando [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="35502-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="35502-122">WMI arresta quindi e attende un'altra chiamata **NextAsync** .</span><span class="sxs-lookup"><span data-stu-id="35502-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="35502-123">Se si chiama un metodo che non restituisce un enumeratore, ad esempio [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), è necessario impostare il parametro *ppCallResult* su un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="35502-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="35502-124">Usare [**IWbemCallResult:: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) sul puntatore restituito per recuperare l' **\_ \_ \_ Errore WBEM**.</span><span class="sxs-lookup"><span data-stu-id="35502-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="35502-125">Terminare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="35502-125">Finish your call.</span></span>

    <span data-ttu-id="35502-126">Per una chiamata che restituisce un enumeratore, WMI chiama [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) per segnalare il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="35502-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="35502-127">Se non è necessario l'intero risultato, rilasciare l'enumeratore chiamando il metodo [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="35502-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="35502-128">La chiamata della **versione** restituisce in WMI l'annullamento del recapito di tutti gli oggetti che rimangono.</span><span class="sxs-lookup"><span data-stu-id="35502-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="35502-129">Per una chiamata che non usa un enumeratore, recuperare l'oggetto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) tramite il parametro *plStatus* del metodo.</span><span class="sxs-lookup"><span data-stu-id="35502-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="35502-130">Nell'esempio di codice C++ in questo argomento sono necessarie le \# istruzioni include seguenti per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="35502-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="35502-131">Nell'esempio di codice seguente viene illustrato come eseguire una chiamata semisincrono a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="35502-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="35502-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35502-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35502-133">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="35502-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
