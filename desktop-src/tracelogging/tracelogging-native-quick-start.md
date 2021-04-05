---
title: Avvio rapido C/C++ TraceLogging
description: Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice nativo in modalità utente.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2020
ms.locfileid: "103956239"
---
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="48974-103">Avvio rapido C/C++ TraceLogging</span><span class="sxs-lookup"><span data-stu-id="48974-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="48974-104">Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice nativo in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="48974-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="48974-105">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="48974-105">Prerequisites</span></span>

-   <span data-ttu-id="48974-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="48974-106">Windows 10</span></span>
-   <span data-ttu-id="48974-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="48974-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="48974-108">Il Software Development Kit (SDK) di Windows 10 è necessario per scrivere un provider in modalità utente</span><span class="sxs-lookup"><span data-stu-id="48974-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="48974-109">Windows Driver Kit (WDK) per Windows 10 è necessario per scrivere un provider in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="48974-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48974-110">Per compilare questi esempi, collegare Advapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="48974-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="48974-111">SimpleTraceLoggingExample. h</span><span class="sxs-lookup"><span data-stu-id="48974-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="48974-112">Questa intestazione di esempio include le API TraceLogging e in diretta dichiara l'handle del provider che verrà usato per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="48974-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="48974-113">Tutte le classi che desiderano utilizzare TraceLogging includono questa intestazione e possono quindi avviare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="48974-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="48974-114">Il file di intestazione include TraceLoggingProvider. h, che definisce l'API TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="48974-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="48974-115">È necessario includere innanzitutto Windows. h perché definisce le costanti utilizzate da TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="48974-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="48974-116">Il file di intestazione dichiara l'handle del provider `g_hMyComponentProvider` che passerà alle API TraceLogging per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="48974-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="48974-117">Questo handle deve essere accessibile a qualsiasi codice che desideri usare TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="48974-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="48974-118">[**TRACELOGGING \_ DECLARE \_ provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) è una macro che crea un `extern const TraceLoggingHProvider` handle usando il nome fornito, che nell'esempio precedente è `g_hMyComponentProvider` .</span><span class="sxs-lookup"><span data-stu-id="48974-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="48974-119">La variabile di handle del provider effettiva viene allocata in un file di codice.</span><span class="sxs-lookup"><span data-stu-id="48974-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="48974-120">SimpleTraceLoggingExample. cpp</span><span class="sxs-lookup"><span data-stu-id="48974-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="48974-121">Nell'esempio seguente viene registrato il provider, viene registrato un evento e viene annullata la registrazione del provider.</span><span class="sxs-lookup"><span data-stu-id="48974-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

<span data-ttu-id="48974-122">Nell'esempio precedente è incluso SimpleTraceLoggingExample. h che contiene la variabile globale del provider che il codice utilizzerà per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="48974-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="48974-123">La macro del [**\_ \_ provider TRACELOGGING define**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) alloca l'archiviazione e definisce la variabile dell'handle del provider.</span><span class="sxs-lookup"><span data-stu-id="48974-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="48974-124">Il nome della variabile fornito a questa macro deve corrispondere al nome usato nella macro del [**provider di \_ Dichiarazione \_ TRACELOGGING**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) nel file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="48974-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="48974-125">Questo handle rimarrà valido fino a quando si trova nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="48974-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="48974-126">Registrare l'handle del provider</span><span class="sxs-lookup"><span data-stu-id="48974-126">Register the provider handle</span></span>

<span data-ttu-id="48974-127">Prima di poter usare l'handle del provider per registrare gli eventi, è necessario chiamare [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) per registrare l'handle del provider.</span><span class="sxs-lookup"><span data-stu-id="48974-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="48974-128">Questa operazione viene in genere eseguita in Main () o DLLMain (), ma può essere eseguita in qualsiasi momento, purché preceda qualsiasi tentativo di registrare un evento.</span><span class="sxs-lookup"><span data-stu-id="48974-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="48974-129">Se si registra un evento prima della registrazione dell'handle del provider, non si verificherà alcun errore, ma l'evento non verrà registrato.</span><span class="sxs-lookup"><span data-stu-id="48974-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="48974-130">Il codice seguente riportato nell'esempio precedente registra l'handle del provider.</span><span class="sxs-lookup"><span data-stu-id="48974-130">The following code from the example above registers the provider handle.</span></span>

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="48974-131">Registra un evento Tracelogging</span><span class="sxs-lookup"><span data-stu-id="48974-131">Log a Tracelogging event</span></span>

<span data-ttu-id="48974-132">Dopo che il provider è stato registrato, il codice seguente registra un evento semplice.</span><span class="sxs-lookup"><span data-stu-id="48974-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="48974-133">La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) richiede fino a 99 argomenti e viene eseguita come diverse istruzioni.</span><span class="sxs-lookup"><span data-stu-id="48974-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="48974-134">Ciò significa che i valori registrati non devono essere oggetti temporanei C++.</span><span class="sxs-lookup"><span data-stu-id="48974-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="48974-135">Il nome dell'evento viene archiviato in formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="48974-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="48974-136">Non è necessario usare caratteri incorporati `null` nell'evento o in altri nomi di campo.</span><span class="sxs-lookup"><span data-stu-id="48974-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="48974-137">Non sono previsti altri limiti per i caratteri consentiti.</span><span class="sxs-lookup"><span data-stu-id="48974-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="48974-138">Ogni argomento che segue il nome dell'evento deve essere incapsulato all'interno di una [macro wrapper TraceLogging](tracelogging-wrapper-macros.md).</span><span class="sxs-lookup"><span data-stu-id="48974-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="48974-139">Se si usa C++, è possibile usare la `TraceLoggingValue` macro wrapper per dedurre automaticamente il tipo dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="48974-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="48974-140">Se si sta scrivendo il driver in C, è necessario utilizzare macro di campo specifiche del tipo, ad esempio `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` e così via. Le macro wrapper TraceLogging sono definite in TraceLoggingProvider. h</span><span class="sxs-lookup"><span data-stu-id="48974-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="48974-141">Oltre alla registrazione di eventi singoli, è anche possibile raggruppare gli eventi in base all'attività usando le macro [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) o [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) disponibili in TraceLoggingActivity. h.</span><span class="sxs-lookup"><span data-stu-id="48974-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="48974-142">Le attività correlano gli eventi e sono utili per gli scenari che hanno un inizio e una fine.</span><span class="sxs-lookup"><span data-stu-id="48974-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="48974-143">Ad esempio, è possibile usare un'attività per misurare uno scenario che inizia con l'avvio di un'applicazione, include il tempo necessario per la visualizzazione della schermata iniziale e termina quando viene visualizzata la schermata iniziale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48974-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="48974-144">Le attività acquisiscono singoli eventi e annidano altre attività che si verificano tra l'inizio e la fine di tale attività.</span><span class="sxs-lookup"><span data-stu-id="48974-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="48974-145">Le attività hanno un ambito per processo e devono essere passate da un thread a un thread per annidare correttamente gli eventi multithread.</span><span class="sxs-lookup"><span data-stu-id="48974-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="48974-146">L'ambito di un handle del provider è limitato esclusivamente al modulo (file DLL, EXE o SYS) in cui è definito. l'handle non deve essere passato ad altre dll.</span><span class="sxs-lookup"><span data-stu-id="48974-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="48974-147">Se una macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) viene richiamata in A.DLL usando un handle del provider definito in B.DLL, potrebbe causare problemi.</span><span class="sxs-lookup"><span data-stu-id="48974-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="48974-148">Il modo più sicuro ed efficiente per soddisfare questo requisito consiste nel fare sempre riferimento direttamente all'handle del provider globale senza mai passare l'handle del provider come parametro.</span><span class="sxs-lookup"><span data-stu-id="48974-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="48974-149">Annulla registrazione del provider</span><span class="sxs-lookup"><span data-stu-id="48974-149">Unregister the provider</span></span>

<span data-ttu-id="48974-150">Al termine della registrazione degli eventi è necessario annullare la registrazione del provider TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="48974-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="48974-151">Il codice seguente annulla la registrazione del provider.</span><span class="sxs-lookup"><span data-stu-id="48974-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="48974-152">Compatibilità</span><span class="sxs-lookup"><span data-stu-id="48974-152">Compatibility</span></span>

<span data-ttu-id="48974-153">A seconda della configurazione, TraceLoggingProvider. h può essere compatibile con le versioni precedenti (compatibile con Windows Vista o versione successiva) oppure può essere ottimizzato per versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48974-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="48974-154">TraceLoggingProvider. h USA WINVER (modalità utente) e NTDDI_VERSION (modalità kernel) per determinare se deve essere compatibile con le versioni precedenti del sistema operativo o essere ottimizzato per le versioni più recenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48974-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="48974-155">Per la modalità utente, se si include <> Windows. h prima di impostare WINVER, <Windows. h> imposta WINVER sulla versione del sistema operativo di destinazione predefinita dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="48974-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="48974-156">Se WINVER è impostato su 0x602 o su un valore superiore, TraceLoggingProvider. h ne ottimizza il comportamento per Windows 8. l'app non verrà eseguita nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="48974-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="48974-157">Se è necessario eseguire il programma in vista o Windows 7, assicurarsi di impostare WINVER sul valore appropriato prima di includere <> Windows. h.</span><span class="sxs-lookup"><span data-stu-id="48974-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="48974-158">Analogamente, se si include <WDM. h> prima di impostare NTDDI_VERSION, <WDM. h> imposta NTDDI_VERSION su un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="48974-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="48974-159">Se NTDDI_VERSION è impostato su 0x06040000 o su un valore superiore, TraceLoggingProvider. h ne ottimizza il comportamento per Windows 10 (il driver non funzionerà nelle versioni precedenti di Windows).</span><span class="sxs-lookup"><span data-stu-id="48974-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="48974-160">Riepilogo e passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="48974-160">Summary and next steps</span></span>

<span data-ttu-id="48974-161">Per informazioni su come acquisire e visualizzare i dati di TraceLogging usando le versioni interne più recenti di Windows Performance Tools (WPT), vedere [registrare e visualizzare gli eventi di TraceLogging](tracelogging-record-and-display-tracelogging-events.md).</span><span class="sxs-lookup"><span data-stu-id="48974-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="48974-162">Per altri esempi di C++ TraceLogging, vedere [esempi di C/C++ Tracelogging](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="48974-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




