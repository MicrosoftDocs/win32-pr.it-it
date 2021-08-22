---
description: Il Gestione ambito ricerca per indicizzazione (CSM) consente di aggiungere e rimuovere le radici di ricerca per gli archivi dati da e verso l'ambito Windows ricerca per indicizzazione.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Gestione delle radici di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758d3c10a4c69f336202274cd1fb40528848b0ddb431fd58646cf700d2b2d736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095288"
---
# <a name="managing-search-roots"></a>Gestione delle radici di ricerca

Il Gestione ambito ricerca per indicizzazione (CSM) consente di aggiungere e rimuovere le radici di ricerca per gli archivi dati da e verso l'ambito Windows ricerca per indicizzazione.

Vengono inoltre presentati gli argomenti seguenti:

-   [Informazioni sulle radici di ricerca](#about-search-roots)
-   [Prima di iniziare](#before-you-begin)
-   [Windows 7: Nuova API Gestione ambito ricerca per indicizzazione](#windows-7-new-crawl-scope-manager-api)
-   [Aggiunta di radici all'ambito di ricerca per indicizzazione](#adding-roots-to-the-crawl-scope)
-   [Rimozione delle radici dall'ambito di ricerca per indicizzazione](#removing-roots-from-the-crawl-scope)
-   [Enumerazione delle radici nell'ambito della ricerca per indicizzazione](#enumerating-roots-in-the-crawl-scope)
-   [Argomenti correlati](#related-topics)

 

## <a name="about-search-roots"></a>Informazioni sulle radici di ricerca

Una radice di ricerca definisce la base di uno spazio dei nomi shell in cui è possibile includere o escludere ambiti specifici ed è in genere il contenitore di livello più alto in un protocollo che può essere enumerato. Non specifica quali parti di questo archivio devono o non devono essere indicizzate. indica semplicemente che un archivio di contenuto esiste ed è associato a un gestore di protocollo registrato. La sintassi per identificare un URL radice di ricerca include il protocollo, l'identificatore di sicurezza dell'archivio o dell'utente, il percorso e facoltativamente un elemento specifico ,ad esempio un file. Gli esempi seguenti illustrano due forme della sintassi per una radice di ricerca.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



Il segmento deve essere seguito da due (2) barre ('/') a meno che non sia il file: protocollo, che richiede tre barre <protocol> (file:///). Il segmento rappresenta un archivio contenuto o un identificatore di sicurezza utente se la radice di ricerca deve <site or SID> essere specifica dell'utente. Il <path> segmento è un set di contenitori, ad esempio directory o cartelle, e può includere il carattere jolly ' \* '. The <item> segment è facoltativo e può includere anche il carattere jolly ' \* '. Se non si include un elemento, assicurarsi di completare il segmento di percorso con una barra oppure l'indicizzatore presuppone che l'ultimo sottocontenitore sia un elemento.

Si supponga, ad esempio, di aver implementato un gestore di protocollo (myPH) per gestire file di tipo \* .myext per un'applicazione personalizzata. Tutti questi file si trovano nella cartella WorkteamA \\ ProjectFiles in un computer locale. La radice di ricerca potrebbe essere simile alla seguente:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Si supponga di voler includere nell'indice tutti i file con estensione myext, ma nessun altro elemento di tale contenitore. La radice di ricerca potrebbe essere simile alla seguente:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* .myext.

I modelli con caratteri jolly definiscono gli URL usando il carattere jolly ' ' e sono considerati un modello anziché un URL, ma la terminologia viene spesso usata \* in modo intercambiabile. Ad esempio, file:///C: \\ i dati projectA \\ \* \\ \\ corrispondono agli URL seguenti:

-   C: \\ Dati di ProjectA versione \\ **1** \\\\
-   C: \\ Dati di ProjectA versione \\ **2** \\\\

Tale modello, tuttavia, non corrisponde a questo URL:

-   C: \\ Dati temporanei di ProjectA versione \\ **1 \\** \\\\

È necessario creare nuove radici di ricerca per i contenitori che non sono già presenti nell'ambito di ricerca per indicizzazione dell'indicizzatore. Se il percorso C: ParentScope è già incluso nell'ambito della ricerca per indicizzazione, non è necessario aggiungere una nuova radice di ricerca per C: ParentScope ChildScope a meno che non si sappia che l'ambito figlio è stato precedentemente \\ \\ \\ escluso.

L'interfaccia utente per l'impostazione Windows opzioni di ricerca visualizza le radici di ricerca per gli utenti in modo che possano perfezionare le regole di ambito per le ricerche. Come parte del processo di installazione per il gestore di protocollo personalizzato, il contenitore e/o l'applicazione, è possibile definire un ambito di ricerca per indicizzazione predefinito, con regole di inclusione ed esclusione. Queste regole vengono presentate agli utenti finali come località. Gli utenti possono spostarsi all'interno delle sottodirectory della radice di ricerca predefinita e selezionare quelli che vogliono includere nelle ricerche o cancellare quelli che vogliono escludere.

 

## <a name="before-you-begin"></a>Prima di iniziare

Prima di poter usare una qualsiasi delle interfacce Gestione ambito ricerca per indicizzazione (CSM), è necessario eseguire i passaggi dei prerequisiti seguenti:

1.  Creare **l'oggetto CrawlSearchManager** e ottenere la [**relativa interfaccia ISearchManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)
2.  Chiamare [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) per "SystemIndex" per ottenere un'istanza di [**un'interfaccia ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)
3.  Chiamare [**ISearchCatalogManager::GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) per ottenere un'istanza [**dell'interfaccia ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

Dopo aver apportato modifiche al Gestione ambito ricerca per indicizzazione (CSM), è necessario chiamare [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall). Questo metodo non accetta parametri e restituisce S \_ OK in caso di esito positivo.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: Nuova API Gestione ambito ricerca per indicizzazione

In **Windows 7 e versioni successive,** [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende la funzionalità dell'interfaccia [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Il [**metodo ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) ottiene la versione di Gestione ambito ricerca per indicizzazione (CSM), che informa i client se lo stato del CSM è stato modificato. **ISearchCrawlScopeManager2::GetVersion** non comporta una chiamata tra processi. Se la funzione ha esito positivo, il puntatore restituito rimane valido fino a quando il client non chiama **UnmapViewOfFile** sul puntatore e **CloseHandle** sull'handle restituito.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Aggiunta di radici all'ambito di ricerca per indicizzazione

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) indica al motore di ricerca i contenitori da sottoporsi a ricerca per indicizzazione e/o controllare e gli elementi in tali contenitori da includere o escludere. Per aggiungere una nuova radice di ricerca, creare un'istanza di un oggetto [**ISearchRoot,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) impostare gli attributi radice e quindi chiamare [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) e passarlo a un puntatore all'oggetto **ISearchRoot.** L'URL radice di ricerca ha lo stesso formato della radice di ricerca descritta in precedenza.

Nella tabella seguente vengono descritti i metodi put pertinenti per [**ISearchRoot.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) Gli altri metodi put dell'interfaccia non vengono attualmente usati da Windows ricerca. È consigliabile includere gli identificatori di sicurezza (SID) degli utenti in tutte le radici per una maggiore sicurezza. Le radici per utente sono più sicure perché le query vengono eseguite in un processo per utente, assicurando che un utente non possa visualizzare gli elementi indicizzati dalla posta in arrivo di un altro utente, ad esempio.



| Metodo                     | Descrizione                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | Impostare su **TRUE se** un gestore di protocollo o un'altra applicazione invierà una notifica al motore di ricerca in caso di modifiche agli URL nella radice di ricerca. La notifica indica che è necessario reindicizzare gli URL. |
| put \_ RootURL               | Imposta l'URL radice della ricerca corrente. L'URL assume il formato radice di ricerca descritto in precedenza.                                                                                                      |



 

 

Per impostazione predefinita, l'indicizzatore non esegue la ricerca per indicizzazione di un ambito quando si aggiunge una radice di ricerca. È anche necessario aggiungere una regola di inclusione per la radice. Se si vuole aggiungere una radice specifica dell'utente per un'applicazione, tale applicazione deve aggiungere le radici appropriate per i nuovi utenti all'avvio dell'applicazione.

Per aggiungere le radici appropriate per i nuovi utenti:

1.  Ottenere il SID dell'utente.
2.  Enumerare tutte le radici per verificare se ne esiste una per questo SID.
3.  Aggiungere una nuova radice usando il SID, se necessario.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Rimozione delle radici dall'ambito di ricerca per indicizzazione

È possibile usare [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) per rimuovere una radice dall'ambito della ricerca per indicizzazione quando non si vuole più indicizzare l'URL. La rimozione di una radice elimina anche tutte le regole di ambito per tale URL. Si supponga, ad esempio, di voler disinstallare un archivio contenuto e/o il relativo gestore di protocollo da un sistema. È possibile disinstallare l'applicazione, rimuovere tutti i dati e quindi rimuovere la radice di ricerca dall'ambito della ricerca per indicizzazione e il Gestione ambito ricerca per indicizzazione rimuoverà la radice e tutte le regole di ambito associate alla radice.

Per rimuovere una radice di ricerca esistente, chiamare [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) con la radice di ricerca da rimuovere. L'URL radice di ricerca ha lo stesso formato della radice di ricerca descritta in precedenza. Questo metodo restituisce S FALSE se la radice non viene trovata e un codice di errore se si è verificato un errore durante la rimozione di una radice \_ trovata.

La rimozione di una radice di ricerca rimuove anche l'URL dall'interfaccia utente per le opzioni di ricerca Windows, pertanto gli utenti potrebbero non essere in grado di aggiungere nuovamente il contenitore o il percorso usando l'interfaccia utente. È anche possibile rimuovere tutte le sostituzioni impostate dall'utente di una radice di ricerca e ripristinare la radice di ricerca originale e le regole di ambito. Per altre informazioni, vedere [Gestione delle regole di ambito](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> In Windows Vista, se gli utenti vengono rimossi tramite profili utente in Pannello di controllo, CSM rimuove tutte le regole e le radici con il SID e rimuove gli elementi indicizzati dal catalogo. In Windows XP è necessario rimuovere manualmente le radici e le regole degli utenti.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerazione delle radici nell'ambito della ricerca per indicizzazione

Il CSM enumera le radici di ricerca usando un'interfaccia enumeratore di tipo COM standard, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). È possibile usare questa interfaccia per enumerare le radici di ricerca per diversi scopi. Ad esempio, potrebbe essere necessario visualizzare l'intero ambito di ricerca per indicizzazione in un'interfaccia utente o scoprire se una determinata radice o l'elemento figlio di una radice si trova già nell'ambito della ricerca per indicizzazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso dell'Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Gestione delle regole di ambito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



