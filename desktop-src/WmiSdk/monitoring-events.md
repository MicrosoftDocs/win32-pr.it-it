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
# <a name="monitoring-events"></a>Monitoraggio degli eventi

Gli amministratori di sistema possono utilizzare WMI per monitorare gli eventi in una rete. Ad esempio:

-   Un servizio viene arrestato in modo imprevisto.
-   Un server diventa non disponibile.
-   Un'unità disco si riempie della capacità del 80%.
-   Gli eventi di sicurezza vengono segnalati a un registro eventi NT.

WMI supporta il rilevamento e il recapito di eventi ai consumer di eventi perché alcuni provider WMI sono provider di eventi. Per ulteriori informazioni, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).

[*I consumer di eventi*](gloss-e.md) sono applicazioni o script che richiedono la notifica di eventi, quindi eseguono attività quando si verificano eventi specifici. È possibile creare script o applicazioni di monitoraggio degli eventi che monitorano temporaneamente quando si verificano gli eventi. WMI fornisce inoltre un set di provider di eventi permanenti preinstallati e le classi consumer permanenti che consentono di monitorare in modo permanente gli eventi. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Utilizzo di consumer di eventi temporanei](#using-temporary-event-consumers)
-   [Utilizzo di consumer di eventi permanenti](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Utilizzo di consumer di eventi temporanei

I consumer di eventi temporanei sono script o applicazioni che restituiscono gli eventi che corrispondono a una query o a un filtro di eventi. Le query di eventi temporanei usano in genere [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) nelle applicazioni C++ o [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) negli script e Visual Basic.

Una query di eventi richiede le istanze di una classe di evento che specifica un determinato tipo di evento, ad esempio [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) o [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

Nell'esempio di codice VBScript seguente viene richiesta una notifica quando viene creata un'istanza di [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) . Un'istanza di questa classe viene generata quando un processo viene avviato o arrestato.

Per eseguire lo script, copiarlo in un file denominato event.vbs e utilizzare la riga di comando seguente: **cscript event.vbs**. È possibile visualizzare l'output dello script avviando Notepad.exe o qualsiasi altro processo. Lo script si interrompe dopo cinque processi avviati o arrestati.

Questo script chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), che è la versione [*semisincrono*](gloss-s.md) del metodo. Vedere lo script successivo per un esempio di configurazione di una sottoscrizione di eventi temporanei asincrona chiamando [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md). Lo script chiama [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) per ottenere ed elaborare ogni evento al suo arrivo. Salvare lo script in un file con estensione vbs ed eseguire lo script in una riga di comando usando CScript: **cscript file.vbs**.


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



I consumer di eventi temporanei devono essere avviati manualmente e non devono essere mantenuti tra i riavvii WMI o i riavvii del sistema operativo. Un consumer di eventi temporaneo può elaborare gli eventi solo mentre è in esecuzione.

Nella procedura riportata di seguito viene descritto come creare un consumer di eventi temporaneo.

**Per creare un consumer di eventi temporaneo**

1.  Decidere quale linguaggio di programmazione usare.

    Il linguaggio di programmazione determina l'API da usare.

    -   Per il linguaggio di programmazione C++, usare l' [API com per WMI](com-api-for-wmi.md).
    -   Per Visual Basic o linguaggi di scripting, usare l' [API di scripting per WMI](scripting-api-for-wmi.md).

2.  Avviare la codifica di un'applicazione consumer di eventi temporanei nello stesso modo in cui si avvia un'applicazione WMI.

    I primi passaggi della codifica dipendono dal linguaggio di programmazione. In genere, si accede a WMI e si configurano le impostazioni di sicurezza. Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).

3.  Definire la query di eventi che si desidera utilizzare.

    Per ottenere alcuni tipi di dati sulle prestazioni, potrebbe essere necessario utilizzare le classi fornite dai provider a prestazioni elevate. Per altre informazioni, vedere [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md), [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md)ed [esecuzione di query con WQL](querying-with-wql.md).

4.  Decidere di effettuare una chiamata asincrona o una chiamata semisincrono e scegliere il metodo API.

    Le chiamate asincrone consentono di evitare l'overhead del polling dei dati. Tuttavia, le chiamate semisincrono offrono prestazioni simili con una maggiore sicurezza. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

5.  Eseguire la chiamata al metodo asincrono o semisincrono e includere una query di eventi come parametro *strQuery* .

    Per le applicazioni C++, chiamare i metodi seguenti:

    -   [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Per gli script, chiamare i metodi seguenti:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Scrivere il codice per elaborare l'oggetto evento restituito.

    Per le query di eventi asincroni, inserire il codice nei vari metodi o eventi del sink di oggetto. Per le query di eventi semisincrono, ogni oggetto viene restituito come WMI lo ottiene, quindi il codice deve essere nel ciclo che gestisce ciascun oggetto.

Il seguente esempio di codice di script è una versione asincrona dello script [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) . Poiché le operazioni asincrone vengono restituite immediatamente, una finestra di dialogo mantiene attivo lo script mentre è in attesa di eventi.

Anziché chiamare [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) per ricevere ogni evento, lo script dispone di un gestore eventi per l'evento [**OnObjectReady di SWbemSink**](swbemsink-onobjectready.md) .


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
> Un callback asincrono, ad esempio un callback gestito dalla `SINK_OnObjectReady` subroutine, consente a un utente non autenticato di fornire dati al sink. Per una maggiore sicurezza, usare la comunicazione semisincrono o la comunicazione sincrona. Per altre informazioni, vedere i seguenti argomenti:
>
> -   [Esecuzione di una chiamata semisincrono con C++](making-a-semisynchronous-call-with-c--.md)
> -   [Esecuzione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Esecuzione di una chiamata asincrona con C++](making-an-asynchronous-call-with-c--.md)
> -   [Esecuzione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md)
> -   [Protezione dei client di scripting](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Utilizzo di consumer di eventi permanenti

Un consumer di eventi permanente viene eseguito finché la registrazione non viene annullata in modo esplicito e quindi viene avviata al riavvio di WMI o del sistema.

Un consumer di eventi permanenti è una combinazione di classi WMI, filtri e oggetti COM in un sistema.

Nell'elenco seguente vengono identificate le parti necessarie per creare un consumer di eventi permanente:

-   Oggetto COM contenente il codice che implementa l'utente permanente.
-   Nuova classe consumer permanente.
-   Istanza della classe consumer permanente.
-   Filtro che contiene la query per gli eventi.
-   Collegamento tra l'utente e il filtro.

Per ulteriori informazioni, vedere [ricezione di eventi in qualsiasi momento](--filtertoconsumerbinding.md).

WMI fornisce diversi consumer permanenti. Le classi consumer e l'oggetto COM che contiene il codice sono preinstallati. Ad esempio, è possibile creare e configurare un'istanza della classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per eseguire uno script quando si verifica un evento. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). Per un esempio dell'uso di **ActiveScriptEventConsumer**, vedere [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md).

Nella procedura seguente viene descritto come creare un consumer di eventi permanenti.

**Per creare un consumer di eventi permanenti**

1.  [Registrare il provider di eventi](registering-a-provider.md) con lo spazio dei nomi in uso.

    Alcuni provider di eventi possono utilizzare solo uno spazio dei nomi specifico. Ad esempio, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) è un evento intrinseco supportato dal [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) e viene registrato per impostazione predefinita con lo \\ \\ spazio dei nomi CIMV2 radice.

    > [!Note]  
    > Per creare una sottoscrizione tra più spazi dei nomi, è possibile utilizzare la proprietà **EventNamespace** di [**\_ \_ EventFilter**](--eventfilter.md) utilizzata nella registrazione. Per altre informazioni, vedere [implementazione delle sottoscrizioni di eventi permanenti tra spazi dei nomi](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registrare il provider di consumer di eventi](registering-an-event-consumer-provider.md) con lo spazio dei nomi in cui si trovano le classi di evento.

    WMI utilizza un provider di consumer di eventi per trovare un consumer di eventi permanente. Il consumer di eventi permanenti è l'applicazione che WMI inizia quando viene ricevuto un evento. Per registrare un consumer di eventi, i provider creano istanze di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Creare un'istanza della classe che rappresenti il consumer di eventi permanenti che si desidera utilizzare.

    Le classi consumer di eventi sono derivate dalla classe [**\_ \_ EventConsumer**](--eventconsumer.md). Impostare le proprietà richieste dall'istanza del consumer di eventi.

4.  Registrare il consumer con COM utilizzando l'utilità **regsvr32** .
5.  Creare un'istanza della classe filtro eventi [**\_ \_ EventFilter**](--eventfilter.md).

    Impostare i campi obbligatori per l'istanza del filtro eventi. I campi obbligatori per [**\_ \_ EventFilter**](--eventfilter.md) sono **Name**, **QueryLanguage** e **query**. La proprietà **Name** può essere un nome univoco per un'istanza di questa classe. La proprietà **QueryLanguage** è sempre impostata su "WQL". La proprietà **query** è una stringa che contiene una query di eventi. Un evento viene generato quando la query di un consumer di eventi permanenti ha esito negativo. L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.

6.  Creare un'istanza della classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare un consumer di eventi logici a un filtro eventi.

    WMI utilizza un'associazione per trovare il consumer di eventi associato all'evento che corrisponde ai criteri specificati nel filtro eventi. WMI utilizza il provider di consumer di eventi per individuare l'applicazione del consumer di eventi permanente da avviare.

 

 
