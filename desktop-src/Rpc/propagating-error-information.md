---
title: Propagazione delle informazioni sugli errori
description: La propagazione di informazioni estese sugli errori consente ai server che ricevono un errore RPC S \ o qualsiasi altro codice di errore per questo tipo di errore, di consentire al tempo di esecuzione RPC di propagare le informazioni ricevute ai \_ \_ chiamanti.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ecf011dbac01d2b4c931a463bebb3739a92322059eb3a7a342160c42a9e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927159"
---
# <a name="propagating-error-information"></a>Propagazione delle informazioni sugli errori

La propagazione di informazioni estese sugli errori consente ai server che ricevono un errore RPC S o qualsiasi altro codice di errore in tal caso, di consentire al tempo di esecuzione RPC di propagare le informazioni ricevute ai \_ \_ \* chiamanti. Il server deve solo chiamare [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) quando si verifica un errore irreversibile. Il tempo di esecuzione RPC si occupa del concatenamento delle eventuali informazioni sull'errore esteso, causando la segnalazione dell'errore irreversibile stesso, purché il codice di errore assegnato a **RpcRaiseException** o **RpcAsyncAbortCall** sia uguale al codice di errore che causa l'errore irreversibile.

 

 




