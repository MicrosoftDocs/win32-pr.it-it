---
description: Effettuando una chiamata asincrona a un metodo WMI o a un metodo del provider è possibile continuare l'esecuzione di uno script mentre gli oggetti restituiscono un oggetto SWbemSink e vengono gestiti da metodi come SWbemSink. OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Esecuzione di una chiamata asincrona con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312695"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="4f373-103">Esecuzione di una chiamata asincrona con VBScript</span><span class="sxs-lookup"><span data-stu-id="4f373-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="4f373-104">Effettuando una chiamata asincrona a un [*metodo WMI*](gloss-w.md) o a un [*metodo del provider*](gloss-p.md) è possibile continuare l'esecuzione di uno script mentre gli oggetti restituiscono un oggetto [**SWbemSink**](swbemsink.md) e vengono gestiti da metodi come [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md).</span><span class="sxs-lookup"><span data-stu-id="4f373-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="4f373-105">Tuttavia, le chiamate asincrone non sono consigliate perché è possibile che i dati non vengano restituiti allo stesso livello di sicurezza della chiamata.</span><span class="sxs-lookup"><span data-stu-id="4f373-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="4f373-106">Quando si usano chiamate di sink asincrone come [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) per ottenere i dati restituiti, è possibile impostare il valore del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="4f373-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="4f373-107">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**</span><span class="sxs-lookup"><span data-stu-id="4f373-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="4f373-108">L'impostazione di questo valore del registro di sistema assicura l'autenticazione degli oggetti dati restituiti al sink.</span><span class="sxs-lookup"><span data-stu-id="4f373-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="4f373-109">Se **UnsecAppAccessControlDefault** è impostato su uno (1), WMI esegue il controllo dell'accesso dei dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="4f373-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="4f373-110">I controlli di accesso verificano che i dati provengano dall'origine corretta.</span><span class="sxs-lookup"><span data-stu-id="4f373-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="4f373-111">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="4f373-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="4f373-112">I metodi asincroni con nomi che terminano con "Async \_ " restituiscono sempre immediatamente dopo essere stati chiamati, in modo che un programma possa continuare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4f373-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="4f373-113">Ad esempio, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) è sincrono e blocca l'esecuzione fino a quando non vengono restituiti tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="4f373-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="4f373-114">Il [**SWbemServices.Exemetodo cQueryAsync**](swbemservices-execqueryasync.md) è la versione asincrona di non blocco.</span><span class="sxs-lookup"><span data-stu-id="4f373-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="4f373-115">Un modo più sicuro per effettuare la chiamata a **SWbemServices.Exe** il non blocco cQuery consiste nell'eseguire la chiamata [*semisincrona*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="4f373-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="4f373-116">Per altre informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md) ed [esecuzione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="4f373-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="4f373-117">Il parametro *iFlags* per le chiamate asincrone viene sempre impostato su zero (0).</span><span class="sxs-lookup"><span data-stu-id="4f373-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="4f373-118">I metodi asincroni non forniscono una raccolta [**SWbemObjectSet**](swbemobjectset.md) alla subroutine del sink.</span><span class="sxs-lookup"><span data-stu-id="4f373-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="4f373-119">Al contrario, la subroutine dell'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) nello script o nell'applicazione riceve ogni oggetto così come viene fornito.</span><span class="sxs-lookup"><span data-stu-id="4f373-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="4f373-120">Al termine della chiamata asincrona originale, viene chiamato l'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto e viene eseguito il codice inserito per elaborare il risultato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="4f373-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="4f373-121">Una pagina di Active Server (ASP) come host di script non supporta una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="4f373-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="4f373-122">Nella procedura riportata di seguito viene descritto come eseguire una chiamata asincrona tramite VBScript.</span><span class="sxs-lookup"><span data-stu-id="4f373-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="4f373-123">**Per eseguire una chiamata asincrona tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="4f373-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="4f373-124">Connettersi a WMI e ottenere un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="4f373-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="4f373-125">Creare il sink di oggetto usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) o (solo per Windows Script Host 2,0) il tag Object con un attributo Events impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="4f373-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="4f373-126">-oppure-</span><span class="sxs-lookup"><span data-stu-id="4f373-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="4f373-127">Crea una subroutine per ogni evento che può essere attivato da un evento asincrono.</span><span class="sxs-lookup"><span data-stu-id="4f373-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="4f373-128">Questi eventi sono definiti come metodi in [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="4f373-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="4f373-129">WMI, ad esempio, effettua un callback a [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) quando ogni istanza restituisce.</span><span class="sxs-lookup"><span data-stu-id="4f373-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="4f373-130">Quando si crea la subroutine, inserire il codice nella subroutine per gestire ogni evento quando viene ricevuto.</span><span class="sxs-lookup"><span data-stu-id="4f373-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="4f373-131">Esaminare il parametro *iHresult* restituito dall'evento [**OnCompleted**](swbemsink-oncompleted.md) per determinare se la chiamata asincrona ha avuto esito positivo o se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="4f373-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="4f373-132">In caso di esito positivo, il valore passato nel parametro *iHresult* è uguale a zero (0).</span><span class="sxs-lookup"><span data-stu-id="4f373-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="4f373-133">Qualsiasi altro valore potrebbe indicare un errore ed è necessario controllare i valori nell'oggetto Error restituito nel parametro *objErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="4f373-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="4f373-134">Eseguire una chiamata asincrona e passare il nome del sink nel parametro *objWbemSink* .</span><span class="sxs-lookup"><span data-stu-id="4f373-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="4f373-135">Eseguire una chiamata che impedisce che lo script venga terminato prima della ricezione di tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="4f373-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="4f373-136">Se lo script può essere eseguito con un'interfaccia schermo, un modo semplice per eseguire questa operazione consiste nell'usare un comando Windows script host (WSH) `Echo` , illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="4f373-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="4f373-137">Quando si esegue questo script, è possibile che la prima istanza venga restituita prima del messaggio **in attesa di istanze** o che venga visualizzata dopo.</span><span class="sxs-lookup"><span data-stu-id="4f373-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="4f373-138">Si tratta della natura dell'elaborazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="4f373-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="4f373-139">Se si chiude troppo presto la finestra di messaggio **in attesa di istanze** , è possibile che non vengano visualizzate tutte le istanze.</span><span class="sxs-lookup"><span data-stu-id="4f373-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="4f373-140">Se si hanno risultati di diverse chiamate asincrone che restituiscono lo stesso sink, archiviare i dati di distinzione necessari nel parametro di contesto *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="4f373-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="4f373-141">Al termine del sink, annullare la chiamata asincrona con il metodo [**Cancel**](swbemsink-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="4f373-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="4f373-142">Il metodo [**Cancel**](swbemsink-cancel.md) indica a WSH di annullare tutte le chiamate asincrone associate a un oggetto sink specificato.</span><span class="sxs-lookup"><span data-stu-id="4f373-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="4f373-143">Pertanto, è consigliabile utilizzare sink distinti per le operazioni asincrone che devono essere indipendenti.</span><span class="sxs-lookup"><span data-stu-id="4f373-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="4f373-144">Rilasciare l'oggetto sink assegnando l'oggetto sink a `Nothing` .</span><span class="sxs-lookup"><span data-stu-id="4f373-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="4f373-145">Nell'esempio di codice seguente viene illustrata una query asincrona per tutte le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="4f373-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="4f373-146">Per una versione semisincrono dello stesso metodo, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4f373-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="4f373-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f373-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f373-148">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="4f373-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="4f373-149">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="4f373-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
