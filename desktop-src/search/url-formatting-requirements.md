---
description: A partire da Windows 7, le incoerenze rimangono nella gestione e nell'analisi degli URL. Questo argomento fornisce una guida limitata all'esplorazione delle incoerenze nei formati di URL di file.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Requisiti per la formattazione degli URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08d7945578118f4d3103f44e6da60b96022e472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525440"
---
# <a name="url-formatting-requirements"></a>Requisiti per la formattazione degli URL

A partire da Windows 7, le incoerenze rimangono nella gestione e nell'analisi degli URL. Questo argomento fornisce una guida limitata all'esplorazione delle incoerenze nei formati di URL di file.

Questo argomento è organizzato nel modo seguente:

-   [Formati URL in uso](#url-formats-in-use)
-   [Direzione barra, stella finale e sensibilità barra finale](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formati URL per API e query](#url-formats-by-api-and-query)
-   [Argomenti correlati](#related-topics)

## <a name="url-formats-in-use"></a>Formati URL in uso

I protocolli di terze parti sono responsabili della definizione del formato URL e della definizione delle query in modo conforme allo standard. Microsoft Outlook, ad esempio, supporta i nomi di cartella con caratteri arbitrari, inclusi quelli non validi in URL come il `"?"` carattere. Il gestore del protocollo MAPI esegue la propria codifica URL degli URL. Di conseguenza, l'indice Archivia `"%3F"` invece di `"?"` e Outlook deve tenere conto di questo durante la creazione di query.

Nella tabella seguente sono elencati i diversi formati a cui viene assegnato un identificatore di lettera per fare riferimento a tali formati più avanti in questo argomento.



| ID  | URL del file locale o remoto | Esempio                     |
|-----|--------------------------|-----------------------------|
| A   | Locale                    | file:///c: \\ esempio di test \\\\ |
| B   | Locale                    | file: c:/test/example/       |
| C   | Locale                    | c: \\ esempio di test \\\\         |
| D   | Remoto                   | \\ \\ condivisione server \\ file:///\\ |
| E   | Remoto                   | file://server/share/        |
| F   | Remoto                   | \\\\\\condivisione server\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Direzione barra, stella finale e sensibilità barra finale

In Windows Search non esiste alcuna sensibilità alla barra di direzione. Se il formato `c:\test\example` è accettato, viene accettato anche c:/test/example. Tuttavia, anche se l' [ambito](-search-sql-folderdepth.md) non è generalmente sensibile alla barra, è sensibile alla direzione della barra nel caso del formato URL remoto F. di conseguenza, non `Scope = '//server/share'` funziona.

L'unica API sensibile alle stelle finali e distingue tra `c:\test\ ` e `c:\test\*` è [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager). Se è presente una regola di esclusione per `c:\test\*` , la directory URL `c:\test` stessa verrà ancora indicizzata. Tuttavia, se l'URL di esclusione è `c:\test\` , la directory URL `c:\test` non verrà indicizzata.

Esistono due posizioni in cui Windows Search è sensibile alle barre finali: ItemUrl e Path queries. Se è presente una directory `c:\test` , la ricerca di Windows viene trattata in `c:\test\` modo diverso rispetto `c:\test` a per i predicati come `path = 'c:\test'` e `System.ItemUrl = 'c:\test'` . Il predicato, ad esempio, `path='file:c:/test'` corrisponderebbe alla directory `c:\test` , ma `path='file:c:/test/'` non a causa della barra finale.

## <a name="url-formats-by-api-and-query"></a>Formati URL per API e query

Nella tabella seguente sono elencati i formati URL dei file locali accettati dalle query e dalle API selezionate. I formati sono associati a una lettera (da A A F), il cui significato è stato indicato nella sezione "[formati di URL in uso](#url-formats-in-use)" riportata in precedenza in questo argomento.



| API o query                                                                                                    | Formattare un | Formato B | Formato C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | S        | N        | S        |
| [**IGatherNotifyInline:: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | S        | S        | S        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | S        | S        | S        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | S        | N        | N        |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | S        | S        | S        |
| Ambito =                                                                                                          | N        | S        | S        |
| Directory =                                                                                                      | N        | S        | S        |
| ItemUrl =                                                                                                        | N        | S        | S        |
| Percorso =                                                                                                           | N        | S        | S        |



 

Nella tabella seguente sono elencati i formati URL file remoti accettati dalle query selezionate.



| Query                                                                                                           | Formato D | Formato E | Formato F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/D      | N/D      | N/D      |
| [**IGatherNotifyInline:: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/D      | N/D      | N/D      |
| Ambito =                                                                                                          | S        | S        | S        |
| Directory =                                                                                                      | S        | S        | S        |
| ItemUrl =                                                                                                        | S        | S        | S        |
| Percorso =                                                                                                           | S        | S        | S        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenuto dell'indice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di indicizzazione in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Esecuzione di query sul processo in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Processo di notifica in Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
