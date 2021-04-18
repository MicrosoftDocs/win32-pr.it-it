---
description: Come per tutte le applicazioni, WMI riceve i codici di errore dal sistema operativo Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Recupero di un codice di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309904"
---
# <a name="retrieving-an-error-code"></a><span data-ttu-id="8229b-103">Recupero di un codice di errore</span><span class="sxs-lookup"><span data-stu-id="8229b-103">Retrieving an Error Code</span></span>

<span data-ttu-id="8229b-104">Come per tutte le applicazioni, WMI riceve i codici di errore dal sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8229b-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="8229b-105">Quando si riceve un codice di errore, sono disponibili le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8229b-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="8229b-106">Esaminare il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="8229b-106">Look at the event log.</span></span>

    <span data-ttu-id="8229b-107">WMI invia messaggi di errore al servizio Registro eventi che controlla i registri eventi per determinare la provocazione di un errore.</span><span class="sxs-lookup"><span data-stu-id="8229b-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="8229b-108">È possibile utilizzare le classi supportate dal provider di [log eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider) per accedere ai registri eventi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="8229b-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="8229b-109">Recuperare il codice di errore normalmente.</span><span class="sxs-lookup"><span data-stu-id="8229b-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="8229b-110">WMI supporta le tecniche standard per recuperare i codici di errore, ovvero i codici di errore COM per C++, e gli oggetti errore nativi, ad esempio [oggetto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))o [**SWbemLastError**](swbemlasterror.md) se il provider fornisce informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="8229b-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="8229b-111">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="8229b-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="8229b-112">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="8229b-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="8229b-113">Gestione di un errore con VBScript</span><span class="sxs-lookup"><span data-stu-id="8229b-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="8229b-114">Gestione di un errore con C++</span><span class="sxs-lookup"><span data-stu-id="8229b-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="8229b-115">Gestione di un errore con VBScript</span><span class="sxs-lookup"><span data-stu-id="8229b-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="8229b-116">Se una chiamata a WMI tramite l'API di scripting per WMI genera un errore, per accedere alle informazioni sull'errore sono disponibili le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8229b-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="8229b-117">Utilizzare i meccanismi di errore nativi del linguaggio di scripting, ad esempio, in VBScript utilizzare l' [oggetto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) per supportare la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="8229b-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="8229b-118">Creare un oggetto [**SWbemLastError**](swbemlasterror.md) per ottenere una segnalazione errori.</span><span class="sxs-lookup"><span data-stu-id="8229b-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="8229b-119">Nello script seguente viene illustrato l'utilizzo dell' [oggetto Err nativo (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8229b-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="8229b-120">Quando viene specificato un valore non corretto per l'handle del processo, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="8229b-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="8229b-121">La proprietà **Description** dell' [oggetto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) è vuota quando ci si connette a WMI tramite il moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="8229b-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="8229b-122">Tuttavia, se si esegue la connessione utilizzando [**SWbemLocator**](swbemlocator.md), la descrizione è disponibile.</span><span class="sxs-lookup"><span data-stu-id="8229b-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="8229b-123">Nella tabella seguente sono elencate le proprietà dell' [oggetto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8229b-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="8229b-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8229b-124">Property</span></span>                   | <span data-ttu-id="8229b-125">Contiene</span><span class="sxs-lookup"><span data-stu-id="8229b-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="8229b-126">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8229b-126">**Description**</span></span><br/> | <span data-ttu-id="8229b-127">Descrizione dell'errore localizzata e leggibile.</span><span class="sxs-lookup"><span data-stu-id="8229b-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="8229b-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="8229b-128">**Number**</span></span><br/>      | <span data-ttu-id="8229b-129">**HRESULT** restituito dall'API di scripting per WMI.</span><span class="sxs-lookup"><span data-stu-id="8229b-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="8229b-130">**Origine**</span><span class="sxs-lookup"><span data-stu-id="8229b-130">**Source**</span></span><br/>      | <span data-ttu-id="8229b-131">Identifica l'oggetto che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="8229b-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="8229b-132">Lo script seguente illustra l'uso di un oggetto [**SWbemLastError**](swbemlasterror.md) per ottenere informazioni dettagliate sugli errori.</span><span class="sxs-lookup"><span data-stu-id="8229b-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="8229b-133">Si noti che non tutti i provider forniscono informazioni a **SWbemLastError**.</span><span class="sxs-lookup"><span data-stu-id="8229b-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="8229b-134">Per ulteriori informazioni sui codici di errore nello script, vedere [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8229b-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="8229b-135">Gestione di un errore con C++</span><span class="sxs-lookup"><span data-stu-id="8229b-135">Handling an Error Using C++</span></span>

<span data-ttu-id="8229b-136">Un'applicazione client WMI può ricevere errori specifici di COM o di WMI.</span><span class="sxs-lookup"><span data-stu-id="8229b-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="8229b-137">Gli errori COM sono conformi alla struttura dei codici di errore COM.</span><span class="sxs-lookup"><span data-stu-id="8229b-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="8229b-138">Tutte le interfacce WMI possono restituire un errore specifico di COM, ad eccezione delle interfacce [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)e [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="8229b-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="8229b-139">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8229b-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="8229b-140">Le pagine di riferimento delle interfacce WMI elencano i codici di errore WMI appropriati nella sezione codici di errore.</span><span class="sxs-lookup"><span data-stu-id="8229b-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="8229b-141">Un'applicazione client deve seguire gli standard COM per verificare i codici di stato e di errore restituiti.</span><span class="sxs-lookup"><span data-stu-id="8229b-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="8229b-142">La differenza principale da scegliere è se si desidera recuperare il codice di errore da una chiamata sincrona, semisincrono o asincrona.</span><span class="sxs-lookup"><span data-stu-id="8229b-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="8229b-143">**Per accedere ai messaggi di errore sincroni e semisincrono con C++**</span><span class="sxs-lookup"><span data-stu-id="8229b-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="8229b-144">Recuperare le informazioni sull'errore con una chiamata alla funzione com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="8229b-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="8229b-145">Assicurarsi di chiamare [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediatamente dopo che un metodo di interfaccia indica un errore.</span><span class="sxs-lookup"><span data-stu-id="8229b-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="8229b-146">Sono inclusi i metodi [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) chiamati durante l'elaborazione di un processo semisincrono.</span><span class="sxs-lookup"><span data-stu-id="8229b-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="8229b-147">Esaminare l'oggetto errore COM restituito con una chiamata al metodo [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="8229b-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="8229b-148">Assicurarsi di specificare IID \_ WbemClassObject per il parametro *riid* nella chiamata [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="8229b-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="8229b-149">Il metodo **QueryInterface** restituisce un'istanza di una classe WMI, in genere [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="8229b-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="8229b-150">WMI non recapita l'oggetto errore tramite [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) per una chiamata asincrona perché non esiste alcun modo per stabilire quando o in quale thread è stata eseguita la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="8229b-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="8229b-151">Pertanto, il codice può gestire solo errori specifici o superare l'errore di chiamata tramite COM.</span><span class="sxs-lookup"><span data-stu-id="8229b-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="8229b-152">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="8229b-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="8229b-153">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8229b-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="8229b-154">**Per accedere ai messaggi di errore asincroni mediante C++**</span><span class="sxs-lookup"><span data-stu-id="8229b-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="8229b-155">Recuperare l'oggetto errore COM dall'implementazione di [**IWbemObjectSink:: sestatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="8229b-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="8229b-156">Nello pseudocodice seguente viene illustrata un'implementazione tipica della gestione degli errori per un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="8229b-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

