---
title: Uso dei metodi
description: Quando un client esegue la registrazione con gestione tabelle di routing, può esportare un set di metodi. Questi metodi vengono usati da altri client per ottenere informazioni specifiche del client. I metodi consentono la comunicazione privata tra i client del gestore tabelle di routing.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150edb6435e0021c13e129f7c1e7a3016dc0974283fcdd138189f7d1c4a3184a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025101"
---
# <a name="using-methods"></a>Uso dei metodi

Quando un client esegue la registrazione con gestione tabelle di routing, può esportare un set di metodi. Questi metodi vengono usati da altri client per ottenere informazioni specifiche del client. I metodi consentono la comunicazione privata tra i client del gestore tabelle di routing.

Un client può ottenere l'elenco dei metodi esportati da un altro client. Il client chiama la [**funzione RtmGetEntityMethods,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) fornendo l'handle del client di destinazione.

Ogni metodo esportato da un client viene identificato in modo univoco dal relativo identificatore di metodo. Ogni client può esportare fino a 32 metodi. Ogni metodo corrisponde a un bit impostato nel membro **MethodType** della struttura [**\_ RTM ENTITY \_ EXPORT \_ METHOD.**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) Per richiamare più metodi, il client deve eseguire un OR logico degli identificatori per tali metodi. Quando il protocollo viene implementato, è necessario specificare la sintassi e la semantica delle strutture di input e output per ogni protocollo.

> [!Note]  
> I valori dell'identificatore di metodo che corrispondono a un bit impostato nella metà inferiore del membro **MethodType** (i 16 bit inferiori) sono riservati da Microsoft.

 

Per richiamare il metodo di un secondo client, un client chiama la [**funzione RtmInvokeMethod.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) Il gestore tabelle di routing abitra tutte le richieste per richiamare i metodi di un client. Gestione tabelle di routing esegue due funzioni quando esegue l'abitrate tra i client:

-   Impedendo al secondo client di richiamare un metodo per un client che annulla la registrazione.
-   Contiene una richiesta "invoke" quando i metodi sono bloccati e consente alla richiesta di continuare quando i metodi vengono sbloccati.

Se un client deve impedire ad altri client di eseguire i propri metodi, il client può chiamare [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods). Il gestore tabelle di routing non consentirà l'elaborazione di una chiamata a [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) finché il client non sblocca nuovamente i relativi metodi.

I client bloccano in genere i metodi quando si apportano modifiche ai dati privati s scambiati tra i client. I metodi di blocco sono un'azione facoltativa. Un client può anche usare blocchi interni per impedire ad altri client di richiamare metodi.

Per il codice di esempio che illustra come usare queste funzioni, vedere Ottenere e [chiamare i metodi esportati per un client](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




