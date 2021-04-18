---
title: Limite di tempo client con IDirectorySearch
description: Un client può imporre un limite di tempo per la restituzione del set di risultati da parte di un server. Quando il server non riesce a rispondere a una query entro il periodo di tempo specificato, il client può abbandonare la ricerca e riprovare più tardi.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite di tempo client con IDirectorySearch
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite di tempo client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297693"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Limite di tempo client con IDirectorySearch

Un client può imporre un limite di tempo per la restituzione del set di risultati da parte di un server. Quando il server non riesce a rispondere a una query entro il periodo di tempo specificato, il client può abbandonare la ricerca e riprovare più tardi.

La preferenza per il limite di tempo client è utile quando un client richiede una ricerca asincrona. In una ricerca asincrona, il client effettua una richiesta e quindi procede con altre attività in attesa che il server restituisca i risultati. È possibile che il server sia offline senza notificare al client. In questo caso, il client non avrà alcuna notifica se il server sta ancora elaborando la query o se non è più attiva. La preferenza per il limite di tempo client fornisce al client un controllo di situazioni come questa.

Il valore predefinito per il limite di tempo client non è limite. Per impostare un limite di tempo client, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ timeout** con un valore **\_ Integer ADSTYPE** che contenga il limite di tempo client, espresso in secondi, nella matrice di [**\_ \_ informazioni SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Un limite di tempo del client pari a zero indica nessun limite di tempo.

Nell'esempio di codice seguente viene illustrato come impostare il limite di tempo del client.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




