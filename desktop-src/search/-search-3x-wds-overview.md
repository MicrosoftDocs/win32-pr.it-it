---
description: Windows La ricerca è una piattaforma di ricerca desktop con funzionalità di ricerca immediata per i tipi di dati e i tipi di file più comuni e gli sviluppatori di terze parti possono estendere queste funzionalità a nuovi tipi di file e tipi di dati.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Panoramica di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a38b757936e9f960d71ac5d1a9759208b4b580af2526e23d4e5d88cde41a206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033129"
---
# <a name="windows-search-overview"></a>Panoramica di Windows Search

Windows La ricerca è una piattaforma di ricerca desktop con funzionalità di ricerca immediata per i tipi di dati e i tipi di file più comuni e gli sviluppatori di terze parti possono estendere queste funzionalità a nuovi tipi di file e tipi di dati.

Questo argomento è organizzato come segue:

-   [Introduzione](#introduction)
    -   [Servizio Windows Search](#windows-search-service)
    -   [Piattaforma di sviluppo](#development-platform)
    -   [Interfaccia utente](#user-interface)
-   [Prerequisiti tecnici](#technical-prerequisites)
    -   [Download e contenuto dell'SDK](#sdk-download-and-contents)
-   [Windows Cercare la documentazione dell'SDK](#windows-search-sdk-documentation)
-   [Cronologia della Windows ricerca](#history-of-windows-search)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Windows La ricerca è un componente standard di Windows 7 e Windows Vista ed è abilitata per impostazione predefinita. Windows Search sostituisce Windows Desktop Search (WDS), disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.

Windows La ricerca è costituita da tre componenti:

-   [Windows Search Service](#windows-search-service) (WSS)
-   [Piattaforma di sviluppo](#development-platform)
-   [Interfaccia utente](#user-interface)

### <a name="windows-search-service"></a>Servizio Windows Search

Il WSS organizza le funzionalità estratte di una raccolta di documenti. Il Windows Search Protocol consente a un client di comunicare con un server che ospita un WSS, sia per eseguire query che per consentire a un amministratore di gestire il server di indicizzazione. Durante l'elaborazione dei file, WSS analizza un set di documenti, estrae informazioni utili e quindi organizza le informazioni estratte in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query.

Una raccolta di documenti su cui è possibile eseguire query include un catalogo, ovvero l'unità organizzativa di livello più alto in Windows Ricerca. Un catalogo rappresenta un set di documenti indicizzati su cui è possibile eseguire query. Un catalogo è costituito da una tabella delle proprietà con il testo o il valore e la posizione corrispondente (impostazioni locali) archiviate nelle colonne della tabella. Ogni riga della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni colonna della tabella corrisponde a una proprietà . Un catalogo può contenere un indice invertito (per la corrispondenza rapida delle parole) e una cache delle proprietà (per il recupero rapido dei valori delle proprietà).

Il processo dell'indicizzatore viene implementato come servizio Windows in esecuzione nell'account LocalSystem ed è sempre in esecuzione per tutti gli utenti (anche se nessun utente è connesso), che consente Windows Search di eseguire le operazioni seguenti:

-   Mantenere un indice condiviso tra tutti gli utenti.
-   Mantenere le restrizioni di sicurezza per l'accesso al contenuto.
-   Elaborare query remote dai computer client in rete.

Il servizio di ricerca è progettato per proteggere l'esperienza utente e le prestazioni del sistema durante l'indicizzazione. Le condizioni seguenti causano la limitazione o la sospensione dell'indicizzazione da parte del servizio:

-   Utilizzo elevato della CPU da parte di processi non correlati alla ricerca.
-   Frequenza di I/O di sistema elevata, tra cui operazioni di lettura e scrittura di file, I/O di file di pagina e cache file e I/O di file mappati.
-   Disponibilità di memoria insufficiente.
-   Durata della batteria insufficiente.
-   Spazio su disco insufficiente nell'unità in cui è archiviato l'indice.

### <a name="development-platform"></a>Piattaforma di sviluppo

Il modo preferito per accedere alle API di ricerca e creare Windows di ricerca è tramite un'origine dati shell. Un'origine dati Shell è un componente usato per estendere lo spazio dei nomi Shell ed esporre elementi in un archivio dati. Un archivio dati è un repository di dati. Un archivio dati può essere esposto al modello di programmazione Shell come contenitore che usa un'origine dati shell. Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows tramite un gestore di protocollo.

Ad esempio, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) è un componente che può creare istanze dell'origine dati della cartella di ricerca, ovvero una sorta di origine dati "virtuale" fornita da Shell che può eseguire query su altre origini dati nello spazio dei nomi Shell ed enumerare i risultati. A tale scopo, è possibile usare l'indicizzatore o enumerando e controllando manualmente gli elementi negli ambiti specificati. Questa interfaccia consente di impostare i parametri della ricerca usando i metodi che creano e modificano le cartelle di ricerca. Se i metodi di questa interfaccia non vengono chiamati, vengono usati i valori predefiniti.

L'accesso Windows funzionalità di ricerca indirettamente tramite il modello di dati Shell è preferibile perché fornisce l'accesso alla funzionalità Shell completa a livello del modello di dati shell. Ad esempio, è possibile impostare l'ambito di una ricerca su una libreria (che è una funzionalità disponibile in Windows 7 e versioni successive) per usare le cartelle della libreria come ambito della query. Windows La ricerca aggrega quindi i risultati della ricerca da tali percorsi se si tratta di indici diversi (se le cartelle si esereranno in computer diversi). Il livello dati Shell crea anche una visualizzazione più completa delle proprietà degli elementi, sintetizzando alcuni valori di proprietà. Fornisce anche l'accesso alle funzionalità di ricerca per gli archivi dati non indicizzati Windows ricerca. Ad esempio, è possibile cercare dispositivi di archiviazione USB (Universal Serial Bus), dispositivi portatili che utilizzano il protocollo MTP o un server File Transfer Protocol (FTP) tramite le origini dati shell che forniscono l'accesso a tali sistemi di archiviazione. In questo modo si garantisce una migliore esperienza utente.

Windows La ricerca include una cache di valori di proprietà che viene usata nell'implementazione del Windows Search Service (WSS). È possibile eseguire query su questi valori di proprietà a livello di codice usando il provider OLE DB di ricerca Windows o [tramite ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), che rappresenta gli elementi nei risultati della ricerca e nelle visualizzazioni basate su query. Windows La ricerca raccoglie e archivia quindi le proprietà generate dai gestori di filtri o dai gestori delle proprietà quando un elemento, ad esempio un documento di Word, viene indicizzato. Questo archivio viene eliminato e ricompilato quando l'indice viene ricompilato.

Gli sviluppatori di terze parti possono creare applicazioni che utilizzano i dati nell'indice tramite query a livello di codice e possono estendere i dati nell'indice per i tipi di file ed elementi personalizzati da indicizzare Windows ricerca. Se si desidera visualizzare i risultati della query in Windows Explorer, è necessario implementare un'origine dati shell prima di poter creare un gestore di protocollo per estendere l'indice. Tuttavia, se tutte le query sono a livello di codice (ad esempio tramite OLE DB) e interpretate dal codice dell'applicazione anziché dalla Shell, uno spazio dei nomi Shell è comunque preferibile, ma non obbligatorio.

Un gestore di protocollo è necessario per Windows ottenere informazioni sul contenuto dei file, ad esempio elementi nei database o tipi di file personalizzati. Sebbene Windows ricerca possa indicizzare il nome e le proprietà del file, Windows non ha informazioni sul contenuto del file. Di conseguenza, tali elementi non possono essere indicizzati o esposti nella Windows Shell. Implementando un gestore di protocollo personalizzato, è possibile esporre questi elementi. Per un elenco dei gestori identificati dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in Windows [Ricerca come piattaforma di sviluppo](-search-3x-wds-development-ovr.md).

> [!Note]  
> Un'origine dati Shell è talvolta nota come estensione dello spazio dei nomi Shell. Un gestore è talvolta noto come estensione shell o gestore dell'estensione shell.

 

### <a name="user-interface"></a>Interfaccia utente

In Windows Vista e versioni successive, Windows ricerca è integrata in tutte le finestre Windows Explorer per l'accesso immediato alla ricerca. In questo modo gli utenti possono cercare rapidamente file ed elementi in base al nome, alle proprietà e al contenuto full-text. È anche possibile filtrare ulteriormente i risultati per perfezionare la ricerca. Ecco alcune altre funzionalità di Windows ricerca:

-   Una casella di ricerca immediata in ogni finestra consente di filtrare immediatamente tutti gli elementi attualmente visualizzati. Le caselle di ricerca immediata vengono visualizzate nel menu Start per cercare programmi o file e nell'angolo superiore destro di tutte le finestre di esplora Windows per filtrare i risultati visualizzati. La ricerca immediata è integrata anche in altre funzionalità Windows, ad esempio Windows Media Player, per trovare i file correlati.
-   I documenti possono essere contrassegnati con parole chiave per raggrupparli in base ai criteri personalizzati definiti dall'utente. I tag sono elementi di metadati assegnati dall'utente o dalle applicazioni per semplificare l'individuazione dei file in base a parole chiave che potrebbero non essere presenti nel nome o nel contenuto dell'elemento. Ad esempio, un set di immagini potrebbe essere contrassegnato come "Arizona Vacation 2009" per recuperarsi rapidamente in un secondo momento cercando una delle parole incluse.
-   Le intestazioni di colonna avanzate nelle Windows Explorer consentono l'ordinamento e il raggruppamento dei documenti in modi diversi. Ad esempio, i file possono essere ordinati in base al nome, alla data di modifica, al tipo, alle dimensioni e ai tag. I documenti possono anche essere raggruppati in base a una di queste proprietà e ogni gruppo può essere filtrato (nascosto o visualizzato) in base alle esigenze.
-   I documenti possono essere impilati in base al nome, alla data di modifica, al tipo, alle dimensioni e ai tag. Gli stack includono tutti i documenti con la proprietà specificata e che si trovano all'interno di qualsiasi sottocartella della cartella selezionata.
-   Le ricerche possono essere salvate (da recuperare in un secondo momento) facendo clic sul pulsante Salva **ricerca** nel riquadro di ricerca in Windows Explorer. I risultati verranno ripopolati dinamicamente in base ai criteri originali quando viene aperta la ricerca salvata. Per istruzioni, vedere [Salvare i risultati della ricerca.](https://windows.microsoft.com/windows-vista/Save-your-search-results)
-   I gestori di anteprima e i gestori di anteprime consentono agli utenti di visualizzare in anteprima i documenti in Windows Explorer senza dover aprire l'applicazione che li ha creati.

## <a name="technical-prerequisites"></a>Prerequisiti tecnici

Prima di iniziare a leggere la documentazione Windows Search SDK, è necessario avere una conoscenza di base dei concetti seguenti:

-   Come implementare un'origine dati shell.
-   Come implementare un gestore.
-   Come usare il codice nativo.

Un'origine dati Shell è un componente usato per estendere lo spazio dei nomi Shell ed esporre elementi in un archivio dati. In passato, l'origine dati Shell è stata definita estensione dello spazio dei nomi Shell. Un gestore è un Component Object Model (COM) che fornisce funzionalità per un elemento della shell. Per un elenco dei gestori identificati dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in Windows [Search as a Development Platform](-search-3x-wds-development-ovr.md).

Per altre informazioni sull'assembly di interoperabilità di Windows Search SDK per l'uso di oggetti COM esposti da ricerca Windows e altri programmi che usano codice gestito, vedere Uso di codice gestito con i dati della shell e ricerca [Windows .](-search-3x-wds-managed-code.md) Si noti tuttavia che i filtri, i gestori di proprietà e i gestori di protocollo devono essere scritti in codice nativo. Ciò è dovuto a potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo in cui vengono eseguiti più componenti aggiuntivi. Gli sviluppatori che non hanno mai iniziato a usare C++ possono iniziare a usare Visual C++ [Developer Center](https://msdn.microsoft.com/vstudio//default.aspx) e Windows Development [Attività iniziali](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Download e contenuti dell'SDK

Oltre a soddisfare i requisiti tecnici elencati, è necessario scaricare anche Windows [SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per ottenere le librerie di Windows ricerca. Gli [Windows SDK di ricerca contengono](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) esempi di codice utili e un assembly di interoperabilità per lo sviluppo con codice gestito. Per altre informazioni sull'uso degli esempi di codice, vedere Windows [di codice di ricerca.](-search-3x-wds-sampleentry.md)

## <a name="windows-search-sdk-documentation"></a>Windows Documentazione dell'SDK di ricerca

Il contenuto della documentazione Windows Search SDK è il seguente:

-   [Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md)

    Descrive i principali scenari di sviluppo in Windows ricerca. Fornisce un elenco di gestori identificati dallo scenario di sviluppo che si sta tentando di ottenere, le linee guida per il programma di installazione dei componenti aggiuntivi e le note sull'implementazione.

-   [Windows Guida per gli sviluppatori di ricerca](-search-developers-guide-entry-page.md)

    Vengono fornite spiegazioni per la gestione [dell'indice,](-search-3x-wds-mngidx-overview.md) [l'esecuzione di query sull'indice a](-search-3x-wds-qryidx-overview.md)livello di codice, [l'estensione dell'indice](-search-3x-wds-extidx-overview.md)e l'estensione [delle risorse del linguaggio](extending-language-resources-in-windows-search.md).

-   [Windows Informazioni di riferimento sulla ricerca](-search-reference-entry-page.md)

    Documenta le categorie seguenti di Windows di ricerca: gestori di protocollo, [query,](-search-querying-interfaces-entry-page.md)ambito [](-search-index-mgt-interfaces-entry-page.md)della ricerca per [indicizzazione,](-search-crawl-scope-interfaces-entry-page.md)componenti aggiuntivi [dati,](-search-data-addins-interfaces-entry-page.md)gestione degli indici e [](-search-protocol-handlers-interfaces-entry-page.md) [notifiche.](-search-notifications-interfaces-entry-page.md) La documentazione di riferimento include anche [costanti ed enumerazioni](-search-constants-and-enumerations-entry-page.md), [strutture](-search-structures-entry-page.md), [mapping delle](-search-3x-wds-propertymappings.md)proprietà e il formato di file di [ricerca salvato](-search-savedsearchfileformat.md).

-   [Windows Esempi di codice di ricerca](-search-samples-ovw.md)

    Descrive gli esempi di codice dell'API di ricerca disponibili.

-   [Ricerca federata in Windows](-search-federated-search-overview.md)

    Descrive Windows 7 per la federazione della ricerca in archivi dati remoti usando tecnologie OpenSearch che consentono agli utenti di accedere e interagire con i dati remoti da Windows Explorer.

-   [Tecnologie di ricerca correlate](-search-3x-wds-sampleentry.md)

    Elenca le tecnologie correlate Windows ricerca: ricerca Enterprise, ricerca SharePoint Enterprise e applicazioni legacy come Windows Desktop Search 2.x e Platform SDK: servizio di indicizzazione.

-   [Windows Glossario della ricerca](search-glossary.md)

    Definisce i termini essenziali usati nelle Windows di ricerca e shell.

## <a name="history-of-windows-search"></a>Cronologia della Windows ricerca

Windows Search sostituisce Windows Desktop Search (WDS), disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. WDS ha sostituito il servizio di indicizzazione legacy delle versioni precedenti di Windows con miglioramenti a prestazioni, usabilità ed estendibilità. La nuova piattaforma di sviluppo supporta requisiti che producono un sistema più sicuro e stabile. Anche se la nuova piattaforma di query non è compatibile con Microsoft Windows Desktop Search (WDS) 2.x, i filtri e i gestori di protocollo scritti per le versioni precedenti di WDS possono essere aggiornati per funzionare con Windows Search. Windows La ricerca supporta anche un nuovo sistema di proprietà. Per informazioni su filtri, gestori di proprietà e gestori di protocollo, vedere [Estensione dell'indice.](-search-3x-wds-extidx-overview.md)

Windows La ricerca è incorporata Windows Vista e versioni successive ed è disponibile come aggiornamento ridistribuibile di WDS 2.x per supportare i sistemi operativi seguenti:

-   Versioni a 32 bit di Windows XP con Service Pack 2 (SP2).
-   Tutte le versioni basate su x64 di Windows XP.
-   Windows Server 2003 con Service Pack 1 (SP1) e versioni successive.
-   Tutte le versioni basate su x64 di Windows Server 2003.

Nei sistemi che eseguono questi sistemi operativi è necessario Windows ricerca per eseguire le applicazioni scritte per Windows ricerca. Per altre informazioni, vedere l'articolo della Knowledge Base [917013: Descrizione di Windows Desktop Search 3.01 e interfaccia utente multilingue Pack per Windows Desktop Search 3.01.](https://support.microsoft.com/kb/917013)

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sulla creazione di un'origine dati shell, vedere [Implementazione delle interfacce dell'oggetto cartella di base.](/previous-versions//bb776815(v=vs.85))
-   Per altre informazioni su [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) e sull'origine dati della cartella db, vedere la descrizione della costante STR \_ PARSE WITH PROPERTIES in Bind Context String \_ \_ [Keys](../shell/str-constants.md). Vedere anche [Association Arrays](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) e [IPropertySystem::GetPropertyDescriptionListFromString.](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring)
-   Per informazioni su OLE DB, vedere Panoramica [OLE DB programmazione .](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019) Per informazioni sull'.NET Framework provider di dati per OLE DB, vedere la documentazione dello spazio dei [nomi System.Data.OleDb.](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true)
-   Per una panoramica dei gestori dei tipi di file (noti anche come gestori dell'estensione della shell e gestori di ricerca), vedere Windows Search as a Development Platform ( Cerca come [piattaforma di sviluppo).](-search-3x-wds-development-ovr.md)
-   Per le bacheche di messaggi supportate dalla community sulle tecnologie di ricerca, vedere il [forum MSDN: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)( Sviluppo di ricerca desktop).
-   Per esempi di codice correlati, vedere Windows [di codice di ricerca.](-search-samples-ovw.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Lingue supportate dalla Windows ricerca](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso di codice gestito con i dati della shell e Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
