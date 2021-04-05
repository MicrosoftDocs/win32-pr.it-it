---
description: È possibile utilizzare le classi consumer standard installate per eseguire azioni in base agli eventi in un sistema operativo.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Monitoraggio e risposta agli eventi con consumer standard
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5bd1d329cd861fa45c99851707177322d0b9d12f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103886338"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Monitoraggio e risposta agli eventi con consumer standard

È possibile utilizzare le [classi consumer standard](standard-consumer-classes.md) installate per eseguire azioni in base agli eventi in un sistema operativo. I consumer standard sono classi semplici già registrate e definiscono classi consumer permanenti. Ogni consumer standard esegue un'azione specifica dopo la ricezione di una notifica degli eventi. Ad esempio, è possibile definire un'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per eseguire uno script quando lo spazio libero su disco in un computer è diverso da una dimensione specificata.

WMI compila gli utenti standard in spazi dei nomi predefiniti che dipendono dal sistema operativo, ad esempio:

-   In Windows Server 2003, tutti gli utenti standard vengono compilati per impostazione predefinita nello \\ spazio dei nomi "sottoscrizione radice".

> [!Note]  
> Per gli spazi dei nomi e i sistemi operativi predefiniti specifici per ogni classe WMI, vedere le sezioni osservazioni e requisiti di ogni argomento della classe.

 

Nella tabella seguente sono elencati e descritti i consumer standard WMI.



| Consumer standard                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | Esegue uno script quando riceve una notifica degli eventi. Per ulteriori informazioni, vedere [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md).                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | Scrive stringhe personalizzate in un file di log di testo quando riceve una notifica degli eventi. Per ulteriori informazioni, vedere [scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md).                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | Registra un messaggio specifico nel registro eventi dell'applicazione. Per ulteriori informazioni, vedere [registrazione nel registro eventi NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md).                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | Invia un messaggio di posta elettronica tramite SMTP ogni volta che viene recapitato un evento. Per ulteriori informazioni, vedere [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md).                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | Avvia un processo quando un evento viene recapitato a un sistema locale. Il file eseguibile deve trovarsi in un percorso sicuro o protetto con un elenco di controllo di accesso (ACL) sicuro per impedire a un utente non autorizzato di sostituire l'eseguibile con un altro eseguibile. Per ulteriori informazioni, vedere [esecuzione di un programma dalla riga di comando in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md). |



 

Nella procedura seguente viene descritto come monitorare e rispondere agli eventi utilizzando un consumer standard. Si noti che la procedura è identica per un file, uno script o un'applicazione di Managed Object Format (MOF).

**Per monitorare e rispondere agli eventi con un consumer standard**

1.  Specificare lo spazio dei nomi in un file MOF utilizzando lo [ \# spazio dei nomi pragma](pragma-namespace.md)del comando per il preprocessore MOF. In uno script o un'applicazione specificare lo spazio dei nomi nel codice che si connette a WMI.

    Nell'esempio di codice MOF seguente viene illustrato come specificare lo \\ spazio dei nomi della sottoscrizione radice.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    La maggior parte [*degli eventi intrinseci*](gloss-i.md) è associata a modifiche alle istanze di classe nello \\ spazio dei nomi CIMV2 radice. Tuttavia, gli eventi del registro di sistema, ad esempio [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) , vengono generati nello \\ spazio dei nomi predefinito radice dal [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

    Un consumer può includere classi di evento situate in altri spazi dei nomi specificando lo spazio dei nomi nella proprietà **EventNamespace** nella query [**\_ \_ EventFilter**](--eventfilter.md) per gli eventi. Le classi [*degli eventi intrinseci*](gloss-i.md) , ad esempio [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , sono disponibili in ogni spazio dei nomi.

2.  Creare e popolare un'istanza di una classe consumer standard.

    Questa istanza può avere un valore univoco nella proprietà **Name** . È possibile aggiornare un consumer esistente riutilizzando lo stesso nome.

    **InsertionStringTemplates** contiene il testo da inserire in un evento specificato in **eventType**. È possibile usare stringhe letterali o fare riferimento direttamente a una proprietà. Per ulteriori informazioni, vedere [utilizzo di modelli di stringa standard](using-standard-string-templates.md) e [istruzione SELECT per le query di eventi](select-statement-for-event-queries.md).

    Utilizzare un'origine esistente per il registro eventi che supporti una stringa di inserimento senza testo associato.

    Nell'esempio di codice MOF seguente viene illustrato come utilizzare un'origine esistente di WSH e un valore **eventId** pari a 8.

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e definire una query per gli eventi.

    Nell'esempio seguente il filtro monitora la chiave del registro di sistema in cui sono registrati i programmi di avvio. Il monitoraggio di questa chiave del registro di sistema può essere importante perché un programma non autorizzato è in grado di registrarsi nella chiave, che ne determina l'avvio all'avvio del computer.

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  Identificazione di un evento per il monitoraggio e la creazione di una query di eventi.

    È possibile verificare se esiste un evento intrinseco o estrinseco che usa. Utilizzare, ad esempio, la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del provider del registro di sistema per monitorare le modifiche apportate al registro di sistema.

    Se non esiste una classe che descrive un evento che è necessario monitorare, è necessario creare un provider di eventi personalizzato e definire nuove classi di evento estrinseche. Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).

    In un file MOF è possibile definire un [*alias*](gloss-a.md) per il filtro e il consumer, che fornisce un modo semplice per descrivere i percorsi dell'istanza.

    Nell'esempio seguente viene illustrato come definire un [*alias*](gloss-a.md) per il filtro e il consumer.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro e le classi consumer. Questa istanza determina che quando si verifica un evento che corrisponde al filtro specificato, è necessario che venga eseguita l'azione specificata dal consumer. [**\_ \_ EventFilter**](--eventfilter.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e **\_ \_ FilterToConsumerBinding** devono avere lo stesso ID di sicurezza (SID) singolo nella proprietà **CreatorSID** . Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).

    Nell'esempio seguente viene illustrato come identificare un'istanza tramite il percorso dell'oggetto o come utilizzare un alias come espressione a sintassi abbreviata per il percorso dell'oggetto.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    Nell'esempio seguente il filtro viene associato al consumer tramite alias.

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    È possibile associare un filtro a diversi consumer, a indicare che quando si verificano eventi corrispondenti, è necessario eseguire diverse azioni. in alternativa, è possibile associare un consumer a diversi filtri, a indicare che l'azione deve essere eseguita quando si verificano eventi che corrispondono a uno dei filtri.

    Le azioni seguenti vengono eseguite in base alla condizione di consumer ed eventi:

    -   Se uno dei consumer permanenti ha esito negativo, altri utenti che richiedono l'evento ricevono la notifica.
    -   Se viene eliminato un evento, WMI genera [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).
    -   Se si sottoscrive questo evento, viene restituito l'evento che viene eliminato e un riferimento a [**\_ \_ EventConsumer**](--eventconsumer.md) rappresenta l'utente che ha avuto esito negativo.
    -   Se un consumer ha esito negativo, WMI genera [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), che può contenere altre informazioni nelle proprietà **ErrorCode**, **ErrorDescription** e **ErrorObject** .

    Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato il file MOF per un'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). Dopo la compilazione di questo MOF, qualsiasi tentativo di creare, eliminare o modificare un valore nel percorso del registro di sistema **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run** registra una voce nel log eventi dell'applicazione, sotto l'origine "WSH".


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricezione di eventi in modo sicuro](receiving-events-securely.md)
</dt> </dl>

 

 
