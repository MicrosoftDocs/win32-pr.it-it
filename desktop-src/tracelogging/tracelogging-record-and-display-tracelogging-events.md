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
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="ace09-103">Registrare e visualizzare gli eventi TraceLogging</span><span class="sxs-lookup"><span data-stu-id="ace09-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="ace09-104">Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con Windows Performance Analyzer (WPA).</span><span class="sxs-lookup"><span data-stu-id="ace09-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ace09-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="ace09-105">Prerequisites</span></span>

-   <span data-ttu-id="ace09-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ace09-106">Windows 10</span></span>
-   <span data-ttu-id="ace09-107">La versione Windows 10 di Windows Performance Recorder (WPR) e la versione Windows 10 di Windows Performance Analyzer (WPA) che fa parte di Windows® Assessment and Deployment Kit (Windows ADK).</span><span class="sxs-lookup"><span data-stu-id="ace09-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ace09-108">Le tracce acquisite con TraceLogging devono essere acquisite con la versione Windows 10 di Windows Performance Recorder e visualizzate con la versione Windows 10 di Windows Performance Analyzer.</span><span class="sxs-lookup"><span data-stu-id="ace09-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="ace09-109">Se non si è in grado di acquisire o decodificare gli eventi, verificare che sia in uso la versione di Windows 10 degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ace09-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="ace09-110">1. acquisire i dati di traccia con WPR</span><span class="sxs-lookup"><span data-stu-id="ace09-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="ace09-111">Per acquisire una traccia in Windows Phone, vedere la pagina relativa all'acquisizione di eventi TraceLogging in Windows Phone di seguito.</span><span class="sxs-lookup"><span data-stu-id="ace09-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="ace09-112">Creare un profilo di registrazione prestazioni Windows (con estensione WPRP) in modo da poter usare WPR per acquisire gli eventi Tracelogging.</span><span class="sxs-lookup"><span data-stu-id="ace09-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="ace09-113">**Creare un oggetto. File WPRP**</span><span class="sxs-lookup"><span data-stu-id="ace09-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="ace09-114">Usare l'esempio di WPRP seguente con l'esempio di codice nativo in [TraceLogging C/C++ avvio rapido](tracelogging-native-quick-start.md) o l'esempio gestito nel [avvio rapido gestito TraceLogging](tracelogging-managed-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="ace09-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="ace09-115">Se si registrano eventi dal proprio provider, sostituire le `TODO` sezioni con i valori appropriati per il provider.</span><span class="sxs-lookup"><span data-stu-id="ace09-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="ace09-116">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="ace09-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="ace09-117">Se si usa la Guida introduttiva di TraceLogging C/C++, specificare il GUID del provider nell' `Name` attributo dell' `<EventProvider>` elemento.</span><span class="sxs-lookup"><span data-stu-id="ace09-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="ace09-118">Ad esempio: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span><span class="sxs-lookup"><span data-stu-id="ace09-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="ace09-119">Se si usa la Guida introduttiva di TraceLogging gestita, specificare il nome del provider preceduto da' \* ' nell' `Name` attributo dell' `<EventProvider />` elemento.</span><span class="sxs-lookup"><span data-stu-id="ace09-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="ace09-120">Ad esempio: `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span><span class="sxs-lookup"><span data-stu-id="ace09-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="ace09-121">File WPRP di esempio.</span><span class="sxs-lookup"><span data-stu-id="ace09-121">Sample WPRP file.</span></span>

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

    

2.  <span data-ttu-id="ace09-122">Salvare il file con un. Estensione del nome di file WPRP.</span><span class="sxs-lookup"><span data-stu-id="ace09-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="ace09-123">Avviare l'acquisizione usando WPR da una finestra del prompt dei comandi con privilegi elevati (Esegui come amministratore).</span><span class="sxs-lookup"><span data-stu-id="ace09-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="ace09-124">**<path to wpr>\\wpr.exe-avviare GeneralProfile-Start TraceLoggingProvider. WPRP**</span><span class="sxs-lookup"><span data-stu-id="ace09-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="ace09-125">\[! Punta\]</span><span class="sxs-lookup"><span data-stu-id="ace09-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="ace09-126">Ai fini della profilatura generale, è anche possibile aggiungere **– Start GeneralProfile** alla riga di comando wpr.exe per acquisire gli eventi di sistema insieme agli eventi del provider.</span><span class="sxs-lookup"><span data-stu-id="ace09-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="ace09-127">Se si vuole solo raccogliere gli eventi, omettere **-Start GeneralProfile**.</span><span class="sxs-lookup"><span data-stu-id="ace09-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="ace09-128">Eseguire l'applicazione che contiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ace09-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="ace09-129">Arrestare l'acquisizione della traccia.</span><span class="sxs-lookup"><span data-stu-id="ace09-129">Stop the trace capture.</span></span>

    <span data-ttu-id="ace09-130">**<path to wpr>\\wpr.exe-arresta la descrizione di TraceCaptureFile. etl**</span><span class="sxs-lookup"><span data-stu-id="ace09-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="ace09-131">\[! Punta\]</span><span class="sxs-lookup"><span data-stu-id="ace09-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="ace09-132">Se è stato aggiunto, **avviare GeneralProfile** per raccogliere gli eventi di sistema, aggiungere **-Stop GeneralProfile** alla riga di comando **wpr.exe** precedente.</span><span class="sxs-lookup"><span data-stu-id="ace09-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="ace09-133">2. acquisire gli eventi TraceLogging nel Windows Phone</span><span class="sxs-lookup"><span data-stu-id="ace09-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="ace09-134">Avviare tracelog per acquisire gli eventi dal provider.</span><span class="sxs-lookup"><span data-stu-id="ace09-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="ace09-135">**CMDD tracelog-Start test-f c: \\ test. etl-GUID \# ProviderGuid**</span><span class="sxs-lookup"><span data-stu-id="ace09-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="ace09-136">Eseguire lo scenario di test per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ace09-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="ace09-137">Arrestare l'acquisizione della traccia.</span><span class="sxs-lookup"><span data-stu-id="ace09-137">Stop trace capture.</span></span>

    <span data-ttu-id="ace09-138">**CMDD tracelog-Interrompi test**</span><span class="sxs-lookup"><span data-stu-id="ace09-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="ace09-139">Unire i risultati della traccia di sistema con i risultati della traccia.</span><span class="sxs-lookup"><span data-stu-id="ace09-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="ace09-140">**CMDD Xperf-merge c: \\ test. etl c: \\ testmerged. etl**</span><span class="sxs-lookup"><span data-stu-id="ace09-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="ace09-141">Recuperare il file di log Unito.</span><span class="sxs-lookup"><span data-stu-id="ace09-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="ace09-142">**GetD c: \\ testmerged. etl**</span><span class="sxs-lookup"><span data-stu-id="ace09-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="ace09-143">3. visualizzare i dati di TraceLogging tramite Windows Performance Analyzer.</span><span class="sxs-lookup"><span data-stu-id="ace09-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="ace09-144">WPA è attualmente l'unico visualizzatore che è possibile usare per visualizzare i file di traccia TraceLogging (con estensione ETL).</span><span class="sxs-lookup"><span data-stu-id="ace09-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="ace09-145">Avviare WPA.</span><span class="sxs-lookup"><span data-stu-id="ace09-145">Start WPA.</span></span>

    <span data-ttu-id="ace09-146">**<path to wpr>\\wpa.exe traceLoggingResults. etl**</span><span class="sxs-lookup"><span data-stu-id="ace09-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="ace09-147">Caricare il file di traccia (con estensione ETL) specificato nel comando wpa.exe precedente, ad esempio traceLoggingResults. etl.</span><span class="sxs-lookup"><span data-stu-id="ace09-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="ace09-148">Visualizzare gli eventi del provider.</span><span class="sxs-lookup"><span data-stu-id="ace09-148">View your provider events.</span></span> <span data-ttu-id="ace09-149">In WPA Graph Explorer espandere attività del **sistema**.</span><span class="sxs-lookup"><span data-stu-id="ace09-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="ace09-150">Fare doppio clic nel riquadro **eventi generici** per visualizzare gli eventi nel riquadro **analisi** .</span><span class="sxs-lookup"><span data-stu-id="ace09-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![Espandi eventi generici](images/expandsystemactivity.png)

5.  <span data-ttu-id="ace09-152">Nel riquadro analisi individuare gli eventi del provider per verificare il corretto funzionamento di TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="ace09-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="ace09-153">Nella colonna **Nome provider** della tabella **eventi generici** trovare e selezionare la riga con il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="ace09-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="ace09-154">Se si dispone di più provider da ordinare, fare clic sull'intestazione di colonna per eseguire l'ordinamento in base al nome della colonna, che può semplificare la ricerca del provider.</span><span class="sxs-lookup"><span data-stu-id="ace09-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="ace09-155">Quando si trova il provider, fare clic con il pulsante destro del mouse sul nome e selezionare **filtro per selezione**.</span><span class="sxs-lookup"><span data-stu-id="ace09-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![Filtra selezione per provider](images/filtertoselection.png)

    <span data-ttu-id="ace09-157">L'evento per SimpleTraceLoggingProvider e il relativo valore verranno visualizzati nel riquadro inferiore della finestra di analisi.</span><span class="sxs-lookup"><span data-stu-id="ace09-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="ace09-158">Espandere il nome del provider per visualizzare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ace09-158">Expand the provider name to see the events.</span></span>

    ![visualizzare l'evento da simpletraceloggingprovider](images/eventview.png)

    <span data-ttu-id="ace09-160">Per ulteriori informazioni sull'utilizzo di WPA, vedere [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="ace09-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="ace09-161">Riepilogo e passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="ace09-161">Summary and next steps</span></span>

<span data-ttu-id="ace09-162">Il processo per la registrazione e la visualizzazione di eventi ETW tramite WPR e WPA si applica anche agli eventi TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="ace09-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="ace09-163">Vedere [esempi di Tracelogging in C/C++](tracelogging-c-cpp-tracelogging-examples.md) per altri esempi di Tracelogging.</span><span class="sxs-lookup"><span data-stu-id="ace09-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 