---
description: Informazioni su Windows Search consente di gestire l'indice Windows Search ricerca con Gestione ricerca, Gestione cataloghi e Gestione ambito ricerca per indicizzazione.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfacce per la gestione dell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120016"
---
# <a name="interfaces-for-managing-the-index"></a>Interfacce per la gestione dell'indice

Windows Search consente di gestire l'indice Windows Search con tre componenti principali: Gestione ricerca, Gestione catalogo e Gestione ambito ricerca per indicizzazione. Alcune di queste interfacce di gestione possono essere usate con privilegi utente standard, ma quelle che modificano lo stato dell'indice richiedono privilegi amministrativi.

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
<td>Gestione ricerca</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></td>
<td>Fornisce metodi per recuperare e impostare informazioni su Windows Search:
<ul>
<li>Recupero di un'istanza di Gestione cataloghi per un catalogo specifico.</li>
<li>Recupero o impostazione delle informazioni sul proxy.</li>
<li>Recupero di informazioni sulla versione del Windows Search di lavoro.</li>
</ul>
Per altre informazioni, vedere <a href="-search-3x-wds-mngidx-searchmanager.md">Uso di Gestione ricerca.</a><br/></td>
</tr>
<tr class="even">
<td>Gestione cataloghi</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Fornisce metodi per gestire un singolo catalogo di ricerca, ad esempio causando una nuova indicizzazione o l'impostazione di timeout. Questa interfaccia gestisce il catalogo in quattro aree:
<ul>
<li>Contenuto del catalogo: assicura che i nuovi dati siano indicizzati e che altri componenti e applicazioni funzionino correttamente forzando una nuova indicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.</li>
<li>Proprietà del catalogo: impostazione delle proprietà che determinano il modo in cui il catalogo gestisce i timeout durante la connessione ai gestori di protocollo e il modo in cui i contrassegni diacritici vengono gestiti nelle ricerche.</li>
<li>Stato del catalogo: recupero di informazioni sul catalogo, inclusi lo stato, le dimensioni e lo stato corrente dell'attività.</li>
<li>Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste dall'Gestione ambito ricerca per indicizzazione, dalle notifiche di modifica dei dati e <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>dall'interfaccia ISearchQueryHelper.</strong></a></li>
</ul>
Per altre informazioni, vedere <a href="-search-3x-wds-mngidx-catalog-manager.md">Uso di Gestione cataloghi.</a><br/></td>
</tr>
<tr class="odd">
<td>Gestione ambito ricerca per indicizzazione</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br/></td>
<td>Fornisce metodi per informare il motore di ricerca sui contenitori da ricercare o controllare e sugli elementi in tali contenitori da includere o escludere nell'indice. È anche possibile eseguire una query sul Gestione ambito ricerca per indicizzazione per verificare se un URL specifico si trova nell'ambito della ricerca per indicizzazione. Per altre informazioni, vedere <a href="-search-3x-wds-extidx-csm.md">Using the Gestione ambito ricerca per indicizzazione</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Argomenti correlati

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)

[Uso di Gestione ricerca](-search-3x-wds-mngidx-searchmanager.md)

[Uso di Gestione cataloghi](-search-3x-wds-mngidx-catalog-manager.md)

[Uso del Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
