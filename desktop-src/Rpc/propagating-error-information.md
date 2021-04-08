---
title: Propagazione delle informazioni sugli errori
description: La propagazione delle informazioni dettagliate sugli errori consente ai server che ricevono un \_ \_ errore RPC o a qualsiasi altro codice di errore, per consentire al tempo di esecuzione RPC di propagare le informazioni ricevute ai chiamanti.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856669"
---
# <a name="propagating-error-information"></a>Propagazione delle informazioni sugli errori

La propagazione delle informazioni estese sugli errori consente ai server che ricevono un errore di RPC \_ \_ \* o a qualsiasi altro codice di errore, per consentire al tempo di esecuzione RPC di propagare le informazioni ricevute ai chiamanti. Tutto il server deve eseguire la chiamata a [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) quando si verifica un errore irreversibile. Il tempo di esecuzione RPC gestisce il concatenamento delle informazioni di errore estese, se presenti, causando l'errore irreversibile nel segnalare l'errore irreversibile, purché il codice di errore assegnato a **RpcRaiseException** o **RpcAsyncAbortCall** sia uguale al codice di errore che ha causato l'errore irreversibile.

 

 




