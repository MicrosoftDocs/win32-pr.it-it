---
description: Le applicazioni WMI scritte in C++ possono eseguire chiamate asincrone utilizzando molti dei metodi dell'interfaccia COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Esecuzione di una chiamata asincrona con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318868"
---
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="28c81-103">Esecuzione di una chiamata asincrona con C++</span><span class="sxs-lookup"><span data-stu-id="28c81-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="28c81-104">Le applicazioni WMI scritte in C++ possono eseguire chiamate asincrone utilizzando molti dei metodi dell'interfaccia com [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="28c81-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="28c81-105">Tuttavia, la procedura consigliata per chiamare un metodo [*WMI*](gloss-w.md) o un [*metodo del provider*](gloss-p.md) consiste nell'utilizzare chiamate semisincrono perché le chiamate semisincrono sono più sicure delle chiamate asincrone.</span><span class="sxs-lookup"><span data-stu-id="28c81-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="28c81-106">Per ulteriori informazioni, vedere [creazione di una chiamata semisincrono con C++](making-a-semisynchronous-call-with-c--.md) e [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="28c81-107">Nella procedura riportata di seguito viene descritto come eseguire una chiamata asincrona utilizzando il sink nel processo.</span><span class="sxs-lookup"><span data-stu-id="28c81-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="28c81-108">**Per eseguire una chiamata asincrona con C++**</span><span class="sxs-lookup"><span data-stu-id="28c81-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="28c81-109">Implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="28c81-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="28c81-110">Tutte le applicazioni che effettuano chiamate asincrone devono implementare [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="28c81-111">I consumer di eventi temporanei implementano anche **IWbemObjectSink** per ricevere la notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="28c81-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="28c81-112">Accedere allo spazio dei nomi WMI di destinazione.</span><span class="sxs-lookup"><span data-stu-id="28c81-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="28c81-113">Le applicazioni devono sempre chiamare la funzione COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante la fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="28c81-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="28c81-114">In caso contrario prima di effettuare una chiamata asincrona, WMI rilascia il sink dell'applicazione senza completare la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="28c81-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="28c81-115">Per ulteriori informazioni, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="28c81-116">Impostare la sicurezza per il sink.</span><span class="sxs-lookup"><span data-stu-id="28c81-116">Set the security for your sink.</span></span>

    <span data-ttu-id="28c81-117">Le chiamate asincrone creano una serie di problemi di sicurezza che potrebbe essere necessario gestire, ad esempio, per consentire l'accesso WMI all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28c81-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="28c81-118">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="28c81-119">Eseguire la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="28c81-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="28c81-120">Il metodo restituisce immediatamente il codice **di \_ \_ \_ Errore WBEM** .</span><span class="sxs-lookup"><span data-stu-id="28c81-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="28c81-121">L'applicazione può procedere con altre attività durante l'attesa del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="28c81-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="28c81-122">WMI segnala all'applicazione chiamando i metodi nell'implementazione [**IWbemObjectSink**](iwbemobjectsink.md) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28c81-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="28c81-123">Se necessario, controllare periodicamente l'implementazione per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="28c81-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="28c81-124">Le applicazioni possono ricevere notifiche dello stato intermedio impostando il parametro *è* nella chiamata asincrona **allo \_ \_ \_ stato di invio del flag WBEM**.</span><span class="sxs-lookup"><span data-stu-id="28c81-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="28c81-125">WMI segnala lo stato della chiamata impostando il parametro *è* di [**IWbemObjectSink**](iwbemobjectsink.md) **\_ sullo stato di stato \_ WBEM**.</span><span class="sxs-lookup"><span data-stu-id="28c81-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="28c81-126">Se necessario, è possibile annullare la chiamata prima di completare l'elaborazione di WMI chiamando il metodo [**IWbemServices:: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="28c81-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="28c81-127">Il metodo [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) Annulla l'elaborazione asincrona rilasciando immediatamente il puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) e garantisce che il puntatore venga rilasciato prima della restituzione di **CancelAsyncCall** .</span><span class="sxs-lookup"><span data-stu-id="28c81-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="28c81-128">Se si usa un oggetto wrapper che implementa l'interfaccia **IUnsecured** per ospitare [**IWbemObjectSink**](iwbemobjectsink.md), è possibile riscontrare alcune complicazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="28c81-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="28c81-129">Poiché l'applicazione deve passare lo stesso puntatore a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) passato nella chiamata asincrona originale, l'applicazione deve mantenere l'oggetto wrapper fino a quando non diventa chiaro che l'annullamento non è necessario.</span><span class="sxs-lookup"><span data-stu-id="28c81-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="28c81-130">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="28c81-131">Al termine, pulire i puntatori e arrestare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28c81-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="28c81-132">WMI fornisce la chiamata di stato finale tramite il metodo [**sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="28c81-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="28c81-133">Dopo l'invio dell'aggiornamento dello stato finale, WMI rilascia il sink di oggetto chiamando il metodo **Release** per la classe che implementa l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="28c81-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="28c81-134">Nell'esempio precedente si tratta del metodo **QuerySink:: Release** .</span><span class="sxs-lookup"><span data-stu-id="28c81-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="28c81-135">Se si desidera controllare la durata dell'oggetto sink, è possibile implementare il sink con un conteggio dei riferimenti iniziale pari a uno (1).</span><span class="sxs-lookup"><span data-stu-id="28c81-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="28c81-136">Se un'applicazione client passa la stessa interfaccia di sink in due diverse chiamate asincrone sovrapposte, WMI non garantisce l'ordine di callback.</span><span class="sxs-lookup"><span data-stu-id="28c81-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="28c81-137">Un'applicazione client che esegue chiamate asincrone sovrapposte deve passare oggetti sink diversi o serializzare le chiamate.</span><span class="sxs-lookup"><span data-stu-id="28c81-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="28c81-138">Nell'esempio seguente sono richieste le seguenti istruzioni Reference e \# include.</span><span class="sxs-lookup"><span data-stu-id="28c81-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="28c81-139">Nell'esempio seguente viene descritto come eseguire una query asincrona utilizzando il metodo [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , ma non vengono create impostazioni di sicurezza o viene rilasciato l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="28c81-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="28c81-140">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> <span data-ttu-id="28c81-141">Il codice precedente non viene compilato senza errori perché la classe **QuerySink** non è stata definita.</span><span class="sxs-lookup"><span data-stu-id="28c81-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="28c81-142">Per ulteriori informazioni su **QuerySink**, vedere [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="28c81-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="28c81-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28c81-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c81-144">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="28c81-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
