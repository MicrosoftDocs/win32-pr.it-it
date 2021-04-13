---
title: Avvio rapido gestiti TraceLogging
description: Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice gestito.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329575"
---
# <a name="tracelogging-managed-quick-start"></a>Avvio rapido gestiti TraceLogging

Nella sezione seguente vengono descritti i passaggi di base necessari per aggiungere TraceLogging al codice gestito.

## <a name="prerequisites"></a>Prerequisiti

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample. cs

Questo esempio illustra come registrare gli eventi Tracelogging senza dover creare manualmente un file XML del manifesto di strumentazione separato.


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



### <a name="create-the-eventsource"></a>Creare il EventSource

Prima di poter registrare gli eventi, è necessario creare un'istanza della classe EventSource. Il primo parametro del costruttore identifica il nome del provider. Il provider viene registrato automaticamente come illustrato nell'esempio.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



L'istanza è statica perché nell'applicazione deve essere presente solo un'istanza di un provider specifico alla volta.

### <a name="log-tracelogging-events"></a>Registra eventi Tracelogging

Dopo la creazione del provider, il seguente codice dell'esempio precedente registra un evento semplice.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Registrare i dati del payload dell'evento strutturato

È possibile definire dati di payload strutturati che vengono registrati con l'evento. Fornire dati di payload strutturati come tipo anonimo o come istanza di una classe che è stata annotata con l' `[EventData]` attributo, come illustrato nell'esempio seguente.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



È necessario aggiungere l' `[EventData]` attributo alle classi di payload di eventi definite come illustrato di seguito.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



L'attributo sostituisce la necessità di creare manualmente un file manifesto per descrivere i dati dell'evento. A questo punto, è sufficiente passare un'istanza della classe al Metodo EventSource. Write () per registrare l'evento e i dati di payload corrispondenti.

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Vedere [registrare e visualizzare gli eventi TraceLogging](tracelogging-record-and-display-tracelogging-events.md) per informazioni su come acquisire e visualizzare i dati di TraceLogging usando le versioni interne più recenti di Windows Performance Tools (WPT).

Per esempi più TraceLogging gestiti, vedere [esempi di Tracelogging .NET](tracelogging-net-examples.md) .

 

 




