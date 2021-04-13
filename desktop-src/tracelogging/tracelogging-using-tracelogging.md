---
title: Uso di TraceLogging
description: Gli argomenti seguenti forniscono una guida introduttiva a TraceLogging per il codice nativo e gestito, con esempi.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e331f5ebec3d7eb8ce9c50d3e9d92f747bf76414
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399645"
---
# <a name="using-tracelogging"></a>Uso di TraceLogging

Gli argomenti seguenti forniscono una guida introduttiva a TraceLogging per il codice nativo e gestito, con esempi.

## <a name="prerequisites"></a>Prerequisiti

-   Il Software Development Kit (SDK) di Windows 10 è necessario per scrivere un provider in modalità utente
-   Per scrivere un provider in modalità kernel, è necessario Windows Driver Kit (WDK)

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Avvio rapido C/C++ TraceLogging](tracelogging-native-quick-start.md)<br/>                             | Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice nativo in modalità utente. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Avvio rapido gestiti TraceLogging](tracelogging-managed-quick-start.md)<br/>                          | Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice gestito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Registrare e visualizzare gli eventi TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | Registrare gli eventi TraceLogging con Windows Performance Recorder (WPR) e visualizzarli con Windows Performance Analyzer (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Esempi di Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Questo argomento contiene esempi di Tracelogging in C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Esempi di .NET Tracelogging](tracelogging-net-examples.md)<br/>                                       | Questo argomento contiene un esempio di codice gestito Tracelogging che illustra come registrare un evento solo quando il livello di dettaglio della sessione è dettagliato e come registrare i dati degli eventi strutturati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Esempio di registrazione piattaforma UWP (Universal Windows Platform)](universal-windows-platform-logging-examples.md)<br/>     | Questo esempio illustra come usare le API di registrazione nello spazio dei nomi Windows. Foundation. Diagnostics, tra cui LoggingChannel, LoggingActivity, LoggingSession e FileLoggingSession. Queste classi sono progettate per la registrazione diagnostica in un'app di Windows. Queste API sono state aggiunte in Windows 8.1. <br/> Le API LoggingChannel e LoggingActivity sono state estese in Windows 10 per supportare la scrittura di eventi complessi mediante la codifica degli eventi TraceLogging.<br/> L'esempio di registrazione di piattaforma UWP (Universal Windows Platform) può essere scaricato da [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Esempi di TraceLogging.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TraceLogging per componenti e driver in modalità kernel](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

