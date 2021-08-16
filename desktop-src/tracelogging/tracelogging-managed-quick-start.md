---
title: Codice gestito TraceLogging Avvio rapido
description: La sezione seguente descrive i passaggi di base necessari per aggiungere TraceLogging al codice gestito.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be29e4a1bd6721b8f53dbe2394be3552ca4845143cf948f130ef55e11881b518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589241"
---
# <a name="tracelogging-managed-quick-start"></a>Codice gestito TraceLogging Avvio rapido

La sezione seguente descrive i passaggi di base necessari per aggiungere TraceLogging al codice gestito.

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample.cs

In questo esempio viene illustrato come registrare eventi Tracelogging senza la necessità di creare manualmente un file XML del manifesto della strumentazione separato.


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a>Creare EventSource

Prima di poter registrare gli eventi, è necessario creare un'istanza della classe EventSource. Il primo parametro del costruttore identifica il nome di questo provider. Il provider viene registrato automaticamente come illustrato nell'esempio.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



L'istanza è statica perché nell'applicazione deve essere presente una sola istanza di un provider specifico alla volta.

### <a name="log-tracelogging-events"></a>Registrare eventi Tracelogging

Dopo aver creato il provider, il codice seguente dell'esempio precedente registra un evento semplice.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Registrare i dati di payload degli eventi strutturati

È possibile definire dati di payload strutturati registrati con l'evento . Fornire dati di payload strutturati come tipo anonimo o come istanza di una classe annotata con l'attributo , come `[EventData]` illustrato nell'esempio seguente.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



È necessario aggiungere `[EventData]` l'attributo alle classi di payload degli eventi definite come illustrato di seguito.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



L'attributo sostituisce la necessità di creare manualmente un file manifesto per descrivere i dati dell'evento. A questo punto è necessario passare un'istanza della classe al metodo EventSource.Write() per registrare l'evento e i dati di payload corrispondenti.

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Vedere [Registrare e visualizzare eventi TraceLogging](tracelogging-record-and-display-tracelogging-events.md) per informazioni su come acquisire e visualizzare i dati TraceLogging usando le versioni interne più recenti di Windows Performance Tools (WPT).

Per altri esempi di TraceLogging gestiti, vedere Esempi di [tracelogging .NET.](tracelogging-net-examples.md)

 

 




