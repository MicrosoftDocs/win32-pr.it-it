---
description: La classe NTEventLogEventConsumer scrive un messaggio nel registro eventi di Windows quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Registrazione nel registro eventi NT in base a un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bf24c0d64c95a012b8681b88bde34dc28fa179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883517"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Registrazione nel registro eventi NT in base a un evento

La classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) scrive un messaggio nel registro eventi di Windows quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.

> [!Note]  
> Per impostazione predefinita, gli utenti autenticati non possono registrare gli eventi nel registro applicazioni in un computer remoto. Di conseguenza, l'esempio descritto in questo argomento avrà esito negativo se si usa la proprietà **UNCServerName** della classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) e si specifica un computer remoto come valore. Per informazioni su come modificare la sicurezza del registro eventi, vedere l' [articolo della Knowledge Knowledge](https://support.microsoft.com/kb/323076).

 

La procedura di base per l'uso di un consumer standard è descritta in [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). Di seguito sono riportati passaggi aggiuntivi oltre alla procedura di base, necessari quando si usa la classe [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) . Nei passaggi viene descritto come creare un consumer di eventi che scrive nel registro eventi dell'applicazione.

Nella procedura seguente viene descritto come creare un consumer di eventi che scrive nel registro eventi NT.

**Per creare un consumer di eventi che scrive nel registro eventi di Windows**

1.  In un file di Managed Object Format (MOF) creare un'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) per ricevere gli eventi richiesti nella query. Per ulteriori informazioni sulla scrittura di codice MOF, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).
2.  Creare, e Name, un'istanza di [**\_ \_ EventFilter**](--eventfilter.md)e quindi creare una query per specificare il tipo di evento che attiva la scrittura nel registro eventi NT.

    Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).

3.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).
4.  Compilare il file MOF utilizzando [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Esempio

L'esempio in questa sezione è codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md). Nell'esempio viene illustrato come creare un consumer per scrivere nel registro eventi dell'applicazione utilizzando [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). Il file MOF crea una nuova classe denominata "NTLogCons \_ example", un filtro eventi per eseguire una query per le operazioni, ad esempio la creazione, in un'istanza di questa nuova classe e un'associazione tra filtro e consumer. Poiché l'ultima azione nel file MOF consiste nel creare un'istanza dell' \_ esempio NTLogCons, è possibile visualizzare immediatamente l'evento nel registro eventi dell'applicazione eseguendo Eventvwr.exe.

`EventID=0x0A for SourceName="WinMgmt"`Identifica un messaggio con il testo seguente. "%1", "%2", "%3" sono segnaposto per le stringhe corrispondenti specificate nella matrice InsertionStringTemplates.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

Nella procedura riportata di seguito viene descritto come utilizzare l'esempio.

**Per usare l'esempio**

1.  Copiare il file MOF riportato di seguito in un file di testo e salvarlo con estensione MOF.
2.  In una finestra di comando compilare il file MOF usando il comando seguente:

    **Mofcomp** *nomefile * * *. mof**

3.  Eseguire Eventvwr.exe. Esaminare il registro eventi dell'applicazione. Verrà visualizzato un evento con ID = 10 ( **eventId**), Source = "WMI" e Type = Error.
4.  Fare doppio clic sul messaggio del **tipo di informazioni** da WMI con 10 nella colonna **evento** . Verrà visualizzata la seguente descrizione per l'evento.

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



