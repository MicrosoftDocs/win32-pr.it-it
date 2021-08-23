---
title: Limite di tempo del server con IDirectorySearch
description: Per evitare di usare tutto il tempo della CPU e impedire l'esecuzione di altre operazioni, specificare il limite di tempo di ricerca su un valore ridotto e quindi rieseguire l'applicazione in un secondo momento se non riesce a generare il report.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Limite di tempo del server con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite di tempo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e120586cb05fa07baf1e26fa8c1db8e11eecdbd1b19ed7f4f9c2215a921409ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262131"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Limite di tempo del server con IDirectorySearch

Quando si richiede una ricerca in un server occupato, è possibile richiedere al server di limitare la ricerca a un limite di tempo specificato. Ad esempio, si vuole eseguire un'applicazione per generare un report settimanale in un server in esecuzione vicino alla capacità. Per evitare di usare tutto il tempo della CPU e impedire l'esecuzione di altre operazioni, specificare il limite di tempo di ricerca su un valore ridotto e quindi rieseguire l'applicazione in un secondo momento se non riesce a generare il report.

Alcuni server potrebbero imporre un proprio limite di tempo amministrativo. In questi casi, se si specifica un valore di limite di tempo di ricerca maggiore del limite di tempo amministrativo, il server ignorerà la specifica e userà invece il valore del limite di tempo interno.

Il valore predefinito per il limite di tempo del server è nessun limite. Per impostare un limite di tempo del server, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ TIME \_ LIMIT** con un valore **INTEGER ADSTYPE \_** che contiene il limite di tempo del server, in secondi, nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Questa operazione è illustrata nell'esempio di codice seguente. Un limite di tempo del server pari a zero indica che non è previsto alcun limite di tempo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




