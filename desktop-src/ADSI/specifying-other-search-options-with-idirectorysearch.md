---
title: Specifica di altre opzioni di ricerca con IDirectorySearch
description: L'interfaccia IDirectorySearch fornisce un controllo aggiuntivo sul modo in cui viene eseguita la ricerca tramite l'utilizzo delle opzioni di ricerca.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Specifica di altre opzioni di ricerca con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955080"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Specifica di altre opzioni di ricerca con IDirectorySearch

L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce un controllo aggiuntivo sul modo in cui viene eseguita la ricerca tramite l'utilizzo delle opzioni di ricerca. Queste opzioni di ricerca vengono impostate compilando una matrice di [**inserzioni \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Structures e chiamando il metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Per altre informazioni, vedere i seguenti argomenti:

-   [Utilizzo del metodo SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Ricerche sincrone e asincrone con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paging con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Caching dei risultati con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Esecuzione di una query sull'ambito degli attributi](performing-an-attribute-scoped-query.md)
-   [Ordinamento dei risultati della ricerca con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Inseguimento dei riferimenti con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Limite dimensioni con IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Limite di tempo del server con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Limite di tempo client con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Restituzione solo dei nomi di attributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




