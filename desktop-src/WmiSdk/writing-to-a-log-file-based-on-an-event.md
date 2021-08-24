---
description: La classe LogFileEventConsumer può scrivere testo predefinito in un file di log quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Scrittura in un file di log in base a un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 881435986a1097c2ba97160693ed15e28bae3d86019fb703adf6bf1e8b07f8a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049729"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Scrittura in un file di log in base a un evento

La [**classe LogFileEventConsumer**](logfileeventconsumer.md) può scrivere testo predefinito in un file di log quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.

La procedura di base per l'uso di consumer standard è sempre la stessa e si trova in Monitoraggio e risposta [agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

La procedura seguente aggiunge alla procedura di base, è specifica della classe [**LogFileEventConsumer**](logfileeventconsumer.md) e descrive come creare un consumer di eventi che esegue un programma.

**Per creare un consumer di eventi che scrive in un file di log**

1.  Nel file Managed Object Format (MOF) creare un'istanza di [**LogFileEventConsumer**](logfileeventconsumer.md) per ricevere gli eventi che si richiedono nella query, assegnare un nome all'istanza nella proprietà **Name** e quindi inserire il percorso del file di log nella proprietà **Filename.**

    Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

2.  Specificare il modello di testo da scrivere nel file di log nella proprietà Text.

    Per altre informazioni, vedere [Uso di modelli di stringa standard.](using-standard-string-templates.md)

3.  Creare un'istanza [**\_ \_ di EventFilter**](--eventfilter.md) e definire una query per specificare gli eventi che attiveranno il consumer.

    Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md)

4.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**LogFileEventConsumer**](logfileeventconsumer.md).
5.  Per controllare chi legge o scrive nel file di log, impostare la sicurezza nella directory in cui si trova il log sul livello richiesto.
6.  Compilare il file MOF [**usandoMofcomp.exe**](mofcomp.md).

## <a name="example"></a>Esempio

L'esempio riportato in questa sezione è in codice MOF, ma è possibile creare le istanze a livello di codice usando [l'API di](scripting-api-for-wmi.md) scripting per WMI o l'API COM [per WMI.](com-api-for-wmi.md) L'esempio usa lo standard LogFileEventConsumer per creare una classe consumer denominata LogFileEvent che scrive una riga nel file c: Logfile.log quando viene creata un'istanza della classe \\ LogFileEvent.

Nella procedura seguente viene descritto come utilizzare l'esempio.

**Per usare l'esempio**

1.  Copiare l'elenco MOF seguente in un file di testo e salvarlo con estensione mof.
2.  In una finestra di comando compilare il file MOF usando il comando seguente.

    **Nome file Mofcomp***.mof** *

3.  Aprire Logfile.log per visualizzare la riga specificata da LogFileEvent.Name: "Logfile Event Consumer event".

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



