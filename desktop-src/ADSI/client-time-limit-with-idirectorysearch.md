---
title: Limite di tempo del client con IDirectorySearch
description: Un client può imporre un limite di tempo per la restituzione del set di risultati da parte di un server. Quando il server non risponde a una query entro il periodo di tempo specificato, il client può abbandonare la ricerca e riprovare più tardi.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite di tempo del client con IDirectorySearch
- ADSI, Ricerca, IDirectorySearch, Altre opzioni di ricerca, Limite di tempo client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1798094a980c41de2e1902533415839020cfd690384f0e56a37bff918d4ecc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692510"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Limite di tempo del client con IDirectorySearch

Un client può imporre un limite di tempo per la restituzione del set di risultati da parte di un server. Quando il server non risponde a una query entro il periodo di tempo specificato, il client può abbandonare la ricerca e riprovare più tardi.

La preferenza relativa al limite di tempo del client è utile quando un client richiede una ricerca asincrona. In una ricerca asincrona, il client effettua una richiesta e quindi procede con altre attività in attesa che il server restituirà i risultati. È possibile che il server possa passare alla modalità offline senza notificare il client. In questo caso, il client non dirà se il server sta ancora elaborando la query o se non è più in tempo reale. La preferenza relativa al limite di tempo del client offre al client il controllo di situazioni come questa.

Il valore predefinito per il limite di tempo del client è nessun limite. Per impostare un limite di tempo client, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ TIMEOUT** con un valore **INTEGER ADSTYPE \_** che contiene il limite di tempo del client, in secondi, nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Un limite di tempo client pari a zero indica nessun limite di tempo.

Nell'esempio di codice seguente viene illustrato come impostare il limite di tempo del client.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




