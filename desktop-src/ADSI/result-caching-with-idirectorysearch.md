---
title: Caching dei risultati con IDirectorySearch
description: La \_ \_ preferenza per i risultati della cache ADS SEARCHPREF memorizza nella \_ cache il set di risultati nel client.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Caching dei risultati con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, Caching di risultati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328372"
---
# <a name="result-caching-with-idirectorysearch"></a>Caching dei risultati con IDirectorySearch

La preferenza per i **\_ Risultati della \_ cache \_ ADS SEARCHPREF** memorizza nella cache il set di risultati nel client. La memorizzazione nella cache dei risultati consente a un'applicazione di mantenere un set di risultati recuperato e di eseguire nuovamente le righe recuperate. Consente inoltre il supporto dei cursori in cui è possibile utilizzare i metodi [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) e [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) per spostarsi verso l'alto e verso il basso del set di risultati.

Per impostazione predefinita, la memorizzazione nella cache dei risultati è disabilitata. La memorizzazione nella cache dei risultati deve essere abilitata se si verifica una delle condizioni seguenti:

-   Se lo stesso set di risultati deve essere enumerato più volte senza eseguire di nuovo la ricerca nel server.
-   Se l'esecuzione della ricerca prevede un utilizzo intensivo delle risorse sul server (connessione lenta, set di risultati di grandi dimensioni o query complesse).
-   Se è richiesto il supporto del cursore.

Disattivare la memorizzazione nella cache se l'applicazione deve ridurre i requisiti di memoria per la memorizzazione nella cache di un set di risultati di grandi dimensioni nel client.

La memorizzazione nella cache dei risultati aumenta i requisiti di memoria sul client, quindi la memorizzazione dei risultati nella cache dovrebbe essere disabilitata se si tratta di un problema.

Per abilitare la memorizzazione nella cache dei risultati, impostare un'opzione di ricerca per i **\_ \_ \_ Risultati della cache ADS SEARCHPREF** con un valore **\_ booleano ADSTYPE** **true** nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

Nell'esempio di codice seguente viene illustrato come abilitare la memorizzazione dei risultati nella cache.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




