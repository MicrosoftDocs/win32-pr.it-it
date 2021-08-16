---
title: Ricerca delle segnalazioni con IDirectorySearch
description: Una segnalazione è il meccanismo utilizzato da un server di directory per indirizzare un client a un altro server quando non contiene dati sufficienti sull'oggetto richiesto da una query.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Ricerca delle segnalazioni con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, ricerca delle segnalazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7fcc74103c5c09816976e9ff91c17ecca8578fcbf596b731df890a350e922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690690"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Ricerca delle segnalazioni con IDirectorySearch

Una segnalazione è il meccanismo utilizzato da un server di directory per indirizzare un client a un altro server quando non contiene dati sufficienti sull'oggetto richiesto da una query.

In una ricerca a un livello o sottoalbero vengono restituite segnalazioni solo per contenitori di dominio, schema o configurazione noti, immediatamente subordinati; cio, domini figlio discendenti diretti. Per altre informazioni, vedere [Ambito di ricerca](/windows/desktop/AD/search-scope).

In una directory non tutti i dati sono disponibili in un singolo server, ma vengono distribuiti su più server diversi in rete. Se i server condividono i dati che altri server possono fornire, possono fornire riferimenti a un client quando una query richiesta non può essere risolta nel server di origine. Ad esempio, quando un client chiede al server A di eseguire query su un oggetto utente (U), A può suggerire che il client continui la ricerca nel Server B se U non risiede in A, ma viene identificato come in B. Il client può scegliere se seguire o meno la segnalazione. Le segnalazioni liberano il client dalla necessità di avere conoscenze precedenti sulla funzionalità di ogni server, ma il client deve specificare il tipo di segnalazioni che un server deve eseguire.

Per abilitare o disabilitare la ricerca delle segnalazioni, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ CHASE \_ REFERRALS** con un valore **ADSTYPE \_ INTEGER** che contiene uno dei valori di enumerazione [**\_ \_ \_ ENUM ADS CHASE REFERRALS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Nell'esempio di codice seguente viene illustrato come abilitare le segnalazioni di sequenza.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Per altre informazioni sulle segnalazioni in Active Directory, vedere [Segnalazioni](/windows/desktop/AD/referrals).

 

 