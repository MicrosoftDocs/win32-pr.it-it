---
description: WMI contiene un'infrastruttura di eventi che genera notifiche sulle modifiche nei dati e nei servizi WMI. Le classi di eventi WMI forniscono una notifica quando si verificano eventi specifici.
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
ms.openlocfilehash: 5dac8aba93cc841211cbdc02bc5e75773ab444eaa2763c4b0367fbd36ada37b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992591"
---
# <a name="receiving-a-wmi-event"></a>Ricezione di un evento WMI

WMI contiene un'infrastruttura di eventi che genera notifiche sulle modifiche nei dati e nei servizi WMI. Le [*classi di eventi*](gloss-e.md) WMI forniscono una notifica quando si verificano eventi specifici.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Query di eventi](#event-queries)
-   [Esempio](#example)
-   [Consumer di eventi](#event-consumers)
-   [Fornire eventi](#providing-events)
-   [Quote di sottoscrizione](#subscription-quotas)
-   [Argomenti correlati](#related-topics)

## <a name="event-queries"></a>Query di eventi

È possibile creare una [**query**](receiving-asynchronous-event-notifications.md) [semisincrona](receiving-synchronous-and-semisynchronous-event-notifications.md) o asincrona per monitorare le modifiche ai log eventi, alla creazione del processo, allo stato del servizio, alla disponibilità del computer o allo spazio disponibile su disco e ad altre entità o eventi. Nello scripting, il [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) viene usato per sottoscrivere gli eventi. In C++ viene [**usato IWbemServices::ExecNotificationQuery.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

La notifica di una modifica nel modello di dati WMI standard è denominata [*evento intrinseco*](gloss-i.md). [**\_ \_ InstanceCreationEvent o**](--instancecreationevent.md) [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md) sono esempi di eventi intrinseci. La notifica di una modifica apportata da un provider per definire un evento del provider è detta evento [*estensiva*](gloss-e.md). Ad esempio, il [provider del Registro di](/previous-versions/windows/desktop/regprov/system-registry-provider)sistema, il provider di eventi di [gestione](/windows/desktop/CIMWin32Prov/power-management-event-provider)alimentazione e il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) definiscono i propri eventi. Per altre informazioni, vedere [Determinare il tipo di evento da ricevere.](determining-the-type-of-event-to-receive.md)

## <a name="example"></a>Esempio

L'esempio di codice di script seguente è una query per [**\_ \_ l'oggetto InstanceCreationEvent intrinseco**](--instancecreationevent.md) della classe di evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). È possibile eseguire questo programma in background e quando è presente un evento, viene visualizzato un messaggio. Se si chiude la **finestra di dialogo** In attesa di eventi, il programma smette di attendere gli eventi. Tenere presente che **SeSecurityPrivilege** deve essere abilitato.


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





Nell'esempio di codice VBScript seguente viene illustrato l'evento estrinsico [ \_ \_ RegistryValueChangeEvent](registering-for-system-registry-events.md) definito dal provider del Registro di sistema. Lo script crea un consumer temporaneo usando la chiamata [**aSWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)e riceve eventi solo quando lo script è in esecuzione. Lo script seguente viene eseguito a tempo indeterminato fino al riavvio del computer, all'arresto di WMI o all'arresto dello script. Per arrestare manualmente lo script, usare Gestione attività per arrestare il processo. Per arrestarlo a livello di codice, usare [**il metodo Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella classe Win32 \_ Process. Per altre informazioni, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)


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

È possibile monitorare o utilizzare gli eventi usando i consumer seguenti durante l'esecuzione di uno script o di un'applicazione:

-   Consumer di eventi temporanei

    Un [*consumer temporaneo*](gloss-t.md) è un'applicazione client WMI che riceve un evento WMI. WMI include un'interfaccia univoca che consente di specificare gli eventi che WMI deve inviare a un'applicazione client. Un consumer di eventi temporaneo viene considerato temporaneo perché funziona solo quando viene caricato in modo specifico da un utente. Per altre informazioni, vedere [Ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md).

-   Consumer di eventi permanenti

    Un [*consumer permanente*](gloss-p.md) è un oggetto COM che può ricevere un evento WMI in qualsiasi momento. Un consumer di eventi permanente usa un set di oggetti e filtri permanenti per acquisire un evento WMI. Analogamente a un consumer di eventi temporaneo, si configura una serie di oggetti e filtri WMI che acquisiscono un evento WMI. Quando si verifica un evento che corrisponde a un filtro, WMI carica il consumer di eventi permanente e invia una notifica sull'evento. Poiché un consumer permanente viene implementato nel repository WMI ed è un file eseguibile registrato in WMI, il consumer di eventi permanente opera e riceve eventi dopo la creazione e anche dopo un riavvio del sistema operativo, purché WMI sia in esecuzione. Per altre informazioni, vedere [Ricezione di eventi in qualsiasi momento.](receiving-events-at-all-times.md)

Gli script o le applicazioni che ricevono eventi hanno considerazioni speciali sulla sicurezza. Per altre informazioni, vedere [Protezione degli eventi WMI](securing-wmi-events.md).

Un'applicazione o uno script può usare un provider di eventi WMI predefinito che fornisce classi [consumer standard.](standard-consumer-classes.md) Ogni classe consumer standard risponde a un evento con un'azione diversa inviando un messaggio di posta elettronica o eseguendo uno script. Non è necessario scrivere codice del provider per usare una classe consumer standard per creare un consumer di eventi permanente. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="providing-events"></a>Fornire eventi

Un provider di eventi è un componente COM che invia un evento a WMI. È possibile creare un provider di eventi per inviare un evento in un'applicazione C++ o C#. La maggior parte dei provider di eventi gestisce un oggetto per WMI, ad esempio un'applicazione o un elemento hardware. Per altre informazioni, vedere [Scrittura di un provider di eventi](writing-an-event-provider.md).

Un evento a tempo o ripetuto è un evento che si verifica in un momento predeterminato.

WMI offre i modi seguenti per creare eventi a tempo o ripetuti per le applicazioni:

-   Infrastruttura di eventi Microsoft standard.
-   Classe timer specializzata.

Per altre informazioni, vedere [Ricezione di un evento a tempo o ripetuto](receiving-a-timed-or-repeating-event.md). Quando si scrive un provider di eventi, prendere in considerazione le informazioni di sicurezza identificate in [Fornire eventi in modo sicuro.](providing-events-securely.md)

È consigliabile compilare le sottoscrizioni di eventi permanenti nello spazio \\ dei nomi della sottoscrizione \\ radice. Per altre informazioni, vedere [Implementazione di sottoscrizioni di eventi permanenti tra spazi dei nomi](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Quote di sottoscrizione

Il polling degli eventi può ridurre le prestazioni per i provider che supportano query su set di dati di grandi dimensioni. Inoltre, qualsiasi utente con accesso in lettura a uno spazio dei nomi con provider dinamici può eseguire un attacco Denial of Service (DoS). WMI gestisce le quote per tutti gli utenti combinati e per ogni consumer di eventi nella singola istanza di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md) che si trova nello spazio \\ dei nomi radice. Queste quote sono globali anziché per ogni spazio dei nomi. Non è possibile modificare le quote.

WMI applica attualmente le quote usando le proprietà di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). Ogni quota ha una versione per utente e una versione totale che include tutti gli utenti combinati, non per ogni spazio dei nomi. Nella tabella seguente sono elencate le quote che si applicano alle proprietà **\_ \_ di ArbitratorConfiguration.**



| Totale/PerUtente                                                                   | Quota                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| TemporarySubscriptionsTotal<br/> TemporarySubscriptionsPerUser<br/> | 10,000<br/> 1\.000<br/>                                          |
| PermanentSubscriptionsTotal<br/> PermanentSubscriptionsPerUser<br/> | 10,000<br/> 1\.000<br/>                                          |
| PollingInstructionsTotal<br/> PollingInstructionsPerUser<br/>       | 10,000<br/> 1\.000<br/>                                          |
| PollingMemoryTotal<br/> PollingMemoryPerUser<br/>                   | 10.000.000 (0x989680) byte<br/> 5.000.000 (0x4CB40) byte<br/> |



 

Un amministratore o un utente con **autorizzazione FULL \_ WRITE** nello spazio dei nomi può modificare l'istanza singleton di [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md). WMI tiene traccia della quota per utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

