---
description: L'interfaccia ISearchManager fornisce metodi che consentono di apportare modifiche tra cataloghi.
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: Utilizzo di gestione ricerche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966541"
---
# <a name="using-the-search-manager"></a>Utilizzo di gestione ricerche

L'interfaccia [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) fornisce metodi che consentono di apportare modifiche tra cataloghi. Le modifiche apportate a livello di **ISearchManager** si applicano globalmente a tutti i cataloghi utilizzati dall'indicizzatore, mentre le modifiche apportate a livello di [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) si applicano a cataloghi specifici. Attualmente, tuttavia, Windows Search usa un solo catalogo, SystemIndex. È possibile utilizzare la gestione ricerca per eseguire le operazioni seguenti:

- Ottenere un'istanza di gestione catalogo per il catalogo di ricerca.
- Ottenere informazioni sulla versione del motore di ricerca di Windows.

I metodi dell'interfaccia [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) seguenti consentono di gestire i cataloghi di ricerca:

| Metodo                                                                      | Descrizione                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | Ottiene un catalogo in base al nome e restituisce un'istanza di [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) per il catalogo. In questo modo è possibile gestire un singolo catalogo di ricerca.                                          |
| [**GetIndexerVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | Restituisce la versione dell'indicizzatore in due Integer: versione principale e versione secondaria. Ad esempio, il numero di versione principale per Windows 10 Search è "10" e il numero di versione secondario è "0". Per Windows Vista Search e Windows Search 3,0 in Windows XP il numero di versione principale è "3" e il numero di versione secondario è "0". |
| [**GetIndexerVersionStr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | Restituisce il numero di versione completo dell'indicizzatore come stringa: ad esempio, "10.0.18309.1000". Per Windows 10 questo corrisponde in genere al numero di versione del sistema operativo. Per Windows XP, vista e 7, sarà diverso.                                                                                                                                        |


Per ulteriori informazioni su questi metodi, vedere la documentazione di [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .

I metodi [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) seguenti sono riservati per un uso futuro. Sono, tuttavia, implementati e non influiscono sull'indicizzatore o sul catalogo, in quanto è attualmente disponibile un solo catalogo per Windows Search.

- **Ottieni \_ bypass**
- **ottenere \_ LocalBypass**
- **ottenere \_ NumeroPorta**
- **ottenere \_ ProxyName**
- **ottenere \_ UseProxy**
- **Ottieni \_ UserAgent**
- **Inserisci \_ UserAgent**
- **SetProxy**

**GetParameter** e **separameter** sono riservati anche per usi futuri, ma non sono implementati.

## <a name="related-topics"></a>Argomenti correlati

[Gestione dell'indice](-search-3x-wds-mngidx-overview.md)

[Interfacce per la gestione dell'indice](interfaces-for-managing-the-index.md)

[Utilizzo di gestione cataloghi](-search-3x-wds-mngidx-catalog-manager.md)

[Utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md)
