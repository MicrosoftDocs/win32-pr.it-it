---
title: Rilevamento riferimenti
description: Rilevamento riferimenti
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474310"
---
# <a name="reference-tracking"></a>Rilevamento riferimenti

Il rilevamento dei riferimenti può impedire la versione iniziale non intenzionale o dannosa di oggetti.

Quando si Abilita il rilevamento dei riferimenti, si richiede che le chiamate [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuite vengano autenticate da com. Quando è abilitata la verifica dei riferimenti, COM tiene traccia dei conteggi dei riferimenti per ogni utente, in modo che un utente possa chiamare la **versione** solo sugli oggetti che l'utente ha precedentemente chiamato **AddRef** . Sebbene il rilevamento dei riferimenti possa ridurre le prestazioni, garantisce che, indipendentemente dal numero di volte in cui un determinato utente chiama il **rilascio**, gli oggetti e gli stub continueranno a esistere se qualcun altro ha un riferimento.

Il client può impostare il rilevamento dei riferimenti per un processo passando il \_ flag EOAC Secure \_ refs Capability in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). È inoltre possibile abilitare o disabilitare il rilevamento dei riferimenti per tutte le applicazioni in un computer utilizzando Dcomcnfg.exe.

Se la verifica dei riferimenti è abilitata, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) utilizza sempre le impostazioni di sicurezza predefinite. In questo caso, le chiamate a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) su **IUnknown** avranno esito negativo.

 

 