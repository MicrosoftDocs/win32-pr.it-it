---
title: Registrare e visualizzare eventi TraceLogging
description: Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con Windows analizzatore prestazioni (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c77c1a1759988252f57c1ec54dca77cffaa21832878ead6ba8a827df3329fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966545"
---
# <a name="record-and-view-tracelogging-events"></a>Registrare e visualizzare eventi TraceLogging

Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con Windows analizzatore prestazioni (WPA).

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10
-   La Windows 10 di Windows Performance Recorder (WPR) e la versione Windows 10 di Windows analizzatore prestazioni (WPA), che fa parte di Windows® Assessment and Deployment Kit (Windows ADK).

> [!IMPORTANT]
> Le tracce acquisite con TraceLogging devono essere acquisite con la versione Windows 10 di Windows Performance Recorder e visualizzate con la Windows 10 di Windows analizzatore prestazioni. Se non è possibile acquisire o decodificare gli eventi, verificare di usare la Windows 10 degli strumenti.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. Acquisire i dati di traccia con WPR

Per acquisire una traccia in Windows Phone, vedere Acquisire eventi TraceLogging Windows Phone di seguito.

Creare un Windows registratore di prestazioni (con estensione wprp) in modo che sia possibile usare la richiesta WPR per acquisire gli eventi di Tracelogging.

**Creare un oggetto . File WPRP**

1.  Usare l'esempio WPRP seguente con l'esempio di codice nativo nel [Avvio rapido TraceLogging C/C++](tracelogging-native-quick-start.md) o l'esempio gestito nell'Avvio rapido [TraceLogging.](tracelogging-managed-quick-start.md) Se si stanno registrare eventi dal proprio provider, sostituire le `TODO` sezioni con i valori appropriati per il provider.

    > \[! Importante\]  

     

    Se si usa la guida introduttiva a TraceLogging C/C++, specificare il GUID del provider `Name` nell'attributo `<EventProvider>` dell'elemento . Ad esempio: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Se si usa la guida introduttiva tracelogging gestita, specificare il nome del provider preceduto da ' \* ' `Name` nell'attributo `<EventProvider />` dell'elemento . Ad esempio, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    File WPRP di esempio.

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  Salvare il file con . Estensione di file WPRP.
3.  Avviare l'acquisizione usando WPR da una finestra del prompt dei comandi con privilegi elevati (esegui come amministratore).

    **<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**

    > \[! mancia\]  
    > Per scopi di profilatura generali, è anche possibile aggiungere **–start GeneralProfile** alla riga di comando di wpr.exe per acquisire gli eventi di sistema insieme agli eventi del provider. Se si vogliono raccogliere solo gli eventi, omettere **-start GeneralProfile**.

     

4.  Eseguire l'applicazione che contiene gli eventi.
5.  Arrestare l'acquisizione della traccia.

    **<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**

    > \[! mancia\]  
    > Se è stato aggiunto **–start GeneralProfile** per raccogliere gli eventi di sistema, aggiungere **-stop GeneralProfile** allawpr.exe **comando** precedente.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. Acquisire eventi TraceLogging in Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Avviare tracelog per acquisire gli eventi dal provider.

    **cmdd tracelog -start test -f c: \\ test.etl -guid \# providerguid**

2.  Eseguire lo scenario di test per registrare gli eventi.
3.  Arrestare l'acquisizione della traccia.

    **cmdd tracelog -stop test**

4.  Unire i risultati della traccia di sistema con i risultati della traccia.

    **cmdd xperf -merge c: \\ test.etl c: \\ testmerged.etl**

5.  Recuperare il file di log unito.

    **getd c: \\ testmerged.etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. Visualizzare i dati di TraceLogging usando Windows analizzatore prestazioni.

WPA è attualmente l'unico visualizzatore che è possibile usare per visualizzare i file di traccia TraceLogging (con estensione etl).

1.  Avviare WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults.etl**

2.  Caricare il file di traccia (con estensione etl) specificato nel comando wpa.exe precedente, ad esempio traceLoggingResults.etl.
3.  Visualizzare gli eventi del provider. In WPA Graph Explorer espandere Attività **di sistema**.
4.  Fare doppio clic nel **riquadro Eventi generici** per visualizzare gli eventi nel **riquadro** Analisi.

    ![espandere eventi generici](images/expandsystemactivity.png)

5.  Nel riquadro Analisi individuare gli eventi del provider per verificare che TraceLogging funzioni.

    Nella colonna **Nome provider** della tabella **Eventi** generici individuare e selezionare la riga con il nome del provider.

    Se sono disponibili più provider da ordinare, fare clic sull'intestazione di colonna per ordinare in base al nome della colonna, in modo da semplificare l'individuazione del provider.

    Quando si trova il provider, fare clic con il pulsante destro del mouse sul nome e **scegliere Filtra in selezione**.

    ![filtrare la selezione al provider](images/filtertoselection.png)

    L'evento per SimpleTraceLoggingProvider e il relativo valore verranno visualizzati nel riquadro inferiore della finestra Analisi. Espandere il nome del provider per visualizzare gli eventi.

    ![visualizzare l'evento da simpletraceloggingprovider](images/eventview.png)

    Per altre informazioni sull'uso di WPA, [vedere Windows analizzatore prestazioni](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Il processo per la registrazione e la visualizzazione degli eventi ETW con WPR e WPA si applica altrettanto bene agli eventi TraceLogging.

Per altri esempi di TraceLogging, vedere Esempi di [tracelogging C/C++.](tracelogging-c-cpp-tracelogging-examples.md)

 

 