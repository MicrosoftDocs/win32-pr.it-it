---
title: Annullamento di una chiamata asincrona
description: Un client può annullare una chiamata asincrona in corso se l'oggetto chiamata implementa l'interfaccia ICancelMethodCalls.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118534"
---
# <a name="canceling-an-asynchronous-call"></a>Annullamento di una chiamata asincrona

Un client può annullare una chiamata asincrona in corso se l'oggetto chiamata implementa l'interfaccia [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . Per gli oggetti che usano il marshalling standard, **ICancelMethodCalls** è sempre disponibile per le chiamate sottoposte a marshalling. Per gli oggetti che usano il marshalling personalizzato o per le chiamate a oggetti server all'interno dello stesso Apartment, questa funzionalità è disponibile solo se l'oggetto chiamata implementa **ICancelMethodCalls**.

Il client può annullare la chiamata in qualsiasi momento, da quando il \_ metodo Begin viene chiamato fino a quando il metodo Finish non \_ restituisce. Se il client Annulla la chiamata prima di chiamare il \_ Metodo Finish, deve chiamare il metodo Finish \_ per pulire lo stato dell'oggetto call. Fino a quando il client non ha eseguito questa operazione, tutte le chiamate a qualsiasi metodo Begin nell' \_ oggetto chiamata restituiranno la \_ chiamata RPC E \_ \_ in sospeso.

**Per annullare una chiamata asincrona**

1.  Eseguire una query sull'oggetto chiamata per [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).

2.  Chiamare [**ICancelMethodCalls:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), quindi chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare il puntatore ottenuto dalla chiamata [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) nel passaggio 1.

3.  Se il client non ha ancora chiamato il \_ Metodo Finish, chiamarlo ora.

Non esiste alcuna garanzia che il server abbia interrotto effettivamente l'esecuzione della chiamata. Se l'ulteriore lavoro del client dipende da uno stato del server in cui è possibile che la chiamata non sia stata modificata, il client deve determinare tale stato prima di procedere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di una chiamata asincrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 