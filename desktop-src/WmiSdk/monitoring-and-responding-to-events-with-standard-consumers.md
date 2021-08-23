---
description: È possibile usare le classi consumer standard installate per eseguire azioni in base agli eventi in un sistema operativo.
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
ms.openlocfilehash: b0b7e7b1d1e79e64fb1eb83f17f3aa2d118a9eb53b23c19cbdfd624e2c501a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992781"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Monitoraggio e risposta agli eventi con consumer standard

È possibile usare le classi [consumer standard installate](standard-consumer-classes.md) per eseguire azioni in base agli eventi in un sistema operativo. I consumer standard sono classi semplici già registrate e definiscono classi consumer permanenti. Ogni consumer standard eserciterà un'azione specifica dopo la ricezione di una notifica degli eventi. Ad esempio, è possibile definire un'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per eseguire uno script quando lo spazio libero su disco in un computer è diverso da una dimensione specificata.

WMI compila i consumer standard in spazi dei nomi predefiniti che dipendono dal sistema operativo, ad esempio:

-   In Windows Server 2003, tutti i consumer standard vengono compilati per impostazione predefinita nello spazio dei nomi "Sottoscrizione \\ radice".

> [!Note]  
> Per gli spazi dei nomi e i sistemi operativi predefiniti specifici per ogni classe WMI, vedere le sezioni Osservazioni e requisiti di ogni classe.

 

Nella tabella seguente sono elencati e descritti i consumer standard WMI.



| Consumer standard                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | Esegue uno script quando riceve una notifica dell'evento. Per altre informazioni, vedere [Esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md).                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | Scrive stringhe personalizzate in un file di log di testo quando riceve una notifica degli eventi. Per altre informazioni, vedere [Scrittura in un file di log basato su un evento](writing-to-a-log-file-based-on-an-event.md).                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | Registra un messaggio specifico nel registro eventi dell'applicazione. Per altre informazioni, vedere [Registrazione nel registro eventi nt in base a un evento](logging-to-nt-event-log-based-on-an-event.md).                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | Invia un messaggio di posta elettronica tramite SMTP ogni volta che viene recapitato un evento. Per altre informazioni, vedere [Invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md).                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | Avvia un processo quando un evento viene recapitato a un sistema locale. Il file eseguibile deve essere in un percorso sicuro o protetto con un elenco di controllo di accesso sicuro (ACL) per impedire a un utente non autorizzato di sostituire il file eseguibile con un file eseguibile diverso. Per altre informazioni, vedere [Esecuzione di un programma dalla riga di comando basata su un evento](running-a-program-from-the-command-line-based-on-an-event.md). |



 

La procedura seguente descrive come monitorare e rispondere agli eventi usando un consumer standard. Si noti che la procedura è la stessa per un file Managed Object Format (MOF), uno script o un'applicazione.

**Per monitorare e rispondere agli eventi con un consumer standard**

1.  Specificare lo spazio dei nomi in un file MOF usando il comando del preprocessore MOF [ \# pragma namespace](pragma-namespace.md). In uno script o in un'applicazione specificare lo spazio dei nomi nel codice che si connette a WMI.

    Nell'esempio di codice MOF seguente viene illustrato come specificare lo spazio dei nomi della \\ sottoscrizione radice.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    La [*maggior parte degli eventi*](gloss-i.md) intrinseci è associata alle modifiche alle istanze della classe nello spazio dei nomi \\ cimv2 radice. Tuttavia, gli eventi del Registro di sistema, ad esempio [**RegistryKeyChangeEvent,**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) vengono generati nello spazio dei nomi predefinito radice \\ dal provider del Registro di [sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

    Un consumer può includere classi di evento che si trovano in altri spazi dei nomi specificando lo spazio dei nomi nella **proprietà EventNamespace** nella query [**\_ \_ EventFilter**](--eventfilter.md) per gli eventi. Le [*classi di eventi intrinseci,*](gloss-i.md) ad esempio [**\_ \_ InstanceOperationEvent,**](--instanceoperationevent.md) sono disponibili in ogni spazio dei nomi.

2.  Creare e popolare un'istanza di una classe consumer standard.

    Questa istanza può avere un valore univoco nella **proprietà** Name. È possibile aggiornare un consumer esistente riutilizzando lo stesso nome.

    **InsertionStringTemplates** contiene il testo da inserire in un evento specificato in **EventType**. È possibile usare stringhe letterali o fare riferimento direttamente a una proprietà. Per altre informazioni, vedere [Uso di modelli di stringa standard](using-standard-string-templates.md) e Istruzione SELECT per le query di [eventi.](select-statement-for-event-queries.md)

    Usare un'origine esistente per il log eventi che supporta una stringa di inserimento senza testo associato.

    L'esempio di codice MOF seguente illustra come usare un'origine esistente di WSH e un **valore EventID** pari a 8.

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

    Nell'esempio seguente il filtro monitora la chiave del Registro di sistema in cui vengono registrati i programmi di avvio. Il monitoraggio di questa chiave del Registro di sistema può essere importante perché un programma non autorizzato può registrarsi sotto la chiave, causando l'avvio all'avvio del computer.

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

4.  Identificare un evento da monitorare e creare una query di eventi.

    È possibile verificare se è presente un evento intrinseco o estensiva che usa . Ad esempio, usare la [**classe RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del provider del Registro di sistema per monitorare le modifiche al Registro di sistema.

    Se non esiste una classe che descrive un evento che è necessario monitorare, è necessario creare un provider di eventi personalizzato e definire nuove classi di evento estensivi. Per altre informazioni, vedere [Scrittura di un provider di eventi](writing-an-event-provider.md).

    In un file MOF è possibile definire un [*alias*](gloss-a.md) per il filtro e il consumer, che fornisce un modo semplice per descrivere i percorsi dell'istanza.

    Nell'esempio seguente viene illustrato come definire un [*alias*](gloss-a.md) per il filtro e il consumer.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Creare un'istanza [**\_ \_ di FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro e le classi consumer. Questa istanza determina che quando si verifica un evento che corrisponde al filtro specificato, deve essere eseguita l'azione specificata dal consumer. [**\_ \_ EventFilter,**](--eventfilter.md) [**\_ \_ EventConsumer**](--eventconsumer.md)e **\_ \_ FilterToConsumerBinding** devono avere lo stesso SID (Individual Security Identifier) nella **proprietà CreatorSID.** Per altre informazioni, vedere [Associazione di un filtro eventi a un consumer logico.](binding-an-event-filter-with-a-logical-consumer.md)

    Nell'esempio seguente viene illustrato come identificare un'istanza in base al percorso dell'oggetto o usare un alias come espressione abbreviata per il percorso dell'oggetto .

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

    È possibile associare un filtro a diversi consumer, che indica che quando si verificano eventi corrispondenti, è necessario eseguire diverse azioni. oppure è possibile associare un consumer a diversi filtri, che indica che l'azione deve essere eseguita quando si verificano eventi che corrispondono a uno dei filtri.

    Le azioni seguenti vengono eseguite in base alla condizione dei consumer e degli eventi:

    -   Se uno dei consumer permanenti ha esito negativo, altri consumer che richiedono l'evento ricevono una notifica.
    -   Se un evento viene eliminato, WMI genera [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).
    -   Se si sottoscrive questo evento, restituisce l'evento eliminato e un riferimento a [**\_ \_ EventConsumer**](--eventconsumer.md) rappresenta il consumer non riuscito.
    -   Se un consumer ha esito negativo, WMI genera [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), che può contenere altre informazioni nelle proprietà **ErrorCode**, **ErrorDescription** **ed ErrorObject.**

    Per altre informazioni, vedere [Associazione di un filtro eventi a un consumer logico.](binding-an-event-filter-with-a-logical-consumer.md)

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato il file MOF per un'istanza di [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). Dopo aver compilato questo FILE MOF, qualsiasi tentativo di creare, eliminare o modificare un valore nel percorso del Registro di sistema **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run** registra una voce nel registro eventi dell'applicazione, sotto l'origine "WSH".


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

 

 
