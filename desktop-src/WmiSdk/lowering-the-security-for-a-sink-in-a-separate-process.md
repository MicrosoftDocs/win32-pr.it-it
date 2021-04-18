---
description: Strumentazione gestione Windows (WMI) può creare il sink per ricevere callback asincroni per un'applicazione client in un processo separato.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Riduzione della sicurezza per un sink in un processo separato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314597"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="8fd86-103">Riduzione della sicurezza per un sink in un processo separato</span><span class="sxs-lookup"><span data-stu-id="8fd86-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="8fd86-104">Strumentazione gestione Windows (WMI) può creare il sink per ricevere callback asincroni per un'applicazione client in un processo separato.</span><span class="sxs-lookup"><span data-stu-id="8fd86-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="8fd86-105">Il processo separato è Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="8fd86-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="8fd86-106">Usare l'interfaccia [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="8fd86-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="8fd86-107">**IWbemUnsecuredApartment** consente di controllare se Unsecapp.exe autentica i callback per il sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="8fd86-108">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="8fd86-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="8fd86-109">È quindi possibile abbassare la sicurezza del processo e WMI può accedere al sink senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="8fd86-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="8fd86-110">Per supportare questa tecnica, WMI fornisce il processo Unsecapp.exe per funzionare come processo separato.</span><span class="sxs-lookup"><span data-stu-id="8fd86-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="8fd86-111">È possibile ospitare Unsecapp.exe con una chiamata all'interfaccia [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .</span><span class="sxs-lookup"><span data-stu-id="8fd86-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="8fd86-112">L'interfaccia [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) consente a un'applicazione client di creare un processo dedicato separato che esegue Unsecapp.exe per l'hosting di un'implementazione di [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd86-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="8fd86-113">Il processo dedicato può chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per concedere l'accesso WMI al processo dedicato senza compromettere la sicurezza del processo principale.</span><span class="sxs-lookup"><span data-stu-id="8fd86-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="8fd86-114">Dopo l'inizializzazione, il processo dedicato funge da intermediario tra il processo principale e WMI.</span><span class="sxs-lookup"><span data-stu-id="8fd86-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="8fd86-115">Nella procedura seguente viene descritto come eseguire una chiamata asincrona con [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="8fd86-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="8fd86-116">**Per eseguire una chiamata asincrona con IUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="8fd86-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="8fd86-117">Creare un processo dedicato con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="8fd86-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="8fd86-118">Nell'esempio di codice seguente viene chiamato [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un processo dedicato.</span><span class="sxs-lookup"><span data-stu-id="8fd86-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="8fd86-119">Creare un'istanza dell'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="8fd86-120">Nell'esempio di codice seguente viene creato un nuovo oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="8fd86-121">Creare uno stub per il sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="8fd86-122">Uno Stub è una funzione wrapper prodotta dal sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="8fd86-123">Nell'esempio di codice seguente viene chiamato [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) per creare uno stub per il sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="8fd86-124">Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per il wrapper e richiedere un puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd86-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="8fd86-125">Nell'esempio di codice seguente viene chiamato [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e viene richiesto un puntatore all'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd86-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="8fd86-126">Rilasciare il puntatore all'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="8fd86-127">È possibile rilasciare il puntatore all'oggetto perché lo stub è ora proprietario del puntatore.</span><span class="sxs-lookup"><span data-stu-id="8fd86-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="8fd86-128">Nell'esempio di codice seguente viene rilasciato il puntatore all'oggetto sink.</span><span class="sxs-lookup"><span data-stu-id="8fd86-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="8fd86-129">Utilizzare lo stub in qualsiasi chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="8fd86-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="8fd86-130">Al termine della chiamata, rilasciare il conteggio dei riferimenti locali.</span><span class="sxs-lookup"><span data-stu-id="8fd86-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="8fd86-131">Nell'esempio di codice seguente viene utilizzato lo stub in una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="8fd86-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="8fd86-132">In alcuni casi potrebbe essere necessario annullare una chiamata asincrona dopo aver effettuato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="8fd86-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="8fd86-133">Se è necessario annullare la chiamata, annullare la chiamata con lo stesso puntatore che ha originariamente effettuato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="8fd86-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="8fd86-134">Nell'esempio di codice seguente viene illustrato come annullare una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="8fd86-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="8fd86-135">Rilasciare il conteggio dei riferimenti locale al termine dell'utilizzo della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="8fd86-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="8fd86-136">Assicurarsi di rilasciare il puntatore *pStubSink* solo dopo aver verificato che non è necessario annullare la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="8fd86-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="8fd86-137">Inoltre, non rilasciare *pStubSink* dopo che WMI rilascia il puntatore di sink *pSink* .</span><span class="sxs-lookup"><span data-stu-id="8fd86-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="8fd86-138">Il rilascio di *pStubSink* dopo *pSink* crea un conteggio dei riferimenti circolari in cui sia il sink che lo stub rimarranno sempre in memoria.</span><span class="sxs-lookup"><span data-stu-id="8fd86-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="8fd86-139">Al contrario, una posizione possibile per rilasciare il puntatore si trova nella chiamata [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , eseguita da WMI per segnalare che la chiamata asincrona originale è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8fd86-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="8fd86-140">Al termine, annullare l'inizializzazione di COM con una chiamata a [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="8fd86-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="8fd86-141">Nell'esempio di codice seguente viene illustrato come chiamare [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="8fd86-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="8fd86-142">Gli esempi di codice in questo argomento richiedono il riferimento e l' \# istruzione include seguenti per la corretta compilazione.</span><span class="sxs-lookup"><span data-stu-id="8fd86-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="8fd86-143">Per ulteriori informazioni sulla funzione e sui parametri [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , vedere la documentazione [com](../cossdk/component-services-portal.md) in Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8fd86-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
