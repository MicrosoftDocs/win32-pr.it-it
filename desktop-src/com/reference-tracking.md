---
title: Rilevamento dei riferimenti
description: Rilevamento dei riferimenti
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1321c922cc0a7493e3e4792f7c0f925618330c2e42665296fb06792635a4ea70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309764"
---
# <a name="reference-tracking"></a>Rilevamento dei riferimenti

Il rilevamento dei riferimenti può impedire il rilascio anticipato non intenzionale o dannoso di oggetti.

Quando si abilita il rilevamento dei riferimenti, si richiede che le [**chiamate AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuite siano autenticate da COM. Quando il rilevamento dei riferimenti è abilitato, COM tiene traccia dei conteggi dei riferimenti per utente in modo che un utente possa chiamare **Release** solo sugli oggetti su cui l'utente ha chiamato in precedenza **AddRef.** Anche se il rilevamento dei riferimenti può ridurre le prestazioni, garantisce che indipendentemente dal numero di chiamate di un determinato utente **a Release**, gli oggetti e gli stub saranno ancora presenti se un altro utente ha un riferimento a essi.

Il client può impostare il rilevamento dei riferimenti per un processo passando il flag di funzionalità EOAC \_ SECURE \_ REFS in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). È anche possibile abilitare o disabilitare il rilevamento dei riferimenti per tutte le applicazioni in un computer usando Dcomcnfg.exe.

Se il rilevamento dei riferimenti è abilitato, [**IUnknown usa**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) sempre le impostazioni di sicurezza predefinite. In questo caso, le chiamate [**a CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) in **IUnknown** avranno esito negativo.

 

 