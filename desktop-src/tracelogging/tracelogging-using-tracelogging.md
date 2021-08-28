---
title: Uso di TraceLogging
description: Negli argomenti seguenti viene fornito un avvio rapido di TraceLogging per il codice nativo e gestito, con esempi.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be48ff03e1efe37b2ed18314557514c81715ea7e36dacfda309f473522dac39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966490"
---
# <a name="using-tracelogging"></a>Uso di TraceLogging

Negli argomenti seguenti viene fornito un avvio rapido di TraceLogging per il codice nativo e gestito, con esempi.

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10 Software Development Kit (SDK) è necessario per scrivere un provider in modalità utente
-   Windows Driver Kit (WDK) è necessario per scrivere un provider in modalità kernel

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++ Avvio rapido](tracelogging-native-quick-start.md)<br/>                             | La sezione seguente descrive i passaggi di base necessari per aggiungere TraceLogging al codice in modalità utente nativa. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [TraceLogging Managed Avvio rapido](tracelogging-managed-quick-start.md)<br/>                          | La sezione seguente descrive i passaggi di base necessari per aggiungere TraceLogging al codice gestito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Registrare e visualizzare eventi TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con il Windows analizzatore prestazioni (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Esempi di traccia C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Questo argomento contiene esempi di tracelogging C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Esempi di tracelogging .NET](tracelogging-net-examples.md)<br/>                                       | Questo argomento contiene un esempio di tracelogging del codice gestito che illustra come registrare un evento solo quando il livello di dettaglio della sessione è dettagliato e come registrare i dati degli eventi strutturati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Esempio di registrazione della Windows Universal Windows Platform](universal-windows-platform-logging-examples.md)<br/>     | Questo esempio illustra come usare le API di registrazione nel Windows. Spazio dei nomi Foundation.Diagnostics, tra cui LoggingChannel, LoggingActivity, LoggingSession e FileLoggingSession. Queste classi sono progettate per la registrazione diagnostica all'interno di un Windows app. Queste API sono state aggiunte in Windows 8.1. <br/> Le API LoggingChannel e LoggingActivity sono state estese in Windows 10 per supportare la scrittura di eventi complessi usando la codifica degli eventi TraceLogging.<br/> L'esempio di registrazione di Universal Windows Platform può essere scaricato [da GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Esempi di TraceLogging.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TraceLogging per driver e componenti in modalità kernel](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

