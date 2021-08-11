---
title: Specifica di altre opzioni di ricerca con IDirectorySearch
description: L'interfaccia IDirectorySearch offre un controllo aggiuntivo sul modo in cui viene eseguita la ricerca tramite l'uso delle opzioni di ricerca.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Specifica di altre opzioni di ricerca con IDirectorySearch ADSI
- ADSI, Ricerca, IDirectorySearch, altre opzioni di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67105d9716934c8c7d1d56193ca0cdfde5f6a4bc4c32605420513dc62700d8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178766"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Specifica di altre opzioni di ricerca con IDirectorySearch

[**L'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) offre un controllo aggiuntivo sul modo in cui viene eseguita la ricerca tramite l'uso delle opzioni di ricerca. Queste opzioni di ricerca vengono impostate compilando una matrice di strutture [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e chiamando il [**metodo IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Per altre informazioni, vedere i seguenti argomenti:

-   [Uso del metodo SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Ricerche sincrone e asincrone con IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Paging con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Risultati Caching con IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Esecuzione di una query di ambito degli attributi](performing-an-attribute-scoped-query.md)
-   [Ordinamento dei risultati della ricerca con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Ricerca delle segnalazioni con IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Limite di dimensioni con IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Limite di tempo del server con IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Limite di tempo del client con IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Restituzione solo di nomi di attributi con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




