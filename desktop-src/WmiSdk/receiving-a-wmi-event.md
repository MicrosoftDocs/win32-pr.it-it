---
description: WMI contiene un'infrastruttura di eventi che genera notifiche sulle modifiche nei dati e nei servizi WMI. Le classi di evento WMI forniscono notifiche quando si verificano eventi specifici.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Ricezione di un evento WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131015"
---
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="b6ce2-104">Ricezione di un evento WMI</span><span class="sxs-lookup"><span data-stu-id="b6ce2-104">Receiving a WMI Event</span></span>

<span data-ttu-id="b6ce2-105">WMI contiene un'infrastruttura di eventi che genera notifiche sulle modifiche nei dati e nei servizi WMI.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="b6ce2-106">[*Le classi di evento*](gloss-e.md) WMI forniscono notifiche quando si verificano eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="b6ce2-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="b6ce2-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="b6ce2-108">Query di eventi</span><span class="sxs-lookup"><span data-stu-id="b6ce2-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="b6ce2-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6ce2-109">Example</span></span>](#example)
-   [<span data-ttu-id="b6ce2-110">Consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="b6ce2-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="b6ce2-111">Invio di eventi</span><span class="sxs-lookup"><span data-stu-id="b6ce2-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="b6ce2-112">Quote di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="b6ce2-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="b6ce2-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6ce2-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="b6ce2-114">Query di eventi</span><span class="sxs-lookup"><span data-stu-id="b6ce2-114">Event Queries</span></span>

<span data-ttu-id="b6ce2-115">È possibile creare una query [semisincrono](receiving-synchronous-and-semisynchronous-event-notifications.md) o [**asincrona**](receiving-asynchronous-event-notifications.md) per monitorare le modifiche apportate ai registri eventi, alla creazione del processo, allo stato del servizio, alla disponibilità del computer o allo spazio libero dell'unità disco e ad altre entità o eventi.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="b6ce2-116">Nello scripting, viene usato il metodo [**cNotificationQuerySWbemServices.Exe**](swbemservices-execnotificationquery.md) per sottoscrivere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="b6ce2-117">In C++ viene usato [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="b6ce2-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="b6ce2-118">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b6ce2-119">La notifica di una modifica nel modello di dati WMI standard è denominata [*evento intrinseco*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="b6ce2-120">[**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) o [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) sono esempi di eventi intrinseci.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="b6ce2-121">La notifica di una modifica apportata da un provider per definire un evento del provider viene chiamata [*evento estrinseco*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="b6ce2-122">Ad esempio, il provider [del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), il [provider di eventi](/windows/desktop/CIMWin32Prov/power-management-event-provider)di risparmio energia e il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) definiscono gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="b6ce2-123">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="b6ce2-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6ce2-124">Example</span></span>

<span data-ttu-id="b6ce2-125">Il seguente esempio di codice di script è una query per il [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrinseco della classe di evento [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="b6ce2-126">È possibile eseguire questo programma in background e, quando si verifica un evento, viene visualizzato un messaggio.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="b6ce2-127">Se si chiude la finestra **di dialogo in attesa di eventi** , il programma interrompe l'attesa di eventi.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="b6ce2-128">Tenere presente che il **SeSecurityPrivilege** deve essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





<span data-ttu-id="b6ce2-129">Nell'esempio di codice VBScript seguente viene illustrato il [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) di eventi estrinseci definito dal provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="b6ce2-130">Lo script crea un consumer temporaneo usando la chiamata a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)e riceve solo gli eventi quando lo script è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="b6ce2-131">Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="b6ce2-132">Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="b6ce2-133">Per arrestarla a livello di codice, usare il metodo [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella \_ classe del processo Win32.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="b6ce2-134">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a><span data-ttu-id="b6ce2-135">consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="b6ce2-135">Event Consumers</span></span>

<span data-ttu-id="b6ce2-136">È possibile monitorare o utilizzare gli eventi utilizzando i seguenti consumer durante l'esecuzione di uno script o un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="b6ce2-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="b6ce2-137">Consumer di eventi temporanei</span><span class="sxs-lookup"><span data-stu-id="b6ce2-137">Temporary event consumers</span></span>

    <span data-ttu-id="b6ce2-138">Un [*consumer temporaneo*](gloss-t.md) è un'applicazione client WMI che riceve un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="b6ce2-139">In WMI è inclusa un'interfaccia univoca che utilizza per specificare gli eventi che WMI deve inviare a un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="b6ce2-140">Un consumer di eventi temporaneo viene considerato temporaneo perché funziona solo quando viene caricato in modo specifico da un utente.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="b6ce2-141">Per ulteriori informazioni, vedere [ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="b6ce2-142">Consumer di eventi permanenti</span><span class="sxs-lookup"><span data-stu-id="b6ce2-142">Permanent event consumers</span></span>

    <span data-ttu-id="b6ce2-143">Un [*consumer permanente*](gloss-p.md) è un oggetto com che può ricevere sempre un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="b6ce2-144">Un consumer di eventi permanenti utilizza un set di oggetti e filtri permanenti per acquisire un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="b6ce2-145">Analogamente a un consumer di eventi temporaneo, è possibile configurare una serie di oggetti e filtri WMI che acquisiscono un evento WMI.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="b6ce2-146">Quando si verifica un evento che corrisponde a un filtro, WMI carica il consumer di eventi permanenti e lo notifica sull'evento.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="b6ce2-147">Poiché un consumer permanente viene implementato nel repository WMI ed è un file eseguibile registrato in WMI, il consumer di eventi permanenti opera e riceve eventi dopo che è stato creato e anche dopo un riavvio del sistema operativo finché WMI è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="b6ce2-148">Per ulteriori informazioni, vedere [ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="b6ce2-149">Gli script o le applicazioni che ricevono eventi hanno particolari considerazioni sulla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="b6ce2-150">Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="b6ce2-151">Un'applicazione o uno script può utilizzare un provider di eventi WMI incorporato che fornisce [classi consumer standard](standard-consumer-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="b6ce2-152">Ogni classe consumer standard risponde a un evento con un'azione diversa inviando un messaggio di posta elettronica o eseguendo uno script.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="b6ce2-153">Non è necessario scrivere codice del provider per usare una classe consumer standard per creare un consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="b6ce2-154">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="b6ce2-155">Invio di eventi</span><span class="sxs-lookup"><span data-stu-id="b6ce2-155">Providing Events</span></span>

<span data-ttu-id="b6ce2-156">Un provider di eventi è un componente COM che invia un evento a WMI.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="b6ce2-157">È possibile creare un provider di eventi per l'invio di un evento in un'applicazione C++ o C#.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="b6ce2-158">La maggior parte dei provider di eventi gestisce un oggetto per WMI, ad esempio, un'applicazione o un elemento hardware.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="b6ce2-159">Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="b6ce2-160">Un evento temporizzato o ripetuto è un evento che si verifica in un momento predeterminato.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="b6ce2-161">WMI fornisce i modi seguenti per creare eventi temporizzati o ripetuti per le applicazioni:</span><span class="sxs-lookup"><span data-stu-id="b6ce2-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="b6ce2-162">Infrastruttura di eventi Microsoft standard.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="b6ce2-163">Classe timer specializzata.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-163">A specialized timer class.</span></span>

<span data-ttu-id="b6ce2-164">Per ulteriori informazioni, vedere [ricezione di un evento temporizzato o ripetuto](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="b6ce2-165">Quando si scrive un provider di eventi, prendere in considerazione le informazioni di sicurezza identificate in [fornire eventi](providing-events-securely.md)in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="b6ce2-166">È consigliabile compilare sottoscrizioni di eventi permanenti nello \\ \\ spazio dei nomi della sottoscrizione radice.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="b6ce2-167">Per altre informazioni, vedere [implementazione delle sottoscrizioni di eventi permanenti tra spazi dei nomi](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="b6ce2-168">Quote di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="b6ce2-168">Subscription Quotas</span></span>

<span data-ttu-id="b6ce2-169">Il polling degli eventi può influire negativamente sulle prestazioni per i provider che supportano le query su set di dati di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="b6ce2-170">Inoltre, qualsiasi utente con accesso in lettura a uno spazio dei nomi con provider dinamici può eseguire un attacco DoS (Denial of Service).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="b6ce2-171">WMI gestisce le quote per tutti gli utenti combinati e per ogni consumer di eventi nella singola istanza di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) che si trova nello \\ spazio dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="b6ce2-172">Queste quote sono globali anziché per ogni spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="b6ce2-173">Non è possibile modificare le quote.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-173">You cannot change the quotas.</span></span>

<span data-ttu-id="b6ce2-174">Attualmente WMI impone le quote usando le proprietà di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="b6ce2-175">Ogni quota ha un per utente e una versione totale che include tutti gli utenti combinati, non per spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="b6ce2-176">Nella tabella seguente sono elencate le quote valide per le proprietà **\_ \_ ArbitratorConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b6ce2-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="b6ce2-177">Totale/lettura</span><span class="sxs-lookup"><span data-stu-id="b6ce2-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="b6ce2-178">Quota</span><span class="sxs-lookup"><span data-stu-id="b6ce2-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b6ce2-179">TemporarySubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="b6ce2-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="b6ce2-180">TemporarySubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="b6ce2-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="b6ce2-181">10,000</span><span class="sxs-lookup"><span data-stu-id="b6ce2-181">10,000</span></span><br/> <span data-ttu-id="b6ce2-182">1\.000</span><span class="sxs-lookup"><span data-stu-id="b6ce2-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="b6ce2-183">PermanentSubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="b6ce2-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="b6ce2-184">PermanentSubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="b6ce2-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="b6ce2-185">10,000</span><span class="sxs-lookup"><span data-stu-id="b6ce2-185">10,000</span></span><br/> <span data-ttu-id="b6ce2-186">1\.000</span><span class="sxs-lookup"><span data-stu-id="b6ce2-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="b6ce2-187">PollingInstructionsTotal</span><span class="sxs-lookup"><span data-stu-id="b6ce2-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="b6ce2-188">PollingInstructionsPerUser</span><span class="sxs-lookup"><span data-stu-id="b6ce2-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="b6ce2-189">10,000</span><span class="sxs-lookup"><span data-stu-id="b6ce2-189">10,000</span></span><br/> <span data-ttu-id="b6ce2-190">1\.000</span><span class="sxs-lookup"><span data-stu-id="b6ce2-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="b6ce2-191">PollingMemoryTotal</span><span class="sxs-lookup"><span data-stu-id="b6ce2-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="b6ce2-192">PollingMemoryPerUser</span><span class="sxs-lookup"><span data-stu-id="b6ce2-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="b6ce2-193">10 milioni (0x989680) byte</span><span class="sxs-lookup"><span data-stu-id="b6ce2-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="b6ce2-194">5 milioni (0x4CB40) byte</span><span class="sxs-lookup"><span data-stu-id="b6ce2-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="b6ce2-195">Un amministratore o un utente con autorizzazione di **\_ scrittura completa** nello spazio dei nomi può modificare l'istanza singleton di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b6ce2-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="b6ce2-196">WMI tiene traccia della quota per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="b6ce2-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6ce2-197">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6ce2-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6ce2-198">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="b6ce2-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

