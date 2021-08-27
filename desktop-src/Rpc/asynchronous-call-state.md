---
title: Stato di chiamata asincrona
description: Questa pagina descrive lo stato della chiamata asincrona per le chiamate RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478627"
---
# <a name="asynchronous-call-state"></a>Stato di chiamata asincrona

Questa pagina descrive lo stato della chiamata asincrona per le chiamate RPC.

## <a name="client-behavior"></a>Comportamento del client




| State | Nome dello stato | Azione | 
|-------|------------|--------|
| C | Effettuare la chiamata | Effettuare la chiamata RPC<ul><li>Se l'operazione ha esito positivo, passare allo stato WComp</li><li>In eccezione passare a Fine</li></ul>Per esito negativo: passare a Can<br /> | 
| Capacità | Annullare la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go a WComp<br /> | 
| WComp | Attendere il completamento | Attendere la ricezione della notificaCall-complete<br /> Passare a Comp<br /> | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Fine | 




 

## <a name="server-behavior"></a>Comportamento del server



| State | Nome dello stato     | Azione                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | La chiamata viene inviata da RPC runtimeProcess<br/> Passare a Comp<br/> Per generare un errore irreversibile (durante l'esecuzione sul thread RPC): genera eccezione. Vai a Fine<br/> Per eseguire correttamente l'errore: passare a A<br/> |
| A     | Interrompere la chiamata | Chiamare [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End<br/>                                                                                                                                             |
| Comp  | Completion     | Problema [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End<br/>                                                                                                                                      |
| Fine   |                |                                                                                                                                                                                                                     |



 

 

 





