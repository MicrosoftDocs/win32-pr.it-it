---
title: Inseguimento dei riferimenti con IDirectorySearch
description: Un riferimento è il meccanismo utilizzato da un server di directory per indirizzare un client a un altro server quando non contiene dati sufficienti sull'oggetto richiesto da una query.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Inseguimento dei riferimenti con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, inseguimento del riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963455"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Inseguimento dei riferimenti con IDirectorySearch

Un riferimento è il meccanismo utilizzato da un server di directory per indirizzare un client a un altro server quando non contiene dati sufficienti sull'oggetto richiesto da una query.

In una ricerca a un livello o un sottoalbero, i riferimenti vengono restituiti solo per i contenitori noti, immediatamente subordinati di dominio, schema o configurazione. ovvero domini figlio che sono discendenti diretti. Per altre informazioni, vedere [ambito di ricerca](/windows/desktop/AD/search-scope).

In una directory, non tutti i dati sono disponibili in un singolo server, bensì distribuiti in più server diversi in rete. Se i server condividono i dati che altri server possono fornire, possono fornire riferimenti a un client quando una query richiesta non può essere risolta nel server di origine. Ad esempio, quando un client chiede al server a di eseguire una query su un oggetto utente (U), un può suggerire che il client continua la ricerca sul server B se U non si trova su un oggetto, ma viene identificato come B. Il client ha la possibilità di proseguire o meno il riferimento. I riferimenti consentono al client di avere una conoscenza precedente della capacità di ogni server, ma il client deve specificare il tipo di riferimenti che un server deve eseguire.

Per abilitare o disabilitare l'indisponibilità di riferimento, impostare un'opzione di ricerca dei **riferimenti di ADS \_ SEARCHPREF \_ Chase \_** con un valore **\_ Integer ADSTYPE** che contenga uno dei valori di enumerazione per gli [**annunci \_ Chase per \_ \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) i riferimenti di enumerazione nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

Nell'esempio di codice seguente viene illustrato come abilitare i riferimenti per Chase.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Per ulteriori informazioni sui riferimenti in Active Directory, vedere [riferimenti](/windows/desktop/AD/referrals).

 

 