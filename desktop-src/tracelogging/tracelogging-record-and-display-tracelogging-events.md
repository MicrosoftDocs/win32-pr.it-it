---
title: Registrare e visualizzare gli eventi TraceLogging
description: Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con Windows Performance Analyzer (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872913"
---
# <a name="record-and-view-tracelogging-events"></a>Registrare e visualizzare gli eventi TraceLogging

Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con Windows Performance Analyzer (WPA).

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10
-   La versione Windows 10 di Windows Performance Recorder (WPR) e la versione Windows 10 di Windows Performance Analyzer (WPA) che fa parte di Windows® Assessment and Deployment Kit (Windows ADK).

> [!IMPORTANT]
> Le tracce acquisite con TraceLogging devono essere acquisite con la versione Windows 10 di Windows Performance Recorder e visualizzate con la versione Windows 10 di Windows Performance Analyzer. Se non si è in grado di acquisire o decodificare gli eventi, verificare che sia in uso la versione di Windows 10 degli strumenti.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. acquisire i dati di traccia con WPR

Per acquisire una traccia in Windows Phone, vedere la pagina relativa all'acquisizione di eventi TraceLogging in Windows Phone di seguito.

Creare un profilo di registrazione prestazioni Windows (con estensione WPRP) in modo da poter usare WPR per acquisire gli eventi Tracelogging.

**Creare un oggetto. File WPRP**

1.  Usare l'esempio di WPRP seguente con l'esempio di codice nativo in [TraceLogging C/C++ avvio rapido](tracelogging-native-quick-start.md) o l'esempio gestito nel [avvio rapido gestito TraceLogging](tracelogging-managed-quick-start.md). Se si registrano eventi dal proprio provider, sostituire le `TODO` sezioni con i valori appropriati per il provider.

    > \[! Importante\]  

     

    Se si usa la Guida introduttiva di TraceLogging C/C++, specificare il GUID del provider nell' `Name` attributo dell' `<EventProvider>` elemento. Ad esempio: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Se si usa la Guida introduttiva di TraceLogging gestita, specificare il nome del provider preceduto da' \* ' nell' `Name` attributo dell' `<EventProvider />` elemento. Ad esempio: `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

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

    

2.  Salvare il file con un. Estensione del nome di file WPRP.
3.  Avviare l'acquisizione usando WPR da una finestra del prompt dei comandi con privilegi elevati (Esegui come amministratore).

    **<path to wpr>\\wpr.exe-avviare GeneralProfile-Start TraceLoggingProvider. WPRP**

    > \[! Punta\]  
    > Ai fini della profilatura generale, è anche possibile aggiungere **– Start GeneralProfile** alla riga di comando wpr.exe per acquisire gli eventi di sistema insieme agli eventi del provider. Se si vuole solo raccogliere gli eventi, omettere **-Start GeneralProfile**.

     

4.  Eseguire l'applicazione che contiene gli eventi.
5.  Arrestare l'acquisizione della traccia.

    **<path to wpr>\\wpr.exe-arresta la descrizione di TraceCaptureFile. etl**

    > \[! Punta\]  
    > Se è stato aggiunto, **avviare GeneralProfile** per raccogliere gli eventi di sistema, aggiungere **-Stop GeneralProfile** alla riga di comando **wpr.exe** precedente.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. acquisire gli eventi TraceLogging nel Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Avviare tracelog per acquisire gli eventi dal provider.

    **CMDD tracelog-Start test-f c: \\ test. etl-GUID \# ProviderGuid**

2.  Eseguire lo scenario di test per registrare gli eventi.
3.  Arrestare l'acquisizione della traccia.

    **CMDD tracelog-Interrompi test**

4.  Unire i risultati della traccia di sistema con i risultati della traccia.

    **CMDD Xperf-merge c: \\ test. etl c: \\ testmerged. etl**

5.  Recuperare il file di log Unito.

    **GetD c: \\ testmerged. etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. visualizzare i dati di TraceLogging tramite Windows Performance Analyzer.

WPA è attualmente l'unico visualizzatore che è possibile usare per visualizzare i file di traccia TraceLogging (con estensione ETL).

1.  Avviare WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults. etl**

2.  Caricare il file di traccia (con estensione ETL) specificato nel comando wpa.exe precedente, ad esempio traceLoggingResults. etl.
3.  Visualizzare gli eventi del provider. In WPA Graph Explorer espandere attività del **sistema**.
4.  Fare doppio clic nel riquadro **eventi generici** per visualizzare gli eventi nel riquadro **analisi** .

    ![Espandi eventi generici](images/expandsystemactivity.png)

5.  Nel riquadro analisi individuare gli eventi del provider per verificare il corretto funzionamento di TraceLogging.

    Nella colonna **Nome provider** della tabella **eventi generici** trovare e selezionare la riga con il nome del provider.

    Se si dispone di più provider da ordinare, fare clic sull'intestazione di colonna per eseguire l'ordinamento in base al nome della colonna, che può semplificare la ricerca del provider.

    Quando si trova il provider, fare clic con il pulsante destro del mouse sul nome e selezionare **filtro per selezione**.

    ![Filtra selezione per provider](images/filtertoselection.png)

    L'evento per SimpleTraceLoggingProvider e il relativo valore verranno visualizzati nel riquadro inferiore della finestra di analisi. Espandere il nome del provider per visualizzare gli eventi.

    ![visualizzare l'evento da simpletraceloggingprovider](images/eventview.png)

    Per ulteriori informazioni sull'utilizzo di WPA, vedere [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Il processo per la registrazione e la visualizzazione di eventi ETW tramite WPR e WPA si applica anche agli eventi TraceLogging.

Vedere [esempi di Tracelogging in C/C++](tracelogging-c-cpp-tracelogging-examples.md) per altri esempi di Tracelogging.

 

 