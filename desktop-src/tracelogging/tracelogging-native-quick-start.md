---
title: TraceLogging C/C++ Avvio rapido
description: La sezione seguente descrive i passaggi di base necessari per aggiungere TraceLogging al codice in modalità utente nativa.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: cb3734e3f314270e3d8082f5c9d25d38ce065829b94c659023950e5e2709047b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966500"
---
# <a name="tracelogging-cc-quick-start"></a>TraceLogging C/C++ Avvio rapido

La sezione seguente descrive i passaggi di base necessari per aggiungere TraceLogging al codice in modalità utente nativa.

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10
-   Microsoft Visual Studio 2013
-   Windows 10 Software Development Kit (SDK) è necessario per scrivere un provider in modalità utente
-   Windows Driver Kit (WDK) per Windows 10 per scrivere un provider in modalità kernel

> [!IMPORTANT]
> Collegare advapi32.lib per compilare questi esempi.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample.h

Questa intestazione di esempio include le API TraceLogging e dichiara in avanti l'handle del provider che verrà usato per registrare gli eventi. Qualsiasi classe che voglia usare TraceLogging includerà questa intestazione e potrà quindi avviare la registrazione.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

Il file di intestazione include TraceLoggingProvider.h che definisce l'API TraceLogging nativa. È necessario includere Windows.h perché definisce le costanti usate da TraceLoggingProvider.h.

Il file di intestazione dichiara l'handle del provider che verrà passato alle API `g_hMyComponentProvider` TraceLogging per registrare gli eventi. Questo handle deve essere accessibile a qualsiasi codice che vuole usare TraceLogging.

[**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) è una macro che crea un handle usando il nome `extern const TraceLoggingHProvider` specificato, che nell'esempio precedente è `g_hMyComponentProvider` . La variabile di handle del provider effettiva verrà allocata in un file di codice.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample.cpp

L'esempio seguente registra il provider, registra un evento e annulla la registrazione del provider.

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

L'esempio precedente include SimpleTraceLoggingExample.h che contiene la variabile del provider globale che verrà utilizzata dal codice per registrare gli eventi.

La macro [**TRACELOGGING \_ DEFINE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) alloca l'archiviazione e definisce la variabile di handle del provider. Il nome della variabile fornito a questa macro deve corrispondere al nome usato nella macro [**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) nel file di intestazione. Questo handle rimarrà valido fino a quando si trova nell'ambito.

### <a name="register-the-provider-handle"></a>Registrare l'handle del provider

Prima di poter usare l'handle del provider per registrare gli eventi, è necessario chiamare [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) per registrare l'handle del provider. Questa operazione viene in genere eseguita in Main() o DLLMain(), ma può essere eseguita in qualsiasi momento, purché preceda qualsiasi tentativo di registrare un evento. Se si registra un evento prima di registrare l'handle del provider, non si verificherà alcun errore, ma l'evento non verrà registrato. Il codice seguente dell'esempio precedente registra l'handle del provider.

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

### <a name="log-a-tracelogging-event"></a>Registrare un evento tracelogging

Dopo la registrazione del provider, il codice seguente registra un evento semplice.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) accetta fino a 99 argomenti ed esegue come diverse istruzioni. Ciò significa che i valori registrati non devono essere oggetti temporanei C++. Il nome dell'evento viene archiviato in formato UTF-8. Non è necessario usare caratteri `null` incorporati nell'evento o in altri nomi di campo. Non sono previsti altri limiti per i caratteri consentiti.

Ogni argomento che segue il nome dell'evento deve essere racchiuso all'interno di una [macro wrapper TraceLogging](tracelogging-wrapper-macros.md). Se si usa C++, è possibile usare la macro wrapper per `TraceLoggingValue` dedurre automaticamente il tipo dell'argomento. Se si scrive il driver in C, è necessario usare macro di campo specifiche del tipo, ad esempio `TraceLoggingInt32` , , e così `TraceLoggingUnicodeString` `TraceLoggingString` via. Le macro del wrapper TraceLogging sono definite in TraceLoggingProvider.h

Oltre a registrare singoli eventi, è anche possibile raggruppare gli eventi in base all'attività usando le macro [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) o [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) disponibili in TraceLoggingActivity.h. Le attività correlano gli eventi e sono utili per gli scenari che hanno un inizio e una fine. Ad esempio, è possibile usare un'attività per misurare uno scenario che inizia con l'avvio di un'applicazione, include il tempo necessario per la schermata iniziale diventa disponibile e termina quando la schermata iniziale dell'applicazione diventa visibile.

Le attività acquisiscono singoli eventi e annidare altre attività che si verificano tra l'inizio e la fine di tale attività. Le attività hanno un ambito per processo e devono essere passate da thread a thread per annidare correttamente gli eventi multi-thread.

L'ambito di un handle del provider è limitato esclusivamente al modulo (file DLL, EXE o SYS) in cui è definito. L'handle non deve essere passato ad altre DLL. Se una macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) viene richiamata in A.DLL usando un handle del provider definito in B.DLL, potrebbero verificarsi problemi. Il modo più sicuro ed efficiente per soddisfare questo requisito è fare sempre riferimento direttamente all'handle del provider globale e non passare mai l'handle del provider come parametro.

### <a name="unregister-the-provider"></a>Annullare la registrazione del provider

Al termine della registrazione degli eventi, è necessario annullare la registrazione del provider TraceLogging. Il codice seguente annulla la registrazione del provider.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilità

A seconda della configurazione, TraceLoggingProvider.h può essere compatibile con le versioni precedenti (compatibile con Windows Vista o versioni successive) o può essere ottimizzato per le versioni successive del sistema operativo. TraceLoggingProvider.h usa WINVER (modalità utente) e NTDDI_VERSION (modalità kernel) per determinare se deve essere compatibile con le versioni precedenti del sistema operativo o essere ottimizzato per le versioni più recenti del sistema operativo.

Per la modalità utente, se si include <windows.h> prima di impostare WINVER, <windows.h> imposta WINVER sulla versione del sistema operativo di destinazione predefinita dell'SDK. Se WINVER è impostato su 0x602 o versione successiva, TraceLoggingProvider.h ottimizza il comportamento per Windows 8 (l'app non verrà eseguita nelle versioni precedenti di Windows). Se è necessario che il programma venga eseguito in Vista o Windows 7, assicurarsi di impostare WINVER sul valore appropriato prima di includere <windows.h>.

Analogamente, se si include <> wdm.h prima di impostare NTDDI_VERSION, <wdm.h> imposta NTDDI_VERSION su un valore predefinito. Se NTDDI_VERSION è impostato su 0x06040000 o versione successiva, TraceLoggingProvider.h ottimizza il comportamento per Windows 10 (il driver non funzionerà nelle versioni precedenti di Windows).

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Per informazioni su come acquisire e visualizzare i dati di TraceLogging usando le versioni interne più recenti di Windows Performance Tools (WPT), vedere Registrare e visualizzare [eventi TraceLogging](tracelogging-record-and-display-tracelogging-events.md).

Per altri [esempi di TraceLogging C++,](tracelogging-c-cpp-tracelogging-examples.md) vedere Esempi di traccia C/C++.

 

 




