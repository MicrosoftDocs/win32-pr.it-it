---
description: Gli amministratori di sistema possono utilizzare WMI per monitorare gli eventi in una rete.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Monitoraggio degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130394"
---
# <a name="monitoring-events"></a><span data-ttu-id="01807-103">Monitoraggio degli eventi</span><span class="sxs-lookup"><span data-stu-id="01807-103">Monitoring Events</span></span>

<span data-ttu-id="01807-104">Gli amministratori di sistema possono utilizzare WMI per monitorare gli eventi in una rete.</span><span class="sxs-lookup"><span data-stu-id="01807-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="01807-105">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="01807-105">For example:</span></span>

-   <span data-ttu-id="01807-106">Un servizio viene arrestato in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="01807-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="01807-107">Un server diventa non disponibile.</span><span class="sxs-lookup"><span data-stu-id="01807-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="01807-108">Un'unità disco si riempie della capacità del 80%.</span><span class="sxs-lookup"><span data-stu-id="01807-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="01807-109">Gli eventi di sicurezza vengono segnalati a un registro eventi NT.</span><span class="sxs-lookup"><span data-stu-id="01807-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="01807-110">WMI supporta il rilevamento e il recapito di eventi ai consumer di eventi perché alcuni provider WMI sono provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="01807-111">Per ulteriori informazioni, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="01807-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="01807-112">[*I consumer di eventi*](gloss-e.md) sono applicazioni o script che richiedono la notifica di eventi, quindi eseguono attività quando si verificano eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="01807-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="01807-113">È possibile creare script o applicazioni di monitoraggio degli eventi che monitorano temporaneamente quando si verificano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="01807-114">WMI fornisce inoltre un set di provider di eventi permanenti preinstallati e le classi consumer permanenti che consentono di monitorare in modo permanente gli eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="01807-115">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="01807-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="01807-116">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="01807-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="01807-117">Utilizzo di consumer di eventi temporanei</span><span class="sxs-lookup"><span data-stu-id="01807-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="01807-118">Utilizzo di consumer di eventi permanenti</span><span class="sxs-lookup"><span data-stu-id="01807-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="01807-119">Utilizzo di consumer di eventi temporanei</span><span class="sxs-lookup"><span data-stu-id="01807-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="01807-120">I consumer di eventi temporanei sono script o applicazioni che restituiscono gli eventi che corrispondono a una query o a un filtro di eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="01807-121">Le query di eventi temporanei usano in genere [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) nelle applicazioni C++ o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) negli script e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="01807-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="01807-122">Una query di eventi richiede le istanze di una classe di evento che specifica un determinato tipo di evento, ad esempio [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) o [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="01807-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="01807-123">Nell'esempio di codice VBScript seguente viene richiesta una notifica quando viene creata un'istanza di [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="01807-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="01807-124">Un'istanza di questa classe viene generata quando un processo viene avviato o arrestato.</span><span class="sxs-lookup"><span data-stu-id="01807-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="01807-125">Per eseguire lo script, copiarlo in un file denominato event.vbs e utilizzare la riga di comando seguente: **cscript event.vbs**.</span><span class="sxs-lookup"><span data-stu-id="01807-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="01807-126">È possibile visualizzare l'output dello script avviando Notepad.exe o qualsiasi altro processo.</span><span class="sxs-lookup"><span data-stu-id="01807-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="01807-127">Lo script si interrompe dopo cinque processi avviati o arrestati.</span><span class="sxs-lookup"><span data-stu-id="01807-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="01807-128">Questo script chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), che è la versione [*semisincrono*](gloss-s.md) del metodo.</span><span class="sxs-lookup"><span data-stu-id="01807-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="01807-129">Vedere lo script successivo per un esempio di configurazione di una sottoscrizione di eventi temporanei asincrona chiamando [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="01807-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="01807-130">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="01807-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="01807-131">Lo script chiama [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) per ottenere ed elaborare ogni evento al suo arrivo.</span><span class="sxs-lookup"><span data-stu-id="01807-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="01807-132">Salvare lo script in un file con estensione vbs ed eseguire lo script in una riga di comando usando CScript: **cscript file.vbs**.</span><span class="sxs-lookup"><span data-stu-id="01807-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



I consumer di eventi temporanei devono essere avviati manualmente e non devono essere mantenuti tra i riavvii WMI o i riavvii del sistema operativo. <span data-ttu-id="01807-134">Un consumer di eventi temporaneo può elaborare gli eventi solo mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="01807-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="01807-135">Nella procedura riportata di seguito viene descritto come creare un consumer di eventi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="01807-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="01807-136">**Per creare un consumer di eventi temporaneo**</span><span class="sxs-lookup"><span data-stu-id="01807-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="01807-137">Decidere quale linguaggio di programmazione usare.</span><span class="sxs-lookup"><span data-stu-id="01807-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="01807-138">Il linguaggio di programmazione determina l'API da usare.</span><span class="sxs-lookup"><span data-stu-id="01807-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="01807-139">Per il linguaggio di programmazione C++, usare l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="01807-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="01807-140">Per Visual Basic o linguaggi di scripting, usare l' [API di scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="01807-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="01807-141">Avviare la codifica di un'applicazione consumer di eventi temporanei nello stesso modo in cui si avvia un'applicazione WMI.</span><span class="sxs-lookup"><span data-stu-id="01807-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="01807-142">I primi passaggi della codifica dipendono dal linguaggio di programmazione.</span><span class="sxs-lookup"><span data-stu-id="01807-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="01807-143">In genere, si accede a WMI e si configurano le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="01807-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="01807-144">Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="01807-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="01807-145">Definire la query di eventi che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="01807-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="01807-146">Per ottenere alcuni tipi di dati sulle prestazioni, potrebbe essere necessario utilizzare le classi fornite dai provider a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="01807-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="01807-147">Per altre informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md), [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md)ed [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="01807-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="01807-148">Decidere di effettuare una chiamata asincrona o una chiamata semisincrono e scegliere il metodo API.</span><span class="sxs-lookup"><span data-stu-id="01807-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="01807-149">Le chiamate asincrone consentono di evitare l'overhead del polling dei dati.</span><span class="sxs-lookup"><span data-stu-id="01807-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="01807-150">Tuttavia, le chiamate semisincrono offrono prestazioni simili con una maggiore sicurezza.</span><span class="sxs-lookup"><span data-stu-id="01807-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="01807-151">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="01807-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="01807-152">Eseguire la chiamata al metodo asincrono o semisincrono e includere una query di eventi come parametro *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="01807-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="01807-153">Per le applicazioni C++, chiamare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="01807-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="01807-154">**IWbemServices:: ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="01807-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="01807-155">**IWbemServices:: ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="01807-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="01807-156">Per gli script, chiamare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="01807-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="01807-157">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="01807-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="01807-158">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="01807-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="01807-159">Scrivere il codice per elaborare l'oggetto evento restituito.</span><span class="sxs-lookup"><span data-stu-id="01807-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="01807-160">Per le query di eventi asincroni, inserire il codice nei vari metodi o eventi del sink di oggetto.</span><span class="sxs-lookup"><span data-stu-id="01807-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="01807-161">Per le query di eventi semisincrono, ogni oggetto viene restituito come WMI lo ottiene, quindi il codice deve essere nel ciclo che gestisce ciascun oggetto.</span><span class="sxs-lookup"><span data-stu-id="01807-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="01807-162">Il seguente esempio di codice di script è una versione asincrona dello script [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="01807-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="01807-163">Poiché le operazioni asincrone vengono restituite immediatamente, una finestra di dialogo mantiene attivo lo script mentre è in attesa di eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="01807-164">Anziché chiamare [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) per ricevere ogni evento, lo script dispone di un gestore eventi per l'evento [**OnObjectReady di SWbemSink**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="01807-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> <span data-ttu-id="01807-165">Un callback asincrono, ad esempio un callback gestito dalla `SINK_OnObjectReady` subroutine, consente a un utente non autenticato di fornire dati al sink.</span><span class="sxs-lookup"><span data-stu-id="01807-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="01807-166">Per una maggiore sicurezza, usare la comunicazione semisincrono o la comunicazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="01807-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="01807-167">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="01807-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="01807-168">Esecuzione di una chiamata semisincrono con C++</span><span class="sxs-lookup"><span data-stu-id="01807-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="01807-169">Esecuzione di una chiamata semisincrono con VBScript</span><span class="sxs-lookup"><span data-stu-id="01807-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="01807-170">Esecuzione di una chiamata asincrona con C++</span><span class="sxs-lookup"><span data-stu-id="01807-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="01807-171">Esecuzione di una chiamata asincrona con VBScript</span><span class="sxs-lookup"><span data-stu-id="01807-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="01807-172">Impostazione della sicurezza per una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="01807-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="01807-173">Protezione dei client di scripting</span><span class="sxs-lookup"><span data-stu-id="01807-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="01807-174">Utilizzo di consumer di eventi permanenti</span><span class="sxs-lookup"><span data-stu-id="01807-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="01807-175">Un consumer di eventi permanente viene eseguito finché la registrazione non viene annullata in modo esplicito e quindi viene avviata al riavvio di WMI o del sistema.</span><span class="sxs-lookup"><span data-stu-id="01807-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="01807-176">Un consumer di eventi permanenti è una combinazione di classi WMI, filtri e oggetti COM in un sistema.</span><span class="sxs-lookup"><span data-stu-id="01807-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="01807-177">Nell'elenco seguente vengono identificate le parti necessarie per creare un consumer di eventi permanente:</span><span class="sxs-lookup"><span data-stu-id="01807-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="01807-178">Oggetto COM contenente il codice che implementa l'utente permanente.</span><span class="sxs-lookup"><span data-stu-id="01807-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="01807-179">Nuova classe consumer permanente.</span><span class="sxs-lookup"><span data-stu-id="01807-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="01807-180">Istanza della classe consumer permanente.</span><span class="sxs-lookup"><span data-stu-id="01807-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="01807-181">Filtro che contiene la query per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="01807-182">Collegamento tra l'utente e il filtro.</span><span class="sxs-lookup"><span data-stu-id="01807-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="01807-183">Per ulteriori informazioni, vedere [ricezione di eventi in qualsiasi momento](--filtertoconsumerbinding.md).</span><span class="sxs-lookup"><span data-stu-id="01807-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="01807-184">WMI fornisce diversi consumer permanenti.</span><span class="sxs-lookup"><span data-stu-id="01807-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="01807-185">Le classi consumer e l'oggetto COM che contiene il codice sono preinstallati.</span><span class="sxs-lookup"><span data-stu-id="01807-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="01807-186">Ad esempio, è possibile creare e configurare un'istanza della classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per eseguire uno script quando si verifica un evento.</span><span class="sxs-lookup"><span data-stu-id="01807-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="01807-187">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="01807-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="01807-188">Per un esempio dell'uso di **ActiveScriptEventConsumer**, vedere [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="01807-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="01807-189">Nella procedura seguente viene descritto come creare un consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="01807-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="01807-190">**Per creare un consumer di eventi permanenti**</span><span class="sxs-lookup"><span data-stu-id="01807-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="01807-191">[Registrare il provider di eventi](registering-a-provider.md) con lo spazio dei nomi in uso.</span><span class="sxs-lookup"><span data-stu-id="01807-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="01807-192">Alcuni provider di eventi possono utilizzare solo uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="01807-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="01807-193">Ad esempio, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) è un evento intrinseco supportato dal [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) e viene registrato per impostazione predefinita con lo \\ \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="01807-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="01807-194">Per creare una sottoscrizione tra più spazi dei nomi, è possibile utilizzare la proprietà **EventNamespace** di [**\_ \_ EventFilter**](--eventfilter.md) utilizzata nella registrazione.</span><span class="sxs-lookup"><span data-stu-id="01807-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="01807-195">Per altre informazioni, vedere [implementazione delle sottoscrizioni di eventi permanenti tra spazi dei nomi](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="01807-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="01807-196">[Registrare il provider di consumer di eventi](registering-an-event-consumer-provider.md) con lo spazio dei nomi in cui si trovano le classi di evento.</span><span class="sxs-lookup"><span data-stu-id="01807-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="01807-197">WMI utilizza un provider di consumer di eventi per trovare un consumer di eventi permanente.</span><span class="sxs-lookup"><span data-stu-id="01807-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="01807-198">Il consumer di eventi permanenti è l'applicazione che WMI inizia quando viene ricevuto un evento.</span><span class="sxs-lookup"><span data-stu-id="01807-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="01807-199">Per registrare un consumer di eventi, i provider creano istanze di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="01807-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="01807-200">Creare un'istanza della classe che rappresenti il consumer di eventi permanenti che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="01807-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="01807-201">Le classi consumer di eventi sono derivate dalla classe [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="01807-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="01807-202">Impostare le proprietà richieste dall'istanza del consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="01807-203">Registrare il consumer con COM utilizzando l'utilità **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="01807-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="01807-204">Creare un'istanza della classe filtro eventi [**\_ \_ EventFilter**](--eventfilter.md).</span><span class="sxs-lookup"><span data-stu-id="01807-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="01807-205">Impostare i campi obbligatori per l'istanza del filtro eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="01807-206">I campi obbligatori per [**\_ \_ EventFilter**](--eventfilter.md) sono **Name**, **QueryLanguage** e **query**.</span><span class="sxs-lookup"><span data-stu-id="01807-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="01807-207">La proprietà **Name** può essere un nome univoco per un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="01807-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="01807-208">La proprietà **QueryLanguage** è sempre impostata su "WQL".</span><span class="sxs-lookup"><span data-stu-id="01807-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="01807-209">La proprietà **query** è una stringa che contiene una query di eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="01807-210">Un evento viene generato quando la query di un consumer di eventi permanenti ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="01807-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="01807-211">L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.</span><span class="sxs-lookup"><span data-stu-id="01807-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="01807-212">Creare un'istanza della classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare un consumer di eventi logici a un filtro eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="01807-213">WMI utilizza un'associazione per trovare il consumer di eventi associato all'evento che corrisponde ai criteri specificati nel filtro eventi.</span><span class="sxs-lookup"><span data-stu-id="01807-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="01807-214">WMI utilizza il provider di consumer di eventi per individuare l'applicazione del consumer di eventi permanente da avviare.</span><span class="sxs-lookup"><span data-stu-id="01807-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
