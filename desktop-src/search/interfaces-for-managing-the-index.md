---
description: Informazioni su Windows ricerca consente di gestire l'indice Windows ricerca con Gestione ricerca, Gestione catalogo e Gestione ambito ricerca per indicizzazione.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfacce per la gestione dell'indice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505752cc496d55057eece87bd673b31a323c6597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476797"
---
# <a name="interfaces-for-managing-the-index"></a>Interfacce per la gestione dell'indice

Windows La ricerca consente di gestire l'Windows di ricerca con tre componenti principali: Gestione ricerca, Gestione cataloghi e Gestione ambito ricerca per indicizzazione. Alcune di queste interfacce di gestione possono essere usate con privilegi utente standard, ma quelle che modificano lo stato dell'indice richiedono privilegi amministrativi.

## <a name="about-the-interfaces-for-managing-the-index"></a>Informazioni sulle interfacce per la gestione dell'indice


| Componente | Interfacce | Descrizione | 
|-----------|------------|-------------|
| Gestione ricerca | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a> | Fornisce metodi per recuperare e impostare le informazioni Windows ricerca:<ul><li>Recupero di un'istanza di Gestione cataloghi per un catalogo specifico.</li><li>Recupero o impostazione delle informazioni sul proxy.</li><li>Recupero di informazioni sulla versione del Windows di ricerca.</li></ul>Per altre informazioni, vedere <a href="-search-3x-wds-mngidx-searchmanager.md">Uso di Gestione ricerca.</a><br /> | 
| Gestione catalogo | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br /> | Fornisce metodi per gestire un singolo catalogo di ricerca, ad esempio causando una nuova indicizzazione o l'impostazione di timeout. Questa interfaccia gestisce il catalogo in quattro aree:<ul><li>Contenuto del catalogo: assicura che i nuovi dati siano indicizzati e che altri componenti e applicazioni funzionino correttamente forzando una nuova indicizzazione di tutto o parte del catalogo o reimpostando l'intero catalogo.</li><li>Proprietà del catalogo: impostazione di proprietà che determinano il modo in cui il catalogo gestisce i timeout durante la connessione ai gestori di protocollo e il modo in cui i contrassegni diacritici vengono gestiti nelle ricerche.</li><li>Stato del catalogo: recupero di informazioni sul catalogo, inclusi lo stato, le dimensioni e lo stato dell'attività corrente.</li><li>Accesso ad altre interfacce: recupero di altre interfacce correlate alla ricerca richieste dall'Gestione ambito ricerca per indicizzazione, dalle notifiche di modifica dei dati e <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>dall'interfaccia ISearchQueryHelper.</strong></a></li></ul>Per altre informazioni, vedere <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.<br /> | 
| Gestione ambito ricerca per indicizzazione | <a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br /><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br /> | Fornisce metodi per informare il motore di ricerca sui contenitori da ricercare o controllare e sugli elementi in tali contenitori da includere o escludere nell'indice. È anche possibile eseguire una query sul Gestione ambito ricerca per indicizzazione per verificare se un URL specifico si trova nell'ambito della ricerca per indicizzazione. Per altre informazioni, vedere <a href="-search-3x-wds-extidx-csm.md">Using the Gestione ambito ricerca per indicizzazione</a>.<br /> | 


## <a name="related-topics"></a>Argomenti correlati

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)

[Uso di Gestione ricerca](-search-3x-wds-mngidx-searchmanager.md)

[Uso di Gestione cataloghi](-search-3x-wds-mngidx-catalog-manager.md)

[Uso del Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
