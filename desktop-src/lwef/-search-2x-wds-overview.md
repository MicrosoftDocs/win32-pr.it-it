---
title: Windows Desktop Search 2. x
description: L'utilizzo di e lo sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore di Windows Search.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5131fe700b7b049371625249768b0073d009a87
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299772"
---
# <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

L'utilizzo di e lo sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore di [Windows Search](../search/-search-3x-wds-overview.md).

WDS è un servizio di indicizzazione e una piattaforma che consente la ricerca rapida di file e dati in diverse origini dati e posizioni. WDS consente agli utenti e ad altre applicazioni di trovare praticamente qualsiasi cosa nei propri computer, messaggi di posta elettronica, appuntamenti del calendario, foto, documenti e altro ancora. Inoltre, WDS può restituire risultati da più origini dati in un ambiente Esplora risorse, in modo che gli utenti possano visualizzare rapidamente un'anteprima, filtrare e agire sui risultati della ricerca.

WDS indicizza i dati all'interno di un determinato ambito di ricerca per indicizzazione, i percorsi specificati in un computer locale e la rete condivisa di cui l'indicizzatore deve eseguire la ricerca Questo ambito di ricerca può essere controllato dalle opzioni impostate dall'utente, dalle API di gestione e dai criteri di gruppo, che gli amministratori di rete possono configurare per controllare le autorizzazioni di accesso degli utenti e le impostazioni di indicizzazione. I criteri di gruppo possono limitare l'accesso a determinate risorse di rete, nonché definire le risorse da indicizzare.

Questa sezione contiene i seguenti argomenti:

-   [Overview](#windows-desktop-search-2x)
    -   [Informazioni sull'indicizzatore WDS](#about-the-wds-indexer)
    -   [Informazioni sul catalogo WDS](#about-the-wds-catalog)
    -   [Informazioni sul motore di ricerca e sui risultati](#about-the-search-engine-and-results)
-   [Sviluppo con WDS](#developing-with-wds)
    -   [Aggiunta di dati all'indice con componenti aggiuntivi](#adding-data-to-the-index-with-add-ins)
    -   [Esecuzione di query sull'indice](#querying-the-index)
-   [Requisiti di compatibilità](#compatibility-requirements)
    -   [System Requirements](#system-requirements)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

### <a name="about-the-wds-indexer"></a>Informazioni sull'indicizzatore WDS

Quando viene installato per la prima volta, l'indicizzatore esegue la ricerca per indicizzazione dei file più comuni dell'utente nella cartella documenti, nelle cartelle di posta elettronica Microsoft Outlook e Microsoft Outlook Express e nei percorsi specificati in Criteri di gruppo. Gli utenti possono anche specificare nuovi file e percorsi per l'indicizzatore da includere (o escludere) in ricerche per indicizzazione successive. Ogni percorso incluso viene identificato da un URL e l'indicizzatore si avvierà in corrispondenza di tale URL e scorre in modo ricorsivo tutte le sottocartelle o i percorsi fino a quando non sono stati indicizzati tutti gli elementi. Un ambito è un set di URL. Le API di gestione possono essere utilizzate da applicazioni personalizzate per definire l'ambito di ricerca per indicizzazione, un set di URL che puntano a percorsi all'interno di un protocollo, ad esempio `file://` per cartelle in un'unità o `mapi:// ` per archivi di posta elettronica MAPI come Outlook. WDS utilizza i gestori di protocollo per accedere agli archivi dati e ai filtri per analizzare e indicizzare il testo e le proprietà degli elementi. Questi dati vengono quindi archiviati nel catalogo.

### <a name="about-the-wds-catalog"></a>Informazioni sul catalogo WDS

Il catalogo WDS è un indice del testo e delle proprietà raccolti dagli elementi del messaggio di posta elettronica, delle unità locali, delle risorse di rete e di altri archivi dati locali specificati. Il contenuto del catalogo si basa su Opzioni e regole impostate da WDS, le applicazioni basate sulla piattaforma WDS, le preferenze utente e i criteri di gruppo. Per ogni elemento indicizzato sono disponibili oltre 200 proprietà, ad esempio la data di creazione, le dimensioni e le proprietà specifiche del tipo ("da" per i messaggi di posta elettronica). Per un elenco di queste proprietà, vedere [riferimento allo schema](-search-2x-wds-schematable.md)WDS.

### <a name="about-the-search-engine-and-results"></a>Informazioni sul motore di ricerca e sui risultati

Dalla deskbar di WDS o da Esplora risorse, gli utenti possono cercare il contenuto e i metadati della proprietà full-text degli elementi indicizzati. Gli stessi tipi di ricerche possono anche essere avviati dalla riga di comando, da una pagina Web o da un'applicazione personalizzata. Il motore di ricerca WDS individua gli elementi che corrispondono ai criteri di ricerca e li restituisce come set di risultati Microsoft ActiveX Data Objects (ADO). WDS Visualizza gli elementi che corrispondono ai criteri di ricerca e può presentare un'anteprima dettagliata dell'elemento. È possibile creare applicazioni per intercettare la query di ricerca, eseguire la ricerca e/o visualizzare il set di risultati.

## <a name="developing-with-wds"></a>Sviluppo con WDS

Sono disponibili due tipi principali di integrazione con WDS: l'aggiunta di dati all'indice e l'esecuzione di query sul contenuto dell'indice per recuperare i record corrispondenti ai criteri di ricerca.

### <a name="adding-data-to-the-index-with-add-ins"></a>Aggiunta di dati all'indice con Add-Ins

Sono fondamentalmente disponibili due tipi di origini dati: archivi file system e archivi non file system. Un gruppo di file in documenti è un semplice archivio file system. WDS è in grado di cercare informazioni nei file archiviati in un file system se è possibile individuare un filtro per il tipo di file. È possibile abilitare WDS per indicizzare un nuovo tipo di file proprietario se si fornisce un'implementazione dell'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per quel tipo di file.

Un archivio non file system, ad esempio un database, richiede un gestore di protocollo per consentire a WDS di spostarsi tra e indicizzare i dati all'interno dell'archivio dati. Se, ad esempio, si dispone di un client di posta elettronica che archivia l'elenco di messaggi di posta elettronica ricevuti in un file specifico, ad esempio file PST in Outlook, è possibile fornire un gestore di protocollo per indicizzare e cercare ogni singolo messaggio di posta elettronica fornendo un gestore di protocollo. Se l'archivio dati è gerarchico, sarà necessario implementare anche un'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per enumerare gli elementi nell'archivio. Per migliorare l'esperienza utente, è possibile implementare un'estensione della Shell per fornire menu di scelta rapida e icone dall'interno della visualizzazione dei risultati.

Attualmente, WDS contiene filtri per più di 200 tipi di elementi (inclusi elementi di testo non crittografato, ad esempio HTML, XML e file di codice sorgente) e utilizza lo stesso [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e la stessa tecnologia del gestore di protocollo di SharePoint Services. Se i filtri sono già installati per i tipi di file proprietari, WDS può utilizzare le interfacce di filtro esistenti per indicizzare i dati.

### <a name="querying-the-index"></a>Esecuzione di query sull'indice

WDS fornisce le applicazioni con set di risultati personalizzati di dati dall'indice in base a uno dei valori dello schema disponibili. I risultati vengono restituiti come set di record ADO. Sono disponibili quattro modi per incorporare le query WDS in un'applicazione, ciascuna delle quali offre diversi livelli di personalizzazione e affidabilità.

-   Interfaccia ISearchDesktop: le API in questa interfaccia vengono usate per chiamare WDS a livello di codice specificando una stringa di query, un elenco di colonne da restituire, le restrizioni di ambito simili a una clausola Structured Query Language (SQL) WHERE e il nome della colonna in base a cui eseguire l'ordinamento. Queste API sono disponibili per il codice nativo e gestito.
-   Controllo ActiveX WDS: questo controllo disegna l'interfaccia di ricerca WDS e gestisce la ricerca e la visualizzazione dei risultati. Questo metodo è più semplice rispetto all'uso delle API ma è meno flessibile. Per utilizzare questo controllo in un'applicazione Microsoft Visual Studio, passare alla finestra di dialogo **Scegli elementi della casella degli** strumenti dal menu **strumenti** e aggiungere "Windows Desktop Search-Results Viewer" alla **casella degli strumenti** dalla scheda **componenti com** . Aggiungere quindi il controllo al modulo in cui si desidera includerlo. Il controllo ActiveX WDS è compatibile con WDS 2. x e 3. x solo in Windows XP.
-   Parametri della riga di comando: le applicazioni possono chiamare il file eseguibile di WDS con diversi parametri per la ricerca e la visualizzazione dei risultati. Verrà aperta una finestra di WDS con i risultati visualizzati. Questo è il modo più semplice per aggiungere la ricerca a un'applicazione, ma non restituisce all'applicazione chiamante le informazioni relative all'operazione eseguita dall'utente all'interno della finestra WDS.
-   Object helper browser WDS (BHO): Analogamente, le pagine Web possono usare il file BHO per inviare query a WDS o l'applicazione di ricerca registrata. Dopo aver convalidato l'URL delle pagine Web rispetto all'elenco di sicurezza del dominio WDS, WDS eseguirà la query e visualizzerà i risultati usando l'interfaccia di ricerca standard o passerà la query all'applicazione di ricerca registrata.

Gli utenti possono utilizzare la [sintassi di query avanzata](-search-2x-wds-aqsreference.md) per eseguire query sul catalogo in modo più efficace controllando l'ambito delle ricerche e combinando i parametri di ricerca con gli operatori booleani. Ad esempio, un utente può cercare un allegato in un messaggio di posta elettronica da John che include "pianificazione progetto" o "piano progetto" con una query simile alla seguente: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Requisiti di compatibilità

WDS 2.6.5 è disponibile solo per Windows 2000, Windows Server 2003 e Windows XP. WDS è un download separato disponibile gratuitamente da Microsoft per uso personale e aziendale. Deve essere installato e utilizzato per l'indicizzazione dell'account utente prima che le applicazioni compilate per WDS 2.6.5 funzionino.

### <a name="system-requirements"></a>Requisiti di sistema

Per utilizzare la ricerca desktop di Windows, è necessario quanto segue:

-   Windows Internet Explorer o versione successiva.
-   Per includere i messaggi di posta elettronica nel catalogo, è necessario disporre di Microsoft Outlook 2000 o versione successiva o Microsoft Outlook Express 6,0 o versione successiva.
-   L'anteprima completa dei documenti di Microsoft Microsoft Office nella visualizzazione dei risultati richiede Office XP o versione successiva.
-   Processore Pentium 500 MHz minimo (consigliato 1 GHz).
-   Windows XP, Windows 2000 SP4 o versioni successive o Windows Server 2003 Service Pack 1.
-   Minimo 128 MB di RAM (256 MB consigliati).
-   500 MB di spazio disponibile su disco rigido consigliato. La dimensione dell'indice dipende dalla quantità di contenuto indicizzata.
-   1024 x 768 risoluzione dello schermo consigliata.

## <a name="related-topics"></a>Argomenti correlati

1.  Esecuzione di query sull'indice

    -   [Chiamata a WDS a livello di codice (tramite ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Chiamata di WDS da pagine Web](-search-2x-wds-browserhelpobject.md)
    -   [Chiamata di WDS dalla riga di comando](-search-2x-wds-fromcommandline.md)

2.  [Estensione dell'indice (panoramica)](-search-2x-wds-extendingtheindex.md)

    -   [Sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md)

3.  Riferimenti generali

    -   [Schema WDS](-search-2x-wds-schematable.md)
    -   [Sintassi di ricerca avanzata](-search-2x-wds-aqsreference.md)
    -   [Tipi percepiti WDS](-search-2x-wds-perceivedtype.md)

 

 