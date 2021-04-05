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
# <a name="tracelogging-cc-quick-start"></a>Avvio rapido C/C++ TraceLogging

Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice nativo in modalità utente.

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10
-   Microsoft Visual Studio 2013
-   Il Software Development Kit (SDK) di Windows 10 è necessario per scrivere un provider in modalità utente
-   Windows Driver Kit (WDK) per Windows 10 è necessario per scrivere un provider in modalità kernel

> [!IMPORTANT]
> Per compilare questi esempi, collegare Advapi32. lib.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample. h

Questa intestazione di esempio include le API TraceLogging e in diretta dichiara l'handle del provider che verrà usato per registrare gli eventi. Tutte le classi che desiderano utilizzare TraceLogging includono questa intestazione e possono quindi avviare la registrazione.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

Il file di intestazione include TraceLoggingProvider. h, che definisce l'API TraceLogging nativa. È necessario includere innanzitutto Windows. h perché definisce le costanti utilizzate da TraceLoggingProvider. h.

Il file di intestazione dichiara l'handle del provider `g_hMyComponentProvider` che passerà alle API TraceLogging per registrare gli eventi. Questo handle deve essere accessibile a qualsiasi codice che desideri usare TraceLogging.

[**TRACELOGGING \_ DECLARE \_ provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) è una macro che crea un `extern const TraceLoggingHProvider` handle usando il nome fornito, che nell'esempio precedente è `g_hMyComponentProvider` . La variabile di handle del provider effettiva viene allocata in un file di codice.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample. cpp

Nell'esempio seguente viene registrato il provider, viene registrato un evento e viene annullata la registrazione del provider.

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

Nell'esempio precedente è incluso SimpleTraceLoggingExample. h che contiene la variabile globale del provider che il codice utilizzerà per registrare gli eventi.

La macro del [**\_ \_ provider TRACELOGGING define**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) alloca l'archiviazione e definisce la variabile dell'handle del provider. Il nome della variabile fornito a questa macro deve corrispondere al nome usato nella macro del [**provider di \_ Dichiarazione \_ TRACELOGGING**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) nel file di intestazione. Questo handle rimarrà valido fino a quando si trova nell'ambito.

### <a name="register-the-provider-handle"></a>Registrare l'handle del provider

Prima di poter usare l'handle del provider per registrare gli eventi, è necessario chiamare [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) per registrare l'handle del provider. Questa operazione viene in genere eseguita in Main () o DLLMain (), ma può essere eseguita in qualsiasi momento, purché preceda qualsiasi tentativo di registrare un evento. Se si registra un evento prima della registrazione dell'handle del provider, non si verificherà alcun errore, ma l'evento non verrà registrato. Il codice seguente riportato nell'esempio precedente registra l'handle del provider.

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

### <a name="log-a-tracelogging-event"></a>Registra un evento Tracelogging

Dopo che il provider è stato registrato, il codice seguente registra un evento semplice.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) richiede fino a 99 argomenti e viene eseguita come diverse istruzioni. Ciò significa che i valori registrati non devono essere oggetti temporanei C++. Il nome dell'evento viene archiviato in formato UTF-8. Non è necessario usare caratteri incorporati `null` nell'evento o in altri nomi di campo. Non sono previsti altri limiti per i caratteri consentiti.

Ogni argomento che segue il nome dell'evento deve essere incapsulato all'interno di una [macro wrapper TraceLogging](tracelogging-wrapper-macros.md). Se si usa C++, è possibile usare la `TraceLoggingValue` macro wrapper per dedurre automaticamente il tipo dell'argomento. Se si sta scrivendo il driver in C, è necessario utilizzare macro di campo specifiche del tipo, ad esempio `TraceLoggingInt32` ,, `TraceLoggingUnicodeString` `TraceLoggingString` e così via. Le macro wrapper TraceLogging sono definite in TraceLoggingProvider. h

Oltre alla registrazione di eventi singoli, è anche possibile raggruppare gli eventi in base all'attività usando le macro [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) o [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) disponibili in TraceLoggingActivity. h. Le attività correlano gli eventi e sono utili per gli scenari che hanno un inizio e una fine. Ad esempio, è possibile usare un'attività per misurare uno scenario che inizia con l'avvio di un'applicazione, include il tempo necessario per la visualizzazione della schermata iniziale e termina quando viene visualizzata la schermata iniziale dell'applicazione.

Le attività acquisiscono singoli eventi e annidano altre attività che si verificano tra l'inizio e la fine di tale attività. Le attività hanno un ambito per processo e devono essere passate da un thread a un thread per annidare correttamente gli eventi multithread.

L'ambito di un handle del provider è limitato esclusivamente al modulo (file DLL, EXE o SYS) in cui è definito. l'handle non deve essere passato ad altre dll. Se una macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) viene richiamata in A.DLL usando un handle del provider definito in B.DLL, potrebbe causare problemi. Il modo più sicuro ed efficiente per soddisfare questo requisito consiste nel fare sempre riferimento direttamente all'handle del provider globale senza mai passare l'handle del provider come parametro.

### <a name="unregister-the-provider"></a>Annulla registrazione del provider

Al termine della registrazione degli eventi è necessario annullare la registrazione del provider TraceLogging. Il codice seguente annulla la registrazione del provider.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilità

A seconda della configurazione, TraceLoggingProvider. h può essere compatibile con le versioni precedenti (compatibile con Windows Vista o versione successiva) oppure può essere ottimizzato per versioni successive del sistema operativo. TraceLoggingProvider. h USA WINVER (modalità utente) e NTDDI_VERSION (modalità kernel) per determinare se deve essere compatibile con le versioni precedenti del sistema operativo o essere ottimizzato per le versioni più recenti del sistema operativo.

Per la modalità utente, se si include <> Windows. h prima di impostare WINVER, <Windows. h> imposta WINVER sulla versione del sistema operativo di destinazione predefinita dell'SDK. Se WINVER è impostato su 0x602 o su un valore superiore, TraceLoggingProvider. h ne ottimizza il comportamento per Windows 8. l'app non verrà eseguita nelle versioni precedenti di Windows. Se è necessario eseguire il programma in vista o Windows 7, assicurarsi di impostare WINVER sul valore appropriato prima di includere <> Windows. h.

Analogamente, se si include <WDM. h> prima di impostare NTDDI_VERSION, <WDM. h> imposta NTDDI_VERSION su un valore predefinito. Se NTDDI_VERSION è impostato su 0x06040000 o su un valore superiore, TraceLoggingProvider. h ne ottimizza il comportamento per Windows 10 (il driver non funzionerà nelle versioni precedenti di Windows).

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Per informazioni su come acquisire e visualizzare i dati di TraceLogging usando le versioni interne più recenti di Windows Performance Tools (WPT), vedere [registrare e visualizzare gli eventi di TraceLogging](tracelogging-record-and-display-tracelogging-events.md).

Per altri esempi di C++ TraceLogging, vedere [esempi di C/C++ Tracelogging](tracelogging-c-cpp-tracelogging-examples.md) .

 

 




