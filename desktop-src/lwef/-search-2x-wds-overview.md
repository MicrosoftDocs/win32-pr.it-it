---
title: Windows Desktop Search 2.x
description: Informazioni su Windows Desktop Search 2.x. Per le versioni di Windows successive a Windows XP e Windows Server 2003, usare Windows Search.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ff43f827458d295e54b71b3f39c7aa471c058d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408124"
---
# <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2.x

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare [invece Windows Search.](../search/-search-3x-wds-overview.md)

L'uso di e lo sviluppo per le versioni 2.x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato a favore [di Windows Search](../search/-search-3x-wds-overview.md).

WDS è un servizio di indicizzazione e una piattaforma che consente una ricerca rapida di file e dati in origini dati e percorsi diversi. WDS consente a utenti e altre applicazioni di trovare quasi tutto ciò che si trova nei loro computer, messaggi di posta elettronica, appuntamenti del calendario, foto, documenti e altro ancora. WdS può inoltre restituire risultati da più origini dati in un ambiente Esplora risorse in modo che gli utenti possano visualizzare in anteprima, filtrare e agire rapidamente sui risultati della ricerca.

WDS indicizza i dati all'interno di un determinato ambito di ricerca per indicizzazione, i percorsi specificati all'interno di un computer locale e di una rete condivisa in cui l'indicizzatore deve eseguire la ricerca per indicizzazione. Questo ambito di ricerca per indicizzazione può essere controllato dalle opzioni impostate dall'utente, dalle API di gestione e dai criteri di gruppo, che gli amministratori di rete possono configurare per controllare le autorizzazioni di accesso utente e le impostazioni di indicizzazione. I criteri di gruppo possono limitare l'accesso a determinate risorse di rete e definire le risorse da indicizzare.

Questa sezione contiene i seguenti argomenti:

-   [Panoramica](#windows-desktop-search-2x)
    -   [Informazioni sull'indicizzatore wds](#about-the-wds-indexer)
    -   [Informazioni sul catalogo di Servizi di distribuzione Windows](#about-the-wds-catalog)
    -   [Informazioni sul motore di ricerca e sui risultati](#about-the-search-engine-and-results)
-   [Sviluppo con WDS](#developing-with-wds)
    -   [Aggiunta di dati all'indice con componenti aggiuntivi](#adding-data-to-the-index-with-add-ins)
    -   [Esecuzione di query sull'indice](#querying-the-index)
-   [Requisiti di compatibilità](#compatibility-requirements)
    -   [System Requirements](#system-requirements)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

### <a name="about-the-wds-indexer"></a>Informazioni sull'indicizzatore wds

Quando viene installato per la prima volta, l'indicizzatore esegue la ricerca per indicizzazione dei file più comuni per gli utenti nella cartella Documenti, nelle cartelle di posta elettronica di Microsoft Outlook e Microsoft Outlook Express e nei percorsi specificati in Criteri di gruppo. Gli utenti possono anche specificare nuovi file e percorsi per l'indicizzatore da includere (o escludere) nelle ricerche per indicizzazione successive. Ogni posizione inclusa è identificata dall'URL e l'indicizzatore inizierà da tale URL e scorrerà in modo ricorsivo tutte le sottocartelle o i percorsi fino a quando tutti gli elementi non sono stati indicizzati. Un ambito è un set di URL. Le API di gestione possono essere usate dalle applicazioni personalizzate per definire l'ambito della ricerca per indicizzazione, un set di URL che puntano ai percorsi all'interno di un protocollo, ad esempio per le cartelle in un'unità o per gli archivi di posta elettronica MAPI come `file://` `mapi:// ` Outlook. WDS usa gestori di protocollo per accedere agli archivi dati e ai filtri per analizzare e indicizzare il testo e le proprietà degli elementi. Questi dati vengono quindi archiviati nel catalogo.

### <a name="about-the-wds-catalog"></a>Informazioni sul catalogo di Servizi di distribuzione Windows

Il catalogo di Servizi di distribuzione Windows è un indice di testo e proprietà raccolte da elementi in posta elettronica, unità locali, risorse di rete e altri archivi dati locali specificati. Il contenuto del catalogo si basa su opzioni e regole impostate da Servizi di distribuzione Windows, applicazioni basate sulla piattaforma WDS, preferenze utente e criteri di gruppo. Sono disponibili oltre 200 proprietà per ogni elemento indicizzato, ad esempio data di creazione, dimensioni e proprietà specifiche del tipo ("Da" per i messaggi di posta elettronica). Per un elenco di queste proprietà, vedere wds [Schema Reference](-search-2x-wds-schematable.md).

### <a name="about-the-search-engine-and-results"></a>Informazioni sul motore di ricerca e sui risultati

Da WDS Deskbar o da Esplora risorse, gli utenti possono eseguire ricerche nel contenuto full-text e nei metadati delle proprietà degli elementi indicizzati. Gli stessi tipi di ricerche possono essere avviati anche dalla riga di comando, da una pagina Web o da un'applicazione personalizzata. Il motore di ricerca wds individua gli elementi corrispondenti ai criteri di ricerca e li restituisce come set di risultati di Microsoft ActiveX Data Objects (ADO). WDS visualizza gli elementi corrispondenti ai criteri di ricerca e può presentare un'anteprima avanzata dell'elemento. È possibile creare applicazioni per intercettare la query di ricerca, eseguire la ricerca e/o visualizzare il set di risultati.

## <a name="developing-with-wds"></a>Sviluppo con WDS

Esistono due tipi principali di integrazione con WDS: l'aggiunta di dati all'indice e l'esecuzione di query sul contenuto dell'indice per recuperare i record corrispondenti ai criteri di ricerca.

### <a name="adding-data-to-the-index-with-add-ins"></a>Aggiunta di dati all'indice con Add-Ins

Esistono fondamentalmente due tipi di origini dati: file system e archivi non file system dati. Un gruppo di file in Documenti è un semplice file system archiviazione. WDS può cercare informazioni nei file archiviati in un file system se è in grado di individuare un filtro per il tipo di file. È possibile abilitare Servizi di distribuzione Windows per indicizzare un nuovo tipo di file proprietario se si fornisce un'implementazione [**dell'interfaccia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per tale tipo di file.

Un archivio non file system, ad esempio un database, richiede un gestore di protocollo per consentire a Servizi di distribuzione Windows di spostarsi all'interno dell'archivio dati e indicizzare i dati. Ad esempio, se si dispone di un client di posta elettronica che archivia l'elenco dei messaggi di posta elettronica ricevuti nel proprio file (ad esempio file PST in Outlook), è possibile fornire un gestore di protocollo per indicizzare e cercare ogni singolo messaggio di posta elettronica fornendo un gestore di protocollo. Se l'archivio dati è gerarchico, sarà necessario implementare anche [**un'interfaccia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)per enumerare gli elementi nell'archivio. Per un'esperienza utente migliore, è possibile implementare un'estensione della shell per fornire menu di scelta rapida e icone all'interno della visualizzazione risultati.

WdS attualmente contiene filtri per più di 200 tipi di elementi (inclusi elementi di testo non crittografato come HTML, XML e file di codice sorgente) e usa la stessa [**tecnologia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e gestore di protocollo di SharePoint Services. Se sono già installati filtri per i tipi di file proprietari, WDS può usare le interfacce di filtro esistenti per indicizzare questi dati.

### <a name="querying-the-index"></a>Esecuzione di query sull'indice

WDS fornisce alle applicazioni set di risultati personalizzati di dati dall'indice in base a uno dei valori dello schema disponibili. I risultati vengono restituiti come set di record ADO. Esistono quattro modi per incorporare le query wds in un'applicazione, ognuna delle quali offre vari livelli di personalizzazione e affidabilità.

-   Interfaccia ISearchDesktop: le API in questa interfaccia vengono usate per chiamare WDS a livello di codice specificando una stringa di query, un elenco di colonne da restituire, restrizioni di ambito simili a una clausola WHERE di Structured Query Language (SQL) e il nome della colonna in base alla quale eseguire l'ordinamento. Queste API sono disponibili per il codice nativo e gestito.
-   Controllo ActiveX WDS: questo controllo disegna l'interfaccia di ricerca di WDS e gestisce la ricerca e la visualizzazione dei risultati. Questo metodo è più semplice rispetto all'uso delle API, ma è meno flessibile. Per usare questo controllo in un'applicazione Microsoft Visual Studio, passare alla finestra di dialogo Scegli elementi della casella  degli strumenti dal **menu** Strumenti e aggiungere "Windows Desktop Search - Visualizzatore risultati" alla casella degli strumenti dalla **scheda Componenti COM.**  Aggiungere quindi il controllo al form in cui si vuole includerlo. Il controllo ActiveX wds è compatibile con WDS 2.x e 3.x solo in Windows XP.
-   Parametri della riga di comando: le applicazioni possono chiamare l'eseguibile wds con vari parametri per cercare e visualizzare i risultati. Verrà aperta una finestra di Servizi di distribuzione Windows con i risultati visualizzati. Questo è il modo più semplice per aggiungere la ricerca a un'applicazione, ma non restituisce all'applicazione chiamante informazioni sulle funzionalità dell'utente all'interno della finestra di Servizi di distribuzione Windows.
-   WDS Browser Helper Object (THEO): analogamente, le pagine Web possono usare LA FUNZIONE PER inviare query a WDS o all'applicazione di ricerca registrata. Dopo aver convalidato l'URL delle pagine Web rispetto all'elenco di sicurezza del dominio di Servizi di distribuzione Windows, WDS eseguirà la query e visualizza i risultati usando l'interfaccia di ricerca standard o passerà la query all'applicazione di ricerca registrata.

Gli utenti possono usare [la sintassi di query](-search-2x-wds-aqsreference.md) avanzata per eseguire query sul catalogo in modo più efficace controllando l'ambito delle ricerche e combinando i parametri di ricerca con gli operatori booleani. Ad esempio, un utente può cercare un allegato in un messaggio di posta elettronica di Giorgio che include "pianificazione del progetto" o "piano di progetto" con una query simile alla seguente: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Requisiti di compatibilità

WDS 2.6.5 è disponibile solo per Windows 2000, Windows Server 2003 e Windows XP. WDS è un download separato disponibile gratuitamente da Microsoft per uso personale e aziendale. Deve essere installato e in uso per l'indicizzazione dell'account utente prima che le applicazioni compilate per WDS 2.6.5 funzionino.

### <a name="system-requirements"></a>Requisiti di sistema

Per usare Windows Desktop Search sono necessari gli elementi seguenti:

-   Windows Internet Explorer o versione successiva.
-   Per includere i messaggi di posta elettronica nel catalogo, è necessario avere Microsoft Outlook 2000 o versione successiva oppure Microsoft Outlook Express 6.0 o versione successiva.
-   L'anteprima completa dei Microsoft Office Microsoft nella visualizzazione risultati richiede Office XP o versione successiva.
-   Processore Pentium minimo a 500 MHz (consigliato 1 GHz).
-   Windows XP, Windows 2000 SP4 o versioni successive o Windows Server 2003 Service Pack 1.
-   Almeno 128 MB di RAM (consigliati 256 MB).
-   Consigliati 500 MB di spazio libero su disco rigido. Le dimensioni dell'indice dipendono dalla quantità di contenuto indicizzato.
-   Risoluzione dello schermo 1024 x 768 consigliata.

## <a name="related-topics"></a>Argomenti correlati

1.  Esecuzione di query sull'indice

    -   [Chiamata di WDS a livello di codice (tramite ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Chiamata di WDS da pagine Web](-search-2x-wds-browserhelpobject.md)
    -   [Chiamata di WDS dalla riga di comando](-search-2x-wds-fromcommandline.md)

2.  [Estensione dell'indice (panoramica)](-search-2x-wds-extendingtheindex.md)

    -   [Sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md)

3.  Riferimenti generali

    -   [WDS Schema](-search-2x-wds-schematable.md)
    -   [Sintassi di ricerca avanzata](-search-2x-wds-aqsreference.md)
    -   [Tipi percepiti di WDS](-search-2x-wds-perceivedtype.md)

 

 