---
title: Annullamento di una chiamata asincrona
description: Un client può annullare una chiamata asincrona in corso se l'oggetto chiamata implementa l'interfaccia ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d2751400d631c62c19f68f2cab841c0845b432df676abe60befed1f231e103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737115"
---
# <a name="canceling-an-asynchronous-call"></a>Annullamento di una chiamata asincrona

Un client può annullare una chiamata asincrona in corso se l'oggetto chiamata implementa [**l'interfaccia ICancelMethodCalls.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) Per gli oggetti che usano il marshalling standard, **ICancelMethodCalls** è sempre disponibile per le chiamate con marshalling. Per gli oggetti che usano il marshalling personalizzato o per le chiamate a oggetti server all'interno dello stesso apartment, questa funzionalità è disponibile solo se l'oggetto chiamata implementa **ICancelMethodCalls**.

Il client può annullare la chiamata in qualsiasi momento, da quando viene chiamato il metodo Begin \_ fino a quando non viene restituito il metodo \_ Finish. Se il client annulla la chiamata prima di chiamare il metodo Finish, deve chiamare il metodo Finish per pulire lo \_ \_ stato dell'oggetto chiamata. Fino a quando il client non ha eseguito questa operazione, tutte le chiamate a qualsiasi metodo Begin \_ nell'oggetto chiamata restituiranno RPC \_ E \_ CALL \_ PENDING.

**Per annullare una chiamata asincrona**

1.  Eseguire una query sull'oggetto chiamata [**per ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).

2.  Chiamare [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)e quindi [**chiamare Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare il puntatore ottenuto dalla chiamata [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) nel passaggio 1.

3.  Se il client non ha già chiamato il metodo \_ Finish, chiamarlo ora.

Non è garantito che il server ha effettivamente arrestato l'esecuzione della chiamata. Se l'ulteriore lavoro del client dipende da uno stato del server che la chiamata può o meno essere stata modificata, il client deve determinare tale stato prima di procedere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 