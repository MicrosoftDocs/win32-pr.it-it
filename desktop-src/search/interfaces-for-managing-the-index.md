---
description: "Windows Search consente di gestire l'indice di ricerca di Windows con tre componenti principali: Search Manager, Catalog Manager e Crawl scope Manager."
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfacce per la gestione dell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225945"
---
# <a name="interfaces-for-managing-the-index"></a>Interfacce per la gestione dell'indice

Windows Search consente di gestire l'indice di ricerca di Windows con tre componenti principali: Search Manager, Catalog Manager e Crawl scope Manager. Alcune di queste interfacce di gestione possono essere utilizzate con privilegi utente standard, ma quelle che modificano lo stato dell'indice richiedono privilegi amministrativi.

## <a name="about-the-interfaces-for-managing-the-index"></a>Informazioni sulle interfacce per la gestione dell'indice

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Interfacce</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gestione ricerche</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></td>
<td>Fornisce metodi per recuperare e impostare informazioni su ricerca di Windows:
<ul>
<li>Recupero di un'istanza di gestione catalogo per un catalogo specifico.</li>
<li>Recupero o impostazione delle informazioni sul proxy.</li>
<li>Recupero delle informazioni sulla versione del motore di ricerca di Windows.</li>
</ul>
Per ulteriori informazioni, vedere <a href="-search-3x-wds-mngidx-searchmanager.md">utilizzo di Search Manager</a>.<br/></td>
</tr>
<tr class="even">
<td>Gestione cataloghi</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Fornisce metodi per la gestione di un singolo catalogo di ricerca, ad esempio la causa di una nuova indicizzazione o l'impostazione di timeout. Questa interfaccia gestisce il catalogo in quattro aree:
<ul>
<li>Contenuto del catalogo: garantire che i nuovi dati vengano indicizzati e che le applicazioni e i componenti funzionino correttamente forzando la reindicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.</li>
<li>Proprietà catalogo-impostazione proprietà che determinano il modo in cui il catalogo gestisce i timeout quando ci si connette ai gestori di protocollo e come vengono trattati i segni diacritici nelle ricerche.</li>
<li>Stato del catalogo: ottenere informazioni sul catalogo, tra cui lo stato, le dimensioni e lo stato dell'attività corrente.</li>
<li>Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste da gestione dell'ambito di ricerca per indicizzazione, notifiche delle modifiche dei dati e interfaccia <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</li>
</ul>
Per ulteriori informazioni, vedere <a href="-search-3x-wds-mngidx-catalog-manager.md">utilizzo di gestione catalogo</a>.<br/></td>
</tr>
<tr class="odd">
<td>Gestione ambito ricerca per indicizzazione</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br/></td>
<td>Fornisce metodi per informare il motore di ricerca sui contenitori per eseguire la ricerca per indicizzazione o l'espressione di controllo e gli elementi in tali contenitori da includere o escludere nell'indice. È anche possibile eseguire una query su Gestione ambito ricerca per verificare se un particolare URL si trova nell'ambito della ricerca per indicizzazione. Per ulteriori informazioni, vedere <a href="-search-3x-wds-extidx-csm.md">utilizzo di gestione ambito indicizzazione</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Argomenti correlati

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)

[Utilizzo di gestione ricerche](-search-3x-wds-mngidx-searchmanager.md)

[Utilizzo di gestione cataloghi](-search-3x-wds-mngidx-catalog-manager.md)

[Utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
