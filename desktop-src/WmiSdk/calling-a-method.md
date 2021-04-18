---
description: WMI fornisce i metodi nell'API COM e nell'API di scripting per ottenere informazioni o modificare gli oggetti in un sistema aziendale.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Chiamata a un metodo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319308"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="80c41-103">Chiamata a un metodo WMI</span><span class="sxs-lookup"><span data-stu-id="80c41-103">Calling a WMI Method</span></span>

<span data-ttu-id="80c41-104">WMI fornisce i metodi nell' [API com](com-api-for-wmi.md) e nell' [API di scripting](scripting-api-for-wmi.md) per ottenere informazioni o modificare gli oggetti in un sistema aziendale.</span><span class="sxs-lookup"><span data-stu-id="80c41-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="80c41-105">Ad esempio, il metodo di scripting WMI [**SWbemServices.ExecQuery**](swbemservices-execquery.md) query per i dati.</span><span class="sxs-lookup"><span data-stu-id="80c41-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="80c41-106">I provider dispongono anche di metodi definiti nelle classi da essi registrate.</span><span class="sxs-lookup"><span data-stu-id="80c41-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="80c41-107">Gli esempi sono i metodi [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) e [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) forniti dal [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider).</span><span class="sxs-lookup"><span data-stu-id="80c41-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="80c41-108">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="80c41-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="80c41-109">Metodi WMI rispetto ai metodi del provider</span><span class="sxs-lookup"><span data-stu-id="80c41-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="80c41-110">Modalità di chiamata di metodo in WMI</span><span class="sxs-lookup"><span data-stu-id="80c41-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="80c41-111">Modalità sincrona</span><span class="sxs-lookup"><span data-stu-id="80c41-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="80c41-112">Modalità asincrona</span><span class="sxs-lookup"><span data-stu-id="80c41-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="80c41-113">Modalità semisincrono</span><span class="sxs-lookup"><span data-stu-id="80c41-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="80c41-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80c41-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="80c41-115">Metodi WMI rispetto ai metodi del provider</span><span class="sxs-lookup"><span data-stu-id="80c41-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="80c41-116">Utilizzando le chiamate al [*metodo WMI*](gloss-w.md) combinate con le chiamate al [*metodo del provider*](gloss-p.md) , è possibile recuperare e modificare le informazioni sull'azienda.</span><span class="sxs-lookup"><span data-stu-id="80c41-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="80c41-117">Per ulteriori informazioni, vedere [chiamata a un metodo WMI](calling-a-wmi-method.md) e [chiamata a un metodo del provider](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="80c41-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="80c41-118">I metodi dell'oggetto [**SWbemObject**](swbemobject.md) di scripting WMI hanno uno stato speciale perché possono essere applicati a qualsiasi classe di dati WMI.</span><span class="sxs-lookup"><span data-stu-id="80c41-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="80c41-119">Per ulteriori informazioni, vedere Creazione di [script con SWbemObject](scripting-with-swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="80c41-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="80c41-120">Nell'esempio di codice seguente vengono chiamati i metodi WMI e provider.</span><span class="sxs-lookup"><span data-stu-id="80c41-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="80c41-121">I seguenti metodi WMI e provider si trovano nell' [API di scripting per WMI](scripting-api-for-wmi.md):</span><span class="sxs-lookup"><span data-stu-id="80c41-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="80c41-122">**objWMIService.ExecQuery** chiama il metodo di scripting WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="80c41-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="80c41-123">**objService. StopService ()** chiama il metodo del provider [ **Win32 \_ Service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="80c41-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="80c41-124">È possibile cercare il codice che può essere visualizzato in "Return" nella sezione codici restituiti per il [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="80c41-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="80c41-125">Modalità Method-Calling in WMI</span><span class="sxs-lookup"><span data-stu-id="80c41-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="80c41-126">La modalità di chiamata semisincrono in genere fornisce il migliore equilibrio tra sicurezza e prestazioni.</span><span class="sxs-lookup"><span data-stu-id="80c41-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="80c41-127">Per ulteriori informazioni su ognuna delle modalità possibili, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="80c41-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="80c41-128">Sincrono</span><span class="sxs-lookup"><span data-stu-id="80c41-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="80c41-129">Asincrono</span><span class="sxs-lookup"><span data-stu-id="80c41-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="80c41-130">Semisincrono</span><span class="sxs-lookup"><span data-stu-id="80c41-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="80c41-131">Modalità sincrona</span><span class="sxs-lookup"><span data-stu-id="80c41-131">Synchronous Mode</span></span>

<span data-ttu-id="80c41-132">La modalità sincrona si verifica quando il programma o gli script vengono sospesi fino a quando la chiamata al metodo non restituisce un oggetto raccolta [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="80c41-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="80c41-133">WMI compila questa raccolta in memoria prima di restituire l'oggetto raccolta al programma o allo script chiamante.</span><span class="sxs-lookup"><span data-stu-id="80c41-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="80c41-134">La modalità sincrona può avere un effetto negativo sulle prestazioni di programmi o script nel computer in cui è in esecuzione il programma o lo script.</span><span class="sxs-lookup"><span data-stu-id="80c41-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="80c41-135">Ad esempio, il recupero sincrono di migliaia di eventi dal registro eventi può richiedere molto tempo e usare una grande quantità di memoria perché WMI crea un oggetto da ogni evento e quindi inserisce tali oggetti in una raccolta prima di passare la raccolta al metodo.</span><span class="sxs-lookup"><span data-stu-id="80c41-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="80c41-136">È consigliabile chiamare solo i metodi che non restituiscono set di dati di grandi dimensioni in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="80c41-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="80c41-137">I metodi [**SWbemServices**](swbemservices.md) seguenti possono essere chiamati in modo sicuro in modalità sincrona:</span><span class="sxs-lookup"><span data-stu-id="80c41-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="80c41-138">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="80c41-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="80c41-139">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="80c41-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="80c41-140">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="80c41-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="80c41-141">Tutti i metodi [**SWbemServices**](swbemservices.md) senza la parola "Async" nel nome possono essere chiamati in modalità sincrona impostando il valore **WbemFlagReturnWhenComplete** nel parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="80c41-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="80c41-142">Modalità asincrona</span><span class="sxs-lookup"><span data-stu-id="80c41-142">Asynchronous Mode</span></span>

<span data-ttu-id="80c41-143">La modalità asincrona si verifica quando il programma o lo script continua l'esecuzione dopo la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="80c41-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="80c41-144">WMI restituisce tutti gli oggetti dal metodo a un oggetto [**SWbemSink**](swbemsink.md) quando viene creato un oggetto.</span><span class="sxs-lookup"><span data-stu-id="80c41-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="80c41-145">Per elaborare gli oggetti restituiti, il programma o lo script chiamante deve avere un oggetto **SWbemSink** e un gestore dell'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="80c41-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="80c41-146">Per ulteriori informazioni sulla creazione di un gestore eventi per la modalità asincrona, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="80c41-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="80c41-147">Sebbene questa modalità non abbia le prestazioni e la penalizzazione delle risorse della modalità sincrona, la modalità asincrona può creare gravi rischi per la sicurezza perché i risultati archiviati nell'oggetto [**SWbemSink**](swbemsink.md) potrebbero non provenire dal programma chiamante o dallo script.</span><span class="sxs-lookup"><span data-stu-id="80c41-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="80c41-148">WMI abbassa il livello di autenticazione per l'oggetto **SWbemSink** fino a quando il metodo non riesce.</span><span class="sxs-lookup"><span data-stu-id="80c41-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="80c41-149">Per ulteriori informazioni su come attenuare questi rischi per la sicurezza, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="80c41-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="80c41-150">I metodi aggiunti con la parola Async sono metodi per la modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="80c41-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="80c41-151">I metodi seguenti sono chiamate asincrone:</span><span class="sxs-lookup"><span data-stu-id="80c41-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="80c41-152">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="80c41-153">**SWbemServices. DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="80c41-154">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="80c41-155">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="80c41-156">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="80c41-157">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="80c41-158">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="80c41-159">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="80c41-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="80c41-160">Per ulteriori informazioni sulla modalità asincrona, vedere:</span><span class="sxs-lookup"><span data-stu-id="80c41-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="80c41-161">Esecuzione di una chiamata asincrona con C++</span><span class="sxs-lookup"><span data-stu-id="80c41-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="80c41-162">Esecuzione di una chiamata asincrona con VBScript</span><span class="sxs-lookup"><span data-stu-id="80c41-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="80c41-163">Modalità semisincrono</span><span class="sxs-lookup"><span data-stu-id="80c41-163">Semisynchronous Mode</span></span>

<span data-ttu-id="80c41-164">La modalità semisincrono è simile alla modalità asincrona in quanto il programma o lo script continua l'esecuzione dopo la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="80c41-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="80c41-165">In modalità semisincrono, WMI recupera gli oggetti in background quando lo script o il programma continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="80c41-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="80c41-166">WMI restituisce ogni oggetto restituito al metodo chiamante subito dopo la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="80c41-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="80c41-167">Poiché WMI gestisce l'oggetto, la modalità semisincrono è più sicura della modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="80c41-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="80c41-168">Tuttavia, se si usa la modalità semisincrono con più di 1.000 istanze, il recupero delle istanze può monopolizzare le risorse disponibili, che possono influire negativamente sulle prestazioni del programma o dello script e del computer con il programma o lo script.</span><span class="sxs-lookup"><span data-stu-id="80c41-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="80c41-169">Ogni oggetto prende le risorse necessarie fino a quando non viene rilasciata la memoria.</span><span class="sxs-lookup"><span data-stu-id="80c41-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="80c41-170">Per ovviare a questa condizione, è possibile chiamare il metodo con il set di parametri *iFlags* con i flag **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** per indicare a WMI di restituire un [**SWbemObjectSet**](swbemobjectset.md)di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="80c41-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="80c41-171">Un **SWbemObjectSet** di sola trasmissione elimina il problema di prestazioni causato da un set di dati di grandi dimensioni rilasciando la memoria dopo l'enumerazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="80c41-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="80c41-172">Qualsiasi metodo [**SWbemServices**](swbemservices.md) che non può essere chiamato in modalità sincrona o asincrona viene chiamato in modalità semisincrono.</span><span class="sxs-lookup"><span data-stu-id="80c41-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="80c41-173">I metodi seguenti vengono chiamati in modalità semisincrono:</span><span class="sxs-lookup"><span data-stu-id="80c41-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="80c41-174">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="80c41-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="80c41-175">**SWbemServices. Delete**</span><span class="sxs-lookup"><span data-stu-id="80c41-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="80c41-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="80c41-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="80c41-177">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="80c41-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="80c41-178">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="80c41-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="80c41-179">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="80c41-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="80c41-180">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="80c41-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="80c41-181">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="80c41-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="80c41-182">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="80c41-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="80c41-183">**SWbemServices. Put**</span><span class="sxs-lookup"><span data-stu-id="80c41-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="80c41-184">Per ulteriori informazioni sulla modalità semisincrono, vedere [creazione di una chiamata semisincrono con C++](making-a-semisynchronous-call-with-c--.md) ed [esecuzione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="80c41-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80c41-185">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80c41-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c41-186">Miglioramento delle prestazioni di enumerazione</span><span class="sxs-lookup"><span data-stu-id="80c41-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="80c41-187">Creazione di script con SWbemObject</span><span class="sxs-lookup"><span data-stu-id="80c41-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="80c41-188">**WbemFlagEnum**</span><span class="sxs-lookup"><span data-stu-id="80c41-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
