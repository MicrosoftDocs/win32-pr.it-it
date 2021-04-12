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
# <a name="receiving-a-wmi-event"></a>Ricezione di un evento WMI

WMI contiene un'infrastruttura di eventi che genera notifiche sulle modifiche nei dati e nei servizi WMI. [*Le classi di evento*](gloss-e.md) WMI forniscono notifiche quando si verificano eventi specifici.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Query di eventi](#event-queries)
-   [Esempio](#example)
-   [Consumer di eventi](#event-consumers)
-   [Invio di eventi](#providing-events)
-   [Quote di sottoscrizione](#subscription-quotas)
-   [Argomenti correlati](#related-topics)

## <a name="event-queries"></a>Query di eventi

È possibile creare una query [semisincrono](receiving-synchronous-and-semisynchronous-event-notifications.md) o [**asincrona**](receiving-asynchronous-event-notifications.md) per monitorare le modifiche apportate ai registri eventi, alla creazione del processo, allo stato del servizio, alla disponibilità del computer o allo spazio libero dell'unità disco e ad altre entità o eventi. Nello scripting, viene usato il metodo [**cNotificationQuerySWbemServices.Exe**](swbemservices-execnotificationquery.md) per sottoscrivere gli eventi. In C++ viene usato [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) . Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

La notifica di una modifica nel modello di dati WMI standard è denominata [*evento intrinseco*](gloss-i.md). [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) o [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) sono esempi di eventi intrinseci. La notifica di una modifica apportata da un provider per definire un evento del provider viene chiamata [*evento estrinseco*](gloss-e.md). Ad esempio, il provider [del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), il [provider di eventi](/windows/desktop/CIMWin32Prov/power-management-event-provider)di risparmio energia e il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) definiscono gli eventi. Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).

## <a name="example"></a>Esempio

Il seguente esempio di codice di script è una query per il [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) intrinseco della classe di evento [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). È possibile eseguire questo programma in background e, quando si verifica un evento, viene visualizzato un messaggio. Se si chiude la finestra **di dialogo in attesa di eventi** , il programma interrompe l'attesa di eventi. Tenere presente che il **SeSecurityPrivilege** deve essere abilitato.


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





Nell'esempio di codice VBScript seguente viene illustrato il [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) di eventi estrinseci definito dal provider del registro di sistema. Lo script crea un consumer temporaneo usando la chiamata a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)e riceve solo gli eventi quando lo script è in esecuzione. Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato. Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo. Per arrestarla a livello di codice, usare il metodo [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella \_ classe del processo Win32. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).


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



## <a name="event-consumers"></a>consumer di eventi

È possibile monitorare o utilizzare gli eventi utilizzando i seguenti consumer durante l'esecuzione di uno script o un'applicazione:

-   Consumer di eventi temporanei

    Un [*consumer temporaneo*](gloss-t.md) è un'applicazione client WMI che riceve un evento WMI. In WMI è inclusa un'interfaccia univoca che utilizza per specificare gli eventi che WMI deve inviare a un'applicazione client. Un consumer di eventi temporaneo viene considerato temporaneo perché funziona solo quando viene caricato in modo specifico da un utente. Per ulteriori informazioni, vedere [ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md).

-   Consumer di eventi permanenti

    Un [*consumer permanente*](gloss-p.md) è un oggetto com che può ricevere sempre un evento WMI. Un consumer di eventi permanenti utilizza un set di oggetti e filtri permanenti per acquisire un evento WMI. Analogamente a un consumer di eventi temporaneo, è possibile configurare una serie di oggetti e filtri WMI che acquisiscono un evento WMI. Quando si verifica un evento che corrisponde a un filtro, WMI carica il consumer di eventi permanenti e lo notifica sull'evento. Poiché un consumer permanente viene implementato nel repository WMI ed è un file eseguibile registrato in WMI, il consumer di eventi permanenti opera e riceve eventi dopo che è stato creato e anche dopo un riavvio del sistema operativo finché WMI è in esecuzione. Per ulteriori informazioni, vedere [ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md).

Gli script o le applicazioni che ricevono eventi hanno particolari considerazioni sulla sicurezza. Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).

Un'applicazione o uno script può utilizzare un provider di eventi WMI incorporato che fornisce [classi consumer standard](standard-consumer-classes.md). Ogni classe consumer standard risponde a un evento con un'azione diversa inviando un messaggio di posta elettronica o eseguendo uno script. Non è necessario scrivere codice del provider per usare una classe consumer standard per creare un consumer di eventi permanenti. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="providing-events"></a>Invio di eventi

Un provider di eventi è un componente COM che invia un evento a WMI. È possibile creare un provider di eventi per l'invio di un evento in un'applicazione C++ o C#. La maggior parte dei provider di eventi gestisce un oggetto per WMI, ad esempio, un'applicazione o un elemento hardware. Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).

Un evento temporizzato o ripetuto è un evento che si verifica in un momento predeterminato.

WMI fornisce i modi seguenti per creare eventi temporizzati o ripetuti per le applicazioni:

-   Infrastruttura di eventi Microsoft standard.
-   Classe timer specializzata.

Per ulteriori informazioni, vedere [ricezione di un evento temporizzato o ripetuto](receiving-a-timed-or-repeating-event.md). Quando si scrive un provider di eventi, prendere in considerazione le informazioni di sicurezza identificate in [fornire eventi](providing-events-securely.md)in modo sicuro.

È consigliabile compilare sottoscrizioni di eventi permanenti nello \\ \\ spazio dei nomi della sottoscrizione radice. Per altre informazioni, vedere [implementazione delle sottoscrizioni di eventi permanenti tra spazi dei nomi](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Quote di sottoscrizione

Il polling degli eventi può influire negativamente sulle prestazioni per i provider che supportano le query su set di dati di grandi dimensioni. Inoltre, qualsiasi utente con accesso in lettura a uno spazio dei nomi con provider dinamici può eseguire un attacco DoS (Denial of Service). WMI gestisce le quote per tutti gli utenti combinati e per ogni consumer di eventi nella singola istanza di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) che si trova nello \\ spazio dei nomi radice. Queste quote sono globali anziché per ogni spazio dei nomi. Non è possibile modificare le quote.

Attualmente WMI impone le quote usando le proprietà di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). Ogni quota ha un per utente e una versione totale che include tutti gli utenti combinati, non per spazio dei nomi. Nella tabella seguente sono elencate le quote valide per le proprietà **\_ \_ ArbitratorConfiguration** .



| Totale/lettura                                                                   | Quota                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10,000<br/> 1\.000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10,000<br/> 1\.000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10,000<br/> 1\.000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10 milioni (0x989680) byte<br/> 5 milioni (0x4CB40) byte<br/> |



 

Un amministratore o un utente con autorizzazione di **\_ scrittura completa** nello spazio dei nomi può modificare l'istanza singleton di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). WMI tiene traccia della quota per singolo utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

