---
title: Limite di tempo del server con IDirectorySearch
description: Per evitare di usare tutto il tempo della CPU e impedire l'esecuzione di altre operazioni, specificare il limite di tempo di ricerca per un valore ridotto, quindi eseguire di nuovo l'applicazione in un secondo momento se non riesce a generare il report.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Limite di tempo del server con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite di tempo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955082"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Limite di tempo del server con IDirectorySearch

Quando si richiede una ricerca in un server occupato, potrebbe essere necessario richiedere che il server limiti la ricerca a un limite di tempo specificato. Si consiglia, ad esempio, di eseguire un'applicazione per generare un report settimanale in un server in cui è in esecuzione quasi la sua capacità. Per evitare di usare tutto il tempo della CPU e impedire l'esecuzione di altre operazioni, specificare il limite di tempo di ricerca per un valore ridotto, quindi eseguire di nuovo l'applicazione in un secondo momento se non riesce a generare il report.

Alcuni server potrebbero imporre un limite di tempo amministrativo. In questi casi, se si specifica un valore per il limite di tempo di ricerca superiore al limite di tempo amministrativo, il server ignorerà la specifica e utilizzerà il relativo valore limite di tempo interno.

Il valore predefinito per il limite di tempo del server non è limite. Per impostare un limite di tempo per il server, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ tempo \_ limite** con un valore **\_ Integer ADSTYPE** che contenga il limite di tempo del server, in secondi, nella matrice di [**\_ \_ informazioni SEARCHPREF degli annunci**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Questa operazione è illustrata nell'esempio di codice seguente. Un limite di tempo del server pari a zero indica nessun limite di tempo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




