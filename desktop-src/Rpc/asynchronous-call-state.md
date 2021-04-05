---
title: Stato di chiamata asincrono
description: Questa pagina descrive lo stato di chiamata asincrono per le chiamate RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856970"
---
# <a name="asynchronous-call-state"></a>Stato di chiamata asincrono

Questa pagina descrive lo stato di chiamata asincrono per le chiamate RPC.

## <a name="client-behavior"></a>Comportamento del client



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>Nome dello stato</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Eseguire la chiamata</td>
<td>Eseguire la chiamata RPC
<ul>
<li>In riuscita Vai a stato WComp</li>
<li>All'eccezione Vai alla fine</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>Capacità</td>
<td>Annulla la chiamata</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp<br/></td>
</tr>
<tr class="odd">
<td>WComp</td>
<td>Attendi completamento</td>
<td>Attendi notificationCall-è necessario ricevere una notifica completa<br/> Vai a comp<br/></td>
</tr>
<tr class="even">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine<br/></td>
</tr>
<tr class="odd">
<td>Fine</td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a>Comportamento del server



| State | Nome dello stato     | Azione                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | La chiamata viene inviata dal runtimeProcess RPC<br/> Vai a comp<br/> Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine<br/> Per eseguire correttamente l'errore: passare a un<br/> |
| A     | Interrompi la chiamata | Chiama [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Vai alla fine<br/>                                                                                                                                             |
| Comp  | Completion     | Problema [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Vai alla fine<br/>                                                                                                                                      |
| Fine   |                |                                                                                                                                                                                                                     |



 

 

 





