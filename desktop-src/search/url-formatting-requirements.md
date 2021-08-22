---
description: A Windows 7, le incoerenze rimangono nella gestione e nell'analisi degli URL. Questo argomento fornisce una guida limitata all'esplorazione delle incoerenze nei formati di URL di file.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Requisiti di formattazione url
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1bb413501548922eaf1b60801b6d35495d7f8a37dc743675052d4e0e5bae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462233"
---
# <a name="url-formatting-requirements"></a>Requisiti di formattazione url

A Windows 7, le incoerenze rimangono nella gestione e nell'analisi degli URL. Questo argomento fornisce una guida limitata all'esplorazione delle incoerenze nei formati di URL di file.

Questo argomento è organizzato come segue:

-   [Formati URL in uso](#url-formats-in-use)
-   [Direzione barra, stella finale e sensibilità barra finale](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formati url per API e query](#url-formats-by-api-and-query)
-   [Argomenti correlati](#related-topics)

## <a name="url-formats-in-use"></a>Formati URL in uso

I protocolli di terze parti sono responsabili della definizione del formato dell'URL e della definizione delle query in modo conforme allo standard. Ad esempio, Microsoft Outlook i nomi di cartella con caratteri arbitrari, inclusi quelli non validi negli URL, ad esempio il `"?"` carattere . Il gestore del protocollo MAPI esegue la propria codifica URL degli URL. Di conseguenza, l'indice archivia anziché e Outlook necessario prendere in considerazione questo valore `"%3F"` durante la creazione di `"?"` query.

I diversi formati sono elencati nella tabella seguente e a ognuno viene assegnato un identificatore di lettera a cui fare riferimento più avanti in questo argomento.



| ID  | URL del file locale o remoto | Esempio                     |
|-----|--------------------------|-----------------------------|
| A   | Locale                    | file:///c: esempio \\ di \\ test\\ |
| B   | Locale                    | file:c:/test/example/       |
| C   | Locale                    | c: \\ esempio di \\ test\\         |
| D   | Remoto                   | file:/// condivisione \\ \\ server \\\\ |
| E   | Remoto                   | file://server/share/        |
| F   | Remoto                   | \\\\condivisione \\ server\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Direzione barra, stella finale e sensibilità barra finale

In Windows ricerca non esiste in gran parte alcuna sensibilità alla direzione della barra. Se il formato viene accettato, viene accettato anche `c:\test\example` c:/test/example. Tuttavia, sebbene [SCOPE](-search-sql-folderdepth.md) non sia in genere sensibile alla direzione della barra, è sensibile alla direzione della barra nel caso del formato URL remoto F. Di conseguenza, `Scope = '//server/share'` non funziona.

L'unica API sensibile alle stelle finali e che distingue tra `c:\test\ ` `c:\test\*` e è [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Se è presente una regola di esclusione `c:\test\*` per , la directory url stessa verrà comunque `c:\test` indicizzata. Tuttavia, se l'URL di esclusione `c:\test\` è , la directory `c:\test` dell'URL non verrà indicizzata.

Esistono due posizioni in cui Windows ricerca è sensibile alle barre finali: query ItemUrl e Path. Se è presente una directory , Windows ricerca considera in `c:\test` modo diverso da per i `c:\test\` `c:\test` predicati come e `path = 'c:\test'` `System.ItemUrl = 'c:\test'` . Ad esempio, il predicato corrisponderebbe alla directory , ma non a causa `path='file:c:/test'` `c:\test` della barra `path='file:c:/test/'` finale.

## <a name="url-formats-by-api-and-query"></a>Formati url per API e query

Nella tabella seguente sono elencati i formati di URL di file locali accettati dalle API e dalle query selezionate. I formati sono associati a una lettera (da A a F), il cui significato è stato denotato nella sezione "[Formati URL in](#url-formats-in-use)Uso " più indietro in questo argomento.



| API o query                                                                                                    | Formatta A | Formato B | Formato C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | S        | N        | S        |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | S        | S        | S        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | S        | S        | S        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | S        | N        | N        |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | S        | S        | S        |
| Scope=                                                                                                          | N        | S        | S        |
| Directory=                                                                                                      | N        | S        | S        |
| ItemUrl=                                                                                                        | N        | S        | S        |
| Path=                                                                                                           | N        | S        | S        |



 

Nella tabella seguente sono elencati i formati di URL di file remoti accettati dalle query selezionate.



| Query                                                                                                           | Formato D | Formato E | Formato F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/D      | N/D      | N/D      |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/D      | N/D      | N/D      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/D      | N/D      | N/D      |
| Scope=                                                                                                          | S        | S        | S        |
| Directory=                                                                                                      | S        | S        | S        |
| ItemUrl=                                                                                                        | S        | S        | S        |
| Path=                                                                                                           | S        | S        | S        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi inclusi nell'indice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di indicizzazione nella Windows ricerca](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di query nella Windows ricerca](querying-process--windows-search-.md)
</dt> <dt>

[Processo di notifica nella Windows ricerca](-search-3x-wds-support.md)
</dt> </dl>

 

 
