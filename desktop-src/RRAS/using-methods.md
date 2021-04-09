---
title: Metodi using
description: Quando un client esegue la registrazione con gestione tabelle di routing, può esportare un set di metodi. Questi metodi vengono usati da altri client per ottenere informazioni specifiche del client. I metodi consentono la comunicazione privata tra i client di gestione tabelle di routing.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955551"
---
# <a name="using-methods"></a>Metodi using

Quando un client esegue la registrazione con gestione tabelle di routing, può esportare un set di metodi. Questi metodi vengono usati da altri client per ottenere informazioni specifiche del client. I metodi consentono la comunicazione privata tra i client di gestione tabelle di routing.

Un client può ottenere l'elenco dei metodi esportati da un altro client. Il client chiama la funzione [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , specificando l'handle del client di destinazione.

Ogni metodo esportato da un client viene identificato in modo univoco dal relativo identificatore del metodo. Ogni client può esportare fino a 32 metodi. Ogni metodo corrisponde a un bit impostato nel membro **MethodType** della struttura del [**\_ metodo di \_ esportazione \_ dell'entità RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) . Per richiamare più metodi, il client deve eseguire un OR logico degli identificatori per tali metodi. Quando il protocollo è implementato, è necessario specificare la sintassi e la semantica delle strutture di input e di output per ogni protocollo.

> [!Note]  
> I valori dell'identificatore di metodo che corrispondono a un bit impostato nella metà inferiore del membro **MethodType** (i 16 bit inferiori) sono riservati da Microsoft.

 

Per richiamare un secondo metodo del client, un client chiama la funzione [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) . Gestione tabelle di routing arbitraggio tutte le richieste per richiamare i metodi di un client. Gestione tabelle di routing esegue due funzioni quando arbitraggio tra i client:

-   Impedire al secondo client di richiamare un metodo per un client che sta annullando la registrazione.
-   Con una richiesta "Invoke" quando i metodi sono bloccati e consentendo la continuazione della richiesta quando i metodi vengono sbloccati.

Se un client deve impedire l'esecuzione dei metodi di altri client, il client può chiamare [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods). Gestione tabelle di routing non consente l'elaborazione di una chiamata a [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) fino a quando il client non sblocca nuovamente i relativi metodi.

I client in genere bloccano i metodi quando si apportano modifiche ai dati privati scambiati tra i client. I metodi di blocco sono un'azione facoltativa. Un client può inoltre utilizzare blocchi interni per impedire che altri client richiamino metodi.

Per il codice di esempio che illustra come usare queste funzioni, vedere [ottenere e chiamare i metodi esportati per un client](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




