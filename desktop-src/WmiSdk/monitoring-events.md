---
description: Gli amministratori di sistema possono usare WMI per monitorare gli eventi in una rete.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Monitoraggio degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90a0a6eef87f88543e8f2414bc38bdea4f7d89c577471d79d23393f331b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317115"
---
# <a name="monitoring-events"></a>Monitoraggio degli eventi

Gli amministratori di sistema possono usare WMI per monitorare gli eventi in una rete. Esempio:

-   Un servizio si arresta in modo imprevisto.
-   Un server diventa non disponibile.
-   Un'unità disco riempie l'80% di capacità.
-   Gli eventi di sicurezza vengono segnalati a un registro eventi NT.

WMI supporta il rilevamento e il recapito degli eventi ai consumer di eventi perché alcuni provider WMI sono provider di eventi. Per altre informazioni, vedere [Ricezione di un evento WMI.](receiving-a-wmi-event.md)

[*I consumer di*](gloss-e.md) eventi sono applicazioni o script che richiedono la notifica degli eventi e quindi eseguono attività quando si verificano eventi specifici. È possibile creare script di monitoraggio degli eventi o applicazioni che monitorano temporaneamente quando si verificano eventi. WMI fornisce anche un set di provider di eventi permanenti preinstallati e le classi consumer permanenti che consentono di monitorare in modo permanente gli eventi. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

In questo argomento vengono illustrate le sezioni seguenti:

-   [Uso di consumer di eventi temporanei](#using-temporary-event-consumers)
-   [Uso di consumer di eventi permanenti](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a>Uso di consumer di eventi temporanei

I consumer di eventi temporanei sono script o applicazioni che restituiscono gli eventi che corrispondono a una query o a un filtro di eventi. Le query di eventi temporanei usano in [**genere IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) nelle applicazioni C++ [**oSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) negli script e Visual Basic.

Una query di eventi richiede istanze di una classe di evento che specifica un determinato tipo di evento, ad esempio [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) o [**RegistryKeyChangeEvent.**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)

L'esempio di codice VBScript seguente richiede una notifica quando viene creata [**un'istanza di Win32 \_ ProcessTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) Un'istanza di questa classe viene generata all'avvio o all'arresto di un processo.

Per eseguire lo script, copiarlo in un file denominato event.vbs e usare la riga di comando seguente: **cscript event.vbs**. È possibile visualizzare l'output dello script avviando Notepad.exe o qualsiasi altro processo. Lo script viene arrestato dopo l'avvio o l'arresto di cinque processi.

Questo script chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), che è la versione [*semisincronous*](gloss-s.md) del metodo. Vedere lo script successivo per un esempio di configurazione di una sottoscrizione di eventi temporanei asincrona chiamando [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md). Lo script chiama [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) per ottenere ed elaborare ogni evento non appena arriva. Salvare lo script in un file con estensione vbs ed eseguire lo script in una riga di comando usando CScript: **cscript file.vbs**.


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



I consumer di eventi temporanei devono essere avviati manualmente e non devono essere mantenuti tra riavvii WMI o riavvii del sistema operativo. Un consumer di eventi temporaneo può elaborare gli eventi solo mentre è in esecuzione.

La procedura seguente descrive come creare un consumer di eventi temporaneo.

**Per creare un consumer di eventi temporaneo**

1.  Decidere quale linguaggio di programmazione usare.

    Il linguaggio di programmazione determina l'API da usare.

    -   Per il linguaggio di programmazione C++, usare [l'API COM per WMI.](com-api-for-wmi.md)
    -   Per Visual Basic o linguaggi di scripting, usare [l'API scripting per WMI.](scripting-api-for-wmi.md)

2.  Iniziare a codificare un'applicazione consumer di eventi temporanea nello stesso modo in cui si avvia un'applicazione WMI.

    I primi passaggi della codifica dipendono dal linguaggio di programmazione. In genere, si accede a WMI e si configurano le impostazioni di sicurezza. Per altre informazioni, vedere [Creazione di un'applicazione WMI o di uno script](creating-a-wmi-application-or-script.md).

3.  Definire la query di eventi da usare.

    Per ottenere alcuni tipi di dati sulle prestazioni, potrebbe essere necessario usare le classi fornite dai provider ad alte prestazioni. Per altre informazioni, vedere [Monitoraggio dei dati sulle prestazioni,](monitoring-performance-data.md)Determinazione del tipo di evento da [ricevere](determining-the-type-of-event-to-receive.md)ed Esecuzione di query [con WQL.](querying-with-wql.md)

4.  Decidere di effettuare una chiamata asincrona o una chiamata semisincrona e scegliere il metodo API.

    Le chiamate asincrone consentono di evitare il sovraccarico del polling dei dati. Tuttavia, le chiamate semisincronose offrono prestazioni simili con maggiore sicurezza. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

5.  Eseguire la chiamata al metodo asincrona o semisincrona e includere una query di eventi come *parametro strQuery.*

    Per le applicazioni C++, chiamare i metodi seguenti:

    -   [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    Per gli script, chiamare i metodi seguenti:

    -   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
    -   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)

6.  Scrivere il codice per elaborare l'oggetto evento restituito.

    Per le query di eventi asincrone, inserire il codice nei vari metodi o eventi dell'object sink. Per le query di eventi semisincronous, ogni oggetto viene restituito quando WMI lo ottiene, quindi il codice deve essere nel ciclo che gestisce ogni oggetto.

L'esempio di codice di script seguente è una versione asincrona dello script [**\_ Win32 ProcessTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) Poiché le operazioni asincrone vengono restituite immediatamente, una finestra di dialogo mantiene lo script attivo mentre è in attesa di eventi.

Anziché chiamare [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) per ricevere ogni evento, lo script dispone di un gestore eventi per [**l'evento SWbemSink OnObjectReady.**](swbemsink-onobjectready.md)


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
> Un callback asincrono, ad esempio un callback gestito dalla subroutine, consente a un utente non autenticato di fornire `SINK_OnObjectReady` dati al sink. Per una maggiore sicurezza, usare la comunicazione semisincrona o la comunicazione sincrona. Per altre informazioni, vedere i seguenti argomenti:
>
> -   [Esecuzione di una chiamata semisincrona con C++](making-a-semisynchronous-call-with-c--.md)
> -   [Esecuzione di una chiamata semisincrona con VBScript](making-a-semisynchronous-call-with-vbscript.md)
> -   [Esecuzione di una chiamata asincrona con C++](making-an-asynchronous-call-with-c--.md)
> -   [Esecuzione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md)
> -   [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md)
> -   [Protezione dei client di scripting](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a>Uso di consumer di eventi permanenti

Un consumer di eventi permanente viene eseguito fino a quando la registrazione non viene annullata in modo esplicito e quindi viene avviata al riavvio di WMI o del sistema.

Un consumer di eventi permanente è una combinazione di classi WMI, filtri e oggetti COM in un sistema.

L'elenco seguente identifica le parti necessarie per creare un consumer di eventi permanente:

-   Oggetto COM contenente il codice che implementa il consumer permanente.
-   Nuova classe consumer permanente.
-   Istanza della classe consumer permanente.
-   Filtro che contiene la query per gli eventi.
-   Collegamento tra il consumer e il filtro.

Per altre informazioni, vedere [Ricezione di eventi in qualsiasi momento.](--filtertoconsumerbinding.md)

WMI fornisce diversi consumer permanenti. Le classi consumer e l'oggetto COM che contiene il codice sono preinstallati. Ad esempio, è possibile creare e configurare un'istanza della [**classe ActiveScriptEventConsumer**](activescripteventconsumer.md) per eseguire uno script quando si verifica un evento. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md) Per un esempio di uso **di ActiveScriptEventConsumer,** vedere Esecuzione di [uno script basato su un evento](running-a-script-based-on-an-event.md).

La procedura seguente descrive come creare un consumer di eventi permanente.

**Per creare un consumer di eventi permanente**

1.  [Registrare il provider di](registering-a-provider.md) eventi con lo spazio dei nomi in uso.

    Alcuni provider di eventi possono usare solo uno spazio dei nomi specifico. Ad esempio, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) è un evento intrinseco supportato dal [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider) ed è registrato per impostazione predefinita con lo spazio \\ dei nomi \\ cimv2 radice.

    > [!Note]  
    > È possibile usare la **proprietà EventNamespace** di [**\_ \_ EventFilter**](--eventfilter.md) usata nella registrazione per creare una sottoscrizione tra spazi dei nomi. Per altre informazioni, vedere [Implementazione di sottoscrizioni di eventi permanenti tra spazi dei nomi](implementing-cross-namespace-permanent-event-subscriptions.md).

     

2.  [Registrare il provider di consumer di](registering-an-event-consumer-provider.md) eventi con lo spazio dei nomi in cui si trovano le classi di evento.

    WMI usa un provider di consumer di eventi per trovare un consumer di eventi permanente. Il consumer di eventi permanente è l'applicazione avviata da WMI quando viene ricevuto un evento. Per registrare il consumer di eventi, i provider creano istanze [**\_ \_ di EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).

3.  Creare un'istanza della classe che rappresenta il consumer di eventi permanente da usare.

    Le classi consumer di eventi derivano dalla [**\_ \_ classe EventConsumer**](--eventconsumer.md). Impostare le proprietà necessarie per l'istanza del consumer di eventi.

4.  Registrare il consumer con COM usando **l'utilità regsvr32.**
5.  Creare un'istanza della classe di filtro eventi [**\_ \_ EventFilter**](--eventfilter.md).

    Impostare i campi obbligatori per l'istanza del filtro eventi. I campi obbligatori per [**\_ \_ EventFilter**](--eventfilter.md) sono **Name,** **QueryLanguage** e **Query.** La **proprietà Name** può essere qualsiasi nome univoco per un'istanza di questa classe. La **proprietà QueryLanguage** è sempre impostata su "WQL". La **proprietà Query** è una stringa che contiene una query di eventi. Viene generato un evento quando la query di un consumer di eventi permanente ha esito negativo. L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.

6.  Creare un'istanza della [**\_ \_ classe FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare un consumer di eventi logico a un filtro eventi.

    WMI usa un'associazione per trovare il consumer di eventi associato all'evento che corrisponde ai criteri specificati nel filtro eventi. WMI usa il provider di consumer di eventi per trovare l'applicazione consumer di eventi permanente da avviare.

 

 
