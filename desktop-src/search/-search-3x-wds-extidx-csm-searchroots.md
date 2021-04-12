---
description: Gestione ambito ricerca per indicizzazione consente di aggiungere e rimuovere le radici di ricerca per gli archivi dati da e verso l'ambito di ricerca per indicizzazione di Windows Search.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Gestione delle radici di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225961"
---
# <a name="managing-search-roots"></a>Gestione delle radici di ricerca

Gestione ambito ricerca per indicizzazione consente di aggiungere e rimuovere le radici di ricerca per gli archivi dati da e verso l'ambito di ricerca per indicizzazione di Windows Search.

Vengono inoltre presentati gli argomenti seguenti:

-   [Informazioni sulle radici di ricerca](#about-search-roots)
-   [Prima di iniziare](#before-you-begin)
-   [Windows 7: nuova API di gestione degli ambiti di ricerca](#windows-7-new-crawl-scope-manager-api)
-   [Aggiunta di radici all'ambito di ricerca per indicizzazione](#adding-roots-to-the-crawl-scope)
-   [Rimozione delle radici dall'ambito della ricerca per indicizzazione](#removing-roots-from-the-crawl-scope)
-   [Enumerazione delle radici nell'ambito della ricerca per indicizzazione](#enumerating-roots-in-the-crawl-scope)
-   [Argomenti correlati](#related-topics)

 

## <a name="about-search-roots"></a>Informazioni sulle radici di ricerca

Una radice di ricerca definisce la base di uno spazio dei nomi della shell in cui è possibile includere o escludere ambiti specifici ed è in genere il contenitore di livello più alto in un protocollo che può essere enumerato. Non specifica quali parti dell'archivio devono essere indicizzate o meno. indica semplicemente che un archivio contenuto esiste ed è associato a un gestore di protocollo registrato. La sintassi per l'identificazione di un URL radice di ricerca include il protocollo, l'ID di sicurezza dell'archivio o dell'utente, il percorso e facoltativamente un elemento specifico (ad esempio un file). Negli esempi seguenti vengono illustrate due forme della sintassi per una radice di ricerca.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



Il <protocol> segmento deve essere seguito da due (2) barre ('/'), a meno che non sia il file: protocollo, che richiede tre barre (file:///). Il <site or SID> segmento rappresenta un archivio del contenuto o un identificatore di sicurezza utente se la radice di ricerca è destinata a essere specifica per l'utente. Il <path> segmento è un set di contenitori, ad esempio directory o cartelle, e può includere il carattere jolly " \* ". Il valore di <item> il segmento è facoltativo e può includere anche il carattere jolly " \* ". Se non si include un elemento, assicurarsi di terminare il segmento di percorso con una barra o l'indicizzatore presuppone che l'ultimo sottocontenitore sia un elemento.

Si supponga, ad esempio, di avere implementato un gestore di protocollo (myPH) per gestire i file di tipo \* . myext per un'applicazione personalizzata. Tutti questi file si trovano nella cartella WorkteamA \\ ProjectFiles in un computer locale. La radice di ricerca per potrebbe essere simile alla seguente:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Si supponga che si stia pianificando di includere tutti i file con estensione myext, ma non nient'altro da tale contenitore nell'indice. La radice di ricerca per potrebbe essere simile alla seguente:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* . myext.

I pattern con caratteri jolly definiscono gli URL usando il carattere jolly " \* " e sono considerati un modello anziché un URL, ma la terminologia viene spesso usata in modo intercambiabile. Ad esempio, file:///C: \\ \\ \* \\ i dati di NomeProgetto \\ corrisponderanno agli URL seguenti:

-   C: \\ ProjectA \\ **Version1** \\ dati\\
-   C: \\ ProjectA \\ **Version2** \\ dati\\

Ma tale modello non corrisponderà a questo URL:

-   C: \\ ProjectA \\ **Version1 \\ Temp** \\ Data\\

È necessario creare nuove radici di ricerca per i contenitori che non si trovano già nell'ambito della ricerca per indicizzazione dell'indicizzatore. Se il percorso C: \\ ParentScope è già incluso nell'ambito della ricerca per indicizzazione, non è necessario aggiungere una nuova radice di ricerca per C: \\ ParentScope ChildScope a meno che non \\ si sappia che l'ambito figlio è stato precedentemente escluso.

L'interfaccia utente per l'impostazione delle opzioni di ricerca di Windows Visualizza le radici di ricerca per gli utenti in modo che possano ridefinire le regole di ambito per le ricerche. Come parte del processo di installazione del gestore di protocollo personalizzato, del contenitore e/o dell'applicazione, è possibile definire un ambito di ricerca per indicizzazione predefinito, con regole di inclusione ed esclusione. Queste regole vengono presentate agli utenti finali come località. Gli utenti possono spostarsi tra le sottodirectory della radice di ricerca predefinita e selezionare quelle che desiderano includere nelle ricerche o deselezionare quelle che vogliono escludere.

 

## <a name="before-you-begin"></a>Prima di iniziare

Prima di poter usare una delle interfacce di gestione dell'ambito di ricerca per indicizzazione (CSM), è necessario eseguire i passaggi dei prerequisiti seguenti:

1.  Creare l'oggetto **CrawlSearchManager** e ottenere la relativa interfaccia [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
2.  Chiamare [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) per "SystemIndex" per ottenere un'istanza di un'interfaccia [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .
3.  Chiamare [**ISearchCatalogManager:: GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) per ottenere un'istanza dell'interfaccia [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .

Dopo aver apportato modifiche al gestore dell'ambito di ricerca per indicizzazione (CSM), è necessario chiamare [**ISearchCrawlScopeManager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall). Questo metodo non accetta parametri e restituisce \_ OK in seguito all'esito positivo.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: nuova API di gestione degli ambiti di ricerca

In **Windows 7 e versioni successive**, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende le funzionalità dell'interfaccia [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) . Il metodo [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) ottiene la versione CSM (Crawl scope Manager), che informa i client se lo stato del CSM è stato modificato. **ISearchCrawlScopeManager2:: GetVersion** non comporta una chiamata tra processi. Se la funzione ha esito positivo, il puntatore restituito rimane valido finché il client non chiama **UnmapViewOfFile** sull'indicatore di misura e **CloseHandle** sull'handle restituito.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Aggiunta di radici all'ambito di ricerca per indicizzazione

Il [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) indica al motore di ricerca i contenitori per la ricerca per indicizzazione e/o l'espressione di controllo e gli elementi in tali contenitori da includere o escludere. Per aggiungere una nuova radice di ricerca, creare un'istanza di un oggetto [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) , impostare gli attributi radice e quindi chiamare [**ISearchCrawlScopeManager:: AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) e passargli un puntatore all'oggetto **ISearchRoot** . L'URL della radice di ricerca ha lo stesso formato della radice di ricerca descritta in precedenza.

Nella tabella seguente vengono descritti i metodi put pertinenti per [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); gli altri metodi put dell'interfaccia non vengono attualmente usati da ricerca di Windows. Per una maggiore sicurezza, è consigliabile includere gli identificatori di sicurezza (SID) degli utenti in tutte le radici. Le radici per utente sono più sicure quando le query vengono eseguite in un processo per utente, assicurando che un utente non possa visualizzare gli elementi indicizzati dalla posta in arrivo di un altro utente, ad esempio.



| Metodo                     | Descrizione                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inserisci \_ ProvidesNotifications | Impostare su **true** se un gestore di protocollo o un'altra applicazione invierà una notifica al motore di ricerca delle modifiche apportate agli URL sotto la radice di ricerca. La notifica indica che è necessario eseguire la reindicizzazione degli URL. |
| Inserisci \_ RootURL               | Imposta l'URL radice della ricerca corrente. L'URL accetta il form radice di ricerca descritto in precedenza.                                                                                                      |



 

 

Per impostazione predefinita, l'indicizzatore non esegue la ricerca per indicizzazione in un ambito quando si aggiunge una radice di ricerca. È inoltre necessario aggiungere una regola di inclusione per la radice. Se si desidera aggiungere una radice specifica dell'utente per un'applicazione, l'applicazione deve aggiungere le radici appropriate per i nuovi utenti all'avvio dell'applicazione.

Per aggiungere le radici appropriate per i nuovi utenti:

1.  Ottenere il SID dell'utente.
2.  Enumerare tutte le radici per verificare se ne esiste uno per questo SID.
3.  Aggiungere una nuova radice, usando il SID, se necessario.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Rimozione delle radici dall'ambito della ricerca per indicizzazione

È possibile usare [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) per rimuovere una radice dall'ambito della ricerca per indicizzazione quando l'URL non è più necessario. La rimozione di una radice comporta anche l'eliminazione di tutte le regole di ambito per tale URL. Si supponga, ad esempio, di voler disinstallare un archivio del contenuto e/o il relativo gestore di protocollo da un sistema. È possibile disinstallare l'applicazione, rimuovere tutti i dati, quindi rimuovere la radice di ricerca dall'ambito della ricerca per indicizzazione e il gestore dell'ambito di ricerca per indicizzazione rimuoverà la radice e tutte le regole di ambito associate alla radice.

Per rimuovere una radice di ricerca esistente, chiamare [**ISearchCrawlScopeManager:: RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) con la radice di ricerca che si vuole rimuovere. L'URL della radice di ricerca ha lo stesso formato della radice di ricerca descritta in precedenza. Questo metodo restituisce \_ false se la radice non viene trovata e un codice di errore se si è verificato un errore durante la rimozione di una radice trovata.

La rimozione di una radice di ricerca consente inoltre di rimuovere l'URL dall'interfaccia utente per le opzioni di ricerca di Windows, in modo che gli utenti potrebbero non essere in grado di aggiungere nuovamente tale contenitore o percorso utilizzando l'interfaccia utente. È anche possibile rimuovere tutte le sostituzioni impostate dall'utente di una radice di ricerca e ripristinare le regole di ambito e radice di ricerca originali. Per ulteriori informazioni, vedere [gestione delle regole di ambito](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> In Windows Vista, se gli utenti vengono rimossi tramite profili utente nel pannello di controllo, CSM rimuove tutte le regole e le radici con il SID e rimuove gli elementi indicizzati dal catalogo. In Windows XP è necessario rimuovere manualmente le radici e le regole degli utenti.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerazione delle radici nell'ambito della ricerca per indicizzazione

CSM enumera le radici di ricerca usando un'interfaccia di enumeratore di tipo COM standard, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). È possibile usare questa interfaccia per enumerare le radici di ricerca per diversi scopi. Ad esempio, potrebbe essere necessario visualizzare l'intero ambito di ricerca per indicizzazione in un'interfaccia utente o scoprire se una particolare radice o l'elemento figlio di una radice è già presente nell'ambito della ricerca per indicizzazione.

 

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

[Utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Gestione delle regole di ambito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



