---
title: Gestione delle chiamate asincrone
description: La routine Manager di una funzione asincrona riceve sempre l'handle asincrono come primo parametro. Il server deve tenere traccia di questo handle e utilizzarlo per inviare la risposta al termine della chiamata asincrona di procedura remota.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396206"
---
# <a name="handling-asynchronous-calls"></a>Gestione delle chiamate asincrone

La routine Manager di una funzione asincrona riceve sempre l'handle asincrono come primo parametro. Il server deve tenere traccia di questo handle e utilizzarlo per inviare la risposta al termine della chiamata asincrona di procedura remota.

Se il server deve interrompere un RPC asincrono, viene chiamato [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall). Questa funzione esegue la stessa pulizia sul lato server di [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) e propaga al client un codice di eccezione (fornito dall'applicazione server), ad eccezione del fatto che non esegue il marshalling degli argomenti out.

Per un esempio di una procedura asincrona, vedere [invio della risposta asincrona](sending-the-asynchronous-reply.md).

 

 




