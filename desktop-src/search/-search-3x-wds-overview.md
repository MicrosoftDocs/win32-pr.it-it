---
description: Windows Search è una piattaforma di ricerca desktop con funzionalità di ricerca immediata per la maggior parte dei tipi di file e tipi di dati comuni e gli sviluppatori di terze parti possono estendere tali funzionalità ai nuovi tipi di file e tipi di dati.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Panoramica di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee4cde62ce663c47ab4cafac0c74ca220fe6faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878826"
---
# <a name="windows-search-overview"></a>Panoramica di Windows Search

Windows Search è una piattaforma di ricerca desktop con funzionalità di ricerca immediata per la maggior parte dei tipi di file e tipi di dati comuni e gli sviluppatori di terze parti possono estendere tali funzionalità ai nuovi tipi di file e tipi di dati.

Questo argomento è organizzato nel modo seguente:

-   [Introduzione](#introduction)
    -   [Servizio Windows Search](#windows-search-service)
    -   [Piattaforma di sviluppo](#development-platform)
    -   [Interfaccia utente](#user-interface)
-   [Prerequisiti tecnici](#technical-prerequisites)
    -   [Download e contenuti dell'SDK](#sdk-download-and-contents)
-   [Documentazione di Windows Search SDK](#windows-search-sdk-documentation)
-   [Cronologia di Windows Search](#history-of-windows-search)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Windows Search è un componente standard di Windows 7 e Windows Vista ed è abilitato per impostazione predefinita. Windows Search sostituisce Windows Desktop Search (WDS), disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.

Windows Search è costituito da tre componenti:

-   [Windows servizio di ricerca](#windows-search-service) (WSS)
-   [Piattaforma di sviluppo](#development-platform)
-   [Interfaccia utente](#user-interface)

### <a name="windows-search-service"></a>Servizio Windows Search

WSS organizza le funzionalità estratte di una raccolta di documenti. Il protocollo di ricerca di Windows consente a un client di comunicare con un server che ospita un WSS, sia per eseguire query che per consentire a un amministratore di gestire il server di indicizzazione. Quando si elaborano i file, WSS analizza un set di documenti, estrae informazioni utili e quindi organizza le informazioni estratte in modo che le proprietà di tali documenti possano essere restituite in modo efficiente in risposta alle query.

Una raccolta di documenti su cui è possibile eseguire query è costituita da un catalogo, che è l'unità di livello più elevata dell'organizzazione in Windows Search. Un catalogo rappresenta un set di documenti indicizzati su cui è possibile eseguire query. Un catalogo è costituito da una tabella delle proprietà con il testo o il valore e il percorso corrispondente (impostazioni locali) archiviato nelle colonne della tabella. Ogni riga della tabella corrisponde a un documento separato nell'ambito del catalogo e ogni colonna della tabella corrisponde a una proprietà. Un catalogo può contenere un indice invertito (per la corrispondenza rapida delle parole) e una cache delle proprietà (per il recupero rapido dei valori delle proprietà).

Il processo dell'indicizzatore viene implementato come un servizio Windows in esecuzione nell'account LocalSystem ed è sempre in esecuzione per tutti gli utenti (anche se nessun utente è connesso), che consente a Windows Search di eseguire le operazioni seguenti:

-   Gestire un indice condiviso tra tutti gli utenti.
-   Mantenere le restrizioni di sicurezza per l'accesso al contenuto.
-   Elaborare query remote da computer client in rete.

Il servizio di ricerca è progettato per proteggere l'esperienza utente e le prestazioni del sistema durante l'indicizzazione. Le condizioni seguenti provocano il rallentamento o la sospensione dell'indicizzazione del servizio:

-   Utilizzo CPU elevato da processi non correlati alla ricerca.
-   Velocità elevata di I/O del sistema, incluse letture e scritture di file, I/O file di paging e I/o di file mappati.
-   Disponibilità di memoria insufficiente.
-   Durata della batteria insufficiente.
-   Spazio su disco insufficiente nell'unità in cui è archiviato l'indice.

### <a name="development-platform"></a>Piattaforma di sviluppo

Il modo migliore per accedere alle API di ricerca e creare applicazioni Windows Search consiste nell'usare un'origine dati della shell. Un'origine dati della shell è un componente usato per estendere lo spazio dei nomi della shell ed esporre gli elementi in un archivio dati. Un archivio dati è un repository di dati. Un archivio dati può essere esposto al modello di programmazione della shell come contenitore che usa un'origine dati della shell. Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo.

Ad esempio, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) è un componente in grado di creare istanze dell'origine dati della cartella di ricerca, ovvero un tipo di origine dati "virtuale" fornita dalla shell che può eseguire query su altre origini dati nello spazio dei nomi della shell ed enumerare i risultati. Questa operazione può essere eseguita usando l'indicizzatore o enumerando manualmente ed esaminando gli elementi negli ambiti specificati. Questa interfaccia consente di configurare i parametri della ricerca usando i metodi che creano e modificano le cartelle di ricerca. Se non vengono chiamati metodi di questa interfaccia, vengono invece utilizzati i valori predefiniti.

È preferibile accedere indirettamente alla funzionalità di ricerca di Windows tramite il modello di dati della shell perché fornisce l'accesso alle funzionalità complete della shell a livello del modello di dati della shell. Ad esempio, è possibile impostare l'ambito di una ricerca su una raccolta, ovvero una funzionalità disponibile in Windows 7 e versioni successive, per utilizzare le cartelle di libreria come ambito della query. Windows Search quindi aggrega i risultati della ricerca da tali percorsi se sono in indici diversi (se le cartelle si trovano in computer diversi). Il livello dati della shell crea anche una visualizzazione più completa delle proprietà degli elementi, sintetizzando alcuni valori di proprietà. Fornisce inoltre l'accesso alle funzionalità di ricerca per gli archivi dati che non sono indicizzati da ricerca di Windows. È ad esempio possibile eseguire ricerche in dispositivi di archiviazione USB (Universal Serial Bus), dispositivi portatili che usano il protocollo MTP o un server File Transfer Protocol (FTP) tramite le origini dati della shell che consentono di accedere a tali sistemi di archiviazione. In questo modo si garantisce un'esperienza utente migliore.

In Windows Search è presente una cache di valori di proprietà utilizzata nell'implementazione di Windows servizio di ricerca (WSS). Questi valori di proprietà possono essere sottoposti a query a livello di codice tramite il provider di OLE DB di ricerca di Windows o tramite [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), che rappresenta gli elementi nei risultati della ricerca e nelle viste basate su query. Windows Search raccoglie e archivia le proprietà generate dai gestori di filtro o dai gestori di proprietà quando un elemento, ad esempio un documento di Word, viene indicizzato. Questo archivio viene eliminato e ricompilato quando l'indice viene ricompilato.

Gli sviluppatori di terze parti possono creare applicazioni che utilizzano i dati nell'indice tramite query a livello di codice e possono estendere i dati nell'indice per i tipi di file e di elemento personalizzati che devono essere indicizzati da ricerca di Windows. Se si desidera visualizzare i risultati della query in Esplora risorse, è necessario implementare un'origine dati della shell prima di poter creare un gestore di protocollo per estendere l'indice. Tuttavia, se tutte le query sono programmatiche (tramite OLE DB ad esempio) e interpretate dal codice dell'applicazione anziché dalla shell, uno spazio dei nomi della shell è ancora preferibile ma non obbligatorio.

Un gestore di protocollo è necessario per Windows per ottenere informazioni sul contenuto dei file, ad esempio elementi nei database o tipi di file personalizzati. Sebbene Windows Search possa indicizzare il nome e le proprietà del file, Windows non contiene informazioni sul contenuto del file. Di conseguenza, tali elementi non possono essere indicizzati o esposti nella shell di Windows. Implementando un gestore di protocollo personalizzato, è possibile esporre questi elementi. Per un elenco di gestori identificato dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in [Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md).

> [!Note]  
> Un'origine dati della shell è talvolta nota come estensione dello spazio dei nomi della shell. Un gestore è talvolta noto come estensione della shell o gestore di estensione della shell.

 

### <a name="user-interface"></a>Interfaccia utente

In Windows Vista e versioni successive, Windows Search è integrato in tutte le finestre di Esplora risorse di Windows per l'accesso immediato alla ricerca. Ciò consente agli utenti di cercare rapidamente i file e gli elementi in base al nome del file, alle proprietà e al contenuto full-text. I risultati possono anche essere filtrati ulteriormente per perfezionare la ricerca. Di seguito sono riportate alcune altre funzionalità di Windows Search:

-   Una casella di ricerca immediata in ogni finestra consente di filtrare immediatamente tutti gli elementi attualmente in visualizzazione. Le caselle di ricerca immediata vengono visualizzate nel menu Start per cercare programmi o file e nell'angolo superiore destro di tutte le finestre di Esplora risorse di Windows per filtrare i risultati mostrati. La ricerca immediata è integrata anche in altre funzionalità di Windows, ad esempio Windows Media Player, per trovare i file correlati.
-   I documenti possono essere contrassegnati con parole chiave per raggrupparli in base ai criteri personalizzati definiti dall'utente. I tag sono elementi di metadati assegnati dall'utente o dalle applicazioni per semplificare la ricerca di file in base alle parole chiave che potrebbero non essere nel nome o nel contenuto dell'elemento. Ad esempio, un set di immagini potrebbe essere contrassegnato come "Arizona Vacation 2009" per recuperare rapidamente in un secondo momento eseguendo una ricerca delle parole incluse.
-   Le intestazioni di colonna migliorate nelle visualizzazioni Esplora risorse consentono l'ordinamento e il raggruppamento di documenti in modi diversi. Ad esempio, i file possono essere ordinati in base al nome, alla data di modifica, al tipo, alle dimensioni e ai tag. I documenti possono anche essere raggruppati in base a una di queste proprietà e ogni gruppo può essere filtrato (nascosto o visualizzato) in base alle esigenze.
-   I documenti possono essere impilati in base al nome, alla data di modifica, al tipo, alle dimensioni e ai tag. Gli stack includono tutti i documenti con la proprietà specificata e che si trovano all'interno di qualsiasi sottocartella della cartella selezionata.
-   Le ricerche possono essere salvate (per poter essere recuperate in seguito) facendo clic sul pulsante **Salva ricerca** nel riquadro di ricerca in Esplora risorse. I risultati verranno ripopolati dinamicamente in base ai criteri originali quando viene aperta la ricerca salvata. Per istruzioni, vedere [salvare i risultati della ricerca](https://windows.microsoft.com/windows-vista/Save-your-search-results).
-   I gestori di anteprime e di anteprime consentono agli utenti di visualizzare in anteprima i documenti in Esplora risorse senza dover aprire l'applicazione che li ha creati.

## <a name="technical-prerequisites"></a>Prerequisiti tecnici

Prima di iniziare a leggere la documentazione di Windows Search SDK, è necessario avere una conoscenza di base dei concetti seguenti:

-   Come implementare un'origine dati della shell.
-   Modalità di implementazione di un gestore.
-   Come usare il codice nativo.

Un'origine dati della shell è un componente usato per estendere lo spazio dei nomi della shell ed esporre gli elementi in un archivio dati. In passato, l'origine dati della shell era denominata estensione dello spazio dei nomi della shell. Un gestore è un oggetto Component Object Model (COM) che fornisce la funzionalità per un elemento della shell. Per un elenco di gestori identificato dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in [Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md).

Per ulteriori informazioni sull'assembly di interoperabilità di Windows Search SDK per l'utilizzo di oggetti COM esposti da ricerca di Windows e altri programmi che utilizzano codice gestito, vedere [utilizzo del codice gestito con i dati della shell e Windows Search](-search-3x-wds-managed-code.md). Si noti tuttavia che i filtri, i gestori di proprietà e i gestori di protocollo devono essere scritti in codice nativo. Ciò è dovuto a potenziali problemi di controllo delle versioni di Common Language Runtime (CLR) con il processo di esecuzione di più componenti aggiuntivi. Gli sviluppatori che non hanno familiarità con C++ possono iniziare a usare il [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx) e [lo sviluppo di Windows Introduzione](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Download e contenuti dell'SDK

Oltre a soddisfare i requisiti tecnici elencati, è inoltre necessario scaricare il [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per ottenere le librerie di ricerca di Windows. Gli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contengono esempi di codice utili e un assembly di interoperabilità per lo sviluppo con codice gestito. Per ulteriori informazioni sull'utilizzo degli esempi di codice, vedere [esempi di codice di Windows Search](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Documentazione di Windows Search SDK

Il contenuto della documentazione di Windows Search SDK è il seguente:

-   [Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md)

    Vengono descritti gli scenari di sviluppo principali di Windows Search. Fornisce un elenco di gestori identificato dallo scenario di sviluppo che si sta tentando di ottenere, le linee guida per il programma di installazione del componente aggiuntivo e le note di implementazione.

-   [Guida per gli sviluppatori di Windows Search](-search-developers-guide-entry-page.md)

    Vengono fornite spiegazioni per la [gestione dell'indice](-search-3x-wds-mngidx-overview.md), l' [esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md), [l'estensione dell'indice e l'](-search-3x-wds-extidx-overview.md) [estensione delle risorse di lingua](extending-language-resources-in-windows-search.md).

-   [Informazioni di riferimento su Windows Search](-search-reference-entry-page.md)

    Vengono documentate le seguenti categorie di interfacce di ricerca di Windows: [gestori di protocollo](-search-protocol-handlers-interfaces-entry-page.md), [query](-search-querying-interfaces-entry-page.md), ambito di ricerca per [indicizzazione](-search-crawl-scope-interfaces-entry-page.md), [componenti aggiuntivi dati](-search-data-addins-interfaces-entry-page.md), [gestione degli indici](-search-index-mgt-interfaces-entry-page.md)e [notifiche](-search-notifications-interfaces-entry-page.md). La documentazione di riferimento include anche [costanti ed enumerazioni](-search-constants-and-enumerations-entry-page.md), [strutture](-search-structures-entry-page.md), [mapping di proprietà](-search-3x-wds-propertymappings.md)e il [formato di file di ricerca salvato](-search-savedsearchfileformat.md).

-   [Esempi di codice di Windows Search](-search-samples-ovw.md)

    Vengono descritti gli esempi di codice dell'API di ricerca disponibili.

-   [Ricerca federata in Windows](-search-federated-search-overview.md)

    Viene descritto il supporto di Windows 7 per la Federazione di ricerca negli archivi dati remoti tramite tecnologie OpenSearch che consentono agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse.

-   [Tecnologie di ricerca correlate](-search-3x-wds-sampleentry.md)

    Elenca le tecnologie correlate a Windows Search: ricerca aziendale, ricerca Enterprise di SharePoint e applicazioni legacy come Windows Desktop Search 2. x e Platform SDK: servizio di indicizzazione.

-   [Glossario di Windows Search](search-glossary.md)

    Definisce i termini essenziali usati nelle tecnologie Windows Search e Shell.

## <a name="history-of-windows-search"></a>Cronologia di Windows Search

Windows Search sostituisce Windows Desktop Search (WDS), disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. WDS ha sostituito il servizio di indicizzazione legacy dalle versioni precedenti di Windows con miglioramenti a prestazioni, usabilità ed estendibilità. La nuova piattaforma di sviluppo supporta i requisiti che producono un sistema più sicuro e stabile. Sebbene la nuova piattaforma di query non sia compatibile con Microsoft Windows Desktop Search (WDS) 2. x, i filtri e i gestori di protocollo scritti per le versioni precedenti di WDS possono essere aggiornati per funzionare con Windows Search. Windows Search supporta anche un nuovo sistema di proprietà. Per informazioni sui filtri, i gestori di proprietà e i gestori di protocollo, vedere [estensione dell'indice](-search-3x-wds-extidx-overview.md).

Windows Search è integrato in Windows Vista e versioni successive ed è disponibile come aggiornamento ridistribuibile di WDS 2. x per supportare i sistemi operativi seguenti:

-   versioni a 32 bit di Windows XP con Service Pack 2 (SP2).
-   Tutte le versioni basate su x64 di Windows XP.
-   Windows Server 2003 con Service Pack 1 (SP1) e versioni successive.
-   Tutte le versioni basate su x64 di Windows Server 2003.

Per eseguire applicazioni scritte per Windows Search, è necessario che nei sistemi che eseguono questi sistemi operativi sia installato Windows Search. Per ulteriori informazioni, vedere [l'articolo KB 917013: Descrizione di Windows desktop search 3,01 e il Multilingual User Interface Pack per Windows desktop search 3,01](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions//bb776815(v=vs.85)).
-   Per ulteriori informazioni su [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) e sull'origine dei dati della cartella del database, vedere la descrizione \_ della \_ costante Parse con \_ proprietà nelle [chiavi di stringa del contesto di binding](../shell/str-constants.md). Vedere anche [array di associazioni](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) e [IPropertySystem:: GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Per informazioni su OLE DB, vedere [Cenni preliminari sulla programmazione OLE DB](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019). Per informazioni sul provider di dati di .NET Framework per OLE DB, vedere la documentazione [dello spazio dei nomi System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) .
-   Per una panoramica dei gestori di tipi di file (noti anche come gestori di estensioni della shell e gestori di ricerca), vedere [Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md).
-   Per bacheche dei messaggi supportati dalla community sulle tecnologie di ricerca, vedere il [Forum MSDN relativo allo sviluppo per Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Per esempi di codice correlati, vedere [esempi di codice di Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Lingue supportate da Windows Search](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso di codice gestito con i dati della shell e Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
