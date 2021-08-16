---
title: Risultati Caching con IDirectorySearch
description: La preferenza ADS \_ SEARCHPREF \_ CACHE RESULTS memorizza nella cache il set di risultati nel \_ client.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Risultati Caching con IDirectorySearch ADSI
- ADSI, Ricerca, IDirectorySearch, Altre opzioni di ricerca, Risultati Caching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838857"
---
# <a name="result-caching-with-idirectorysearch"></a>Risultati Caching con IDirectorySearch

La **preferenza ADS \_ SEARCHPREF \_ CACHE \_ RESULTS** memorizza nella cache il set di risultati nel client. La memorizzazione nella cache dei risultati consente a un'applicazione di mantenere un set di risultati recuperato e di scorrere nuovamente le righe recuperate. Abilita anche il supporto del cursore in cui è possibile usare i metodi [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) e [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) per spostare verso l'alto e verso il basso il set di risultati.

Per impostazione predefinita, la memorizzazione nella cache dei risultati è disabilitata. La memorizzazione nella cache dei risultati deve essere abilitata se si verifica una delle condizioni seguenti:

-   Se lo stesso set di risultati deve essere enumerato più volte senza eseguire di nuovo la ricerca nel server.
-   Se l'esecuzione della ricerca richiede molte risorse nel server (connessione lenta, set di risultati di grandi dimensioni o query complessa).
-   Se è necessario il supporto del cursore.

Disattivare la memorizzazione nella cache se l'applicazione deve ridurre i requisiti di memoria per la memorizzazione nella cache di un set di risultati di grandi dimensioni nel client.

La memorizzazione nella cache dei risultati aumenta i requisiti di memoria nel client, pertanto la memorizzazione nella cache dei risultati deve essere disabilitata se si tratta di un problema.

Per abilitare la memorizzazione nella cache dei risultati, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ CACHE \_ RESULTS** con valore **BOOLEANo ADSTYPE \_** **TRUE** nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Nell'esempio di codice seguente viene illustrato come abilitare la memorizzazione nella cache dei risultati.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




