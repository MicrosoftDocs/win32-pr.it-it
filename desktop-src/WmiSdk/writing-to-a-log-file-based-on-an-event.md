---
description: La classe LogFileEventConsumer può scrivere testo predefinito in un file di log quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.
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
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226931"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Scrittura in un file di log in base a un evento

La classe [**LogFileEventConsumer**](logfileeventconsumer.md) può scrivere testo predefinito in un file di log quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.

La procedura di base per l'utilizzo di consumer standard è sempre la stessa ed è disponibile per il [monitoraggio e la risposta a eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

La procedura seguente aggiunge alla procedura di base, è specifica della classe [**LogFileEventConsumer**](logfileeventconsumer.md) e descrive come creare un consumer di eventi che esegue un programma.

**Per creare un consumer di eventi che scrive in un file di log**

1.  Nel file Managed Object Format (MOF) creare un'istanza di [**LogFileEventConsumer**](logfileeventconsumer.md) per ricevere gli eventi richiesti nella query, assegnare un nome all'istanza nella proprietà **Name** e quindi inserire il percorso del file di log nella proprietà **filename** .

    Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

2.  Consente di specificare il modello di testo da scrivere nel file di log nella proprietà Text.

    Per ulteriori informazioni, vedere [utilizzo di modelli di stringa standard](using-standard-string-templates.md).

3.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e definire una query per specificare gli eventi che attiveranno il consumer.

    Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).

4.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**LogFileEventConsumer**](logfileeventconsumer.md).
5.  Per controllare chi legge o scrive nel file di log, impostare la sicurezza per la directory in cui si trova il registro al livello richiesto.
6.  Compilare il file MOF usando [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Esempio

L'esempio in questa sezione è codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md). Nell'esempio viene usato il LogFileEventConsumer standard per creare una classe consumer denominata LogFileEvent che scrive una riga nel file c: \\ logfile. log quando viene creata un'istanza della classe LogFileEvent.

Nella procedura riportata di seguito viene descritto come utilizzare l'esempio.

**Per usare l'esempio**

1.  Copiare il file MOF riportato di seguito in un file di testo e salvarlo con estensione MOF.
2.  In una finestra di comando compilare il file MOF usando il comando seguente.

    **Mofcomp** *nomefile * * *. mof**

3.  Aprire logfile. log per visualizzare la riga specificata da LogFileEvent.Name: "evento del consumer di eventi di logfile".

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

 

 



