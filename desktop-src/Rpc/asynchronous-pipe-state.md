---
title: Stato di pipe asincrono
description: Questa pagina descrive lo stato asincrono della pipe per le chiamate RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046317"
---
# <a name="asynchronous-pipe-state"></a>Stato di pipe asincrono

Questa pagina descrive lo stato asincrono della pipe per le chiamate RPC.

## <a name="in-pipe"></a>IN pipe

Comportamento del client

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>State Name</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Eseguire la chiamata</td>
<td>Eseguire la chiamata RPC
<ul>
<li>Alla riuscita Vai a stato WS</li>
<li>All'eccezione Vai alla fine</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Push</td>
<td>Eseguire un push
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Alla riuscita andare a WS</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Attendi invio</td>
<td>Attendi notifica
<ul>
<li>In caso di errore di ricevere una notifica, passare a Can</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a P</li>
<li>Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</li>
<li>Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> go comp</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Push 0 byte (push null)
<ul>
<li>In caso di errore Vai alla fine</li>
<li>In riuscita andare a WComp</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="odd">
<td>Capacità</td>
<td>Annulla la chiamata</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Attendi completamento</td>
<td>Attendere la ricezione della notifica notificationCall-complete.<br/> Vai a comp<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine<br/></td>
</tr>
<tr class="even">
<td>Fine</td>


</tr>
</tbody>
</table>



 

Comportamento del server

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>State Name</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>La chiamata viene inviata dal runtime RPC Vai a P<br/> Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine<br/> Per eseguire correttamente l'errore: passare a un<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Pull</td>
<td>Eseguire un pull
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Al completamento dell'operazione riuscita e sincrona con byte diversi da zero, vai a P</li>
<li>Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) Vai a comp</li>
<li>Alla riuscita e al completamento asincrono (ERROR_IO_PENDING viene restituito) andare a WP</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendi pull</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a</li>
<li>Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a un</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, vedere Vai a P</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte letti (pull null) Vai a comp</li>
<li>Se viene ricevuto un errore, passare a un</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>Interrompi la chiamata</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Vai alla fine<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine<br/></td>
</tr>
<tr class="even">
<td>Fine</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>Pipe OUT

Comportamento del client

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>State Name</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Eseguire la chiamata</td>
<td>Eseguire la chiamata RPC
<ul>
<li>Alla riuscita andare a P</li>
<li>In caso di errore Vai a comp</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Pull</td>
<td>Eseguire un pull
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Al completamento dell'operazione riuscita e sincrona con byte diversi da zero, vai a P</li>
<li>Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) passare a WComp</li>
<li>Alla riuscita e al completamento asincrono (ERROR_IO_PENDING viene restituito) andare a WP</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendi pull</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a Can</li>
<li>Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a Can</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, vedere Vai a P</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte letti (pull null) Vai a comp</li>
<li>Se viene ricevuto un errore, Go può</li>
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
<td>Attendere la notifica. È necessario ricevere una notifica di completamento della chiamata.<br/> Vai a comp<br/></td>
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



 

Comportamento del server

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>State Name</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>La chiamata viene inviata dal runtime RPC Vai a P<br/> Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine<br/> Per eseguire correttamente l'errore: passare a un<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Push</td>
<td>Eseguire un push
<ul>
<li>In riuscita andare a WP</li>
<li>In caso di errore Vai alla fine</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Attendi push</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a P</li>
<li>Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</li>
<li>Se viene ricevuto un errore go comp</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Push 0 byte
<ul>
<li>in riuscita andare a WNP</li>
<li>in caso di errore Vai a comp</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Attendi push null</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a</li>
<li>Se viene ricevuto un errore go comp</li>
<li>Se viene ricevuta una riuscita, vai comp</li>
</ul></td>
</tr>
<tr class="even">
<td>A</td>
<td>Interrompi la chiamata</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; Vai alla fine</td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; Vai alla fine</td>
</tr>
<tr class="even">
<td>Fine</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>Pipe IN uscita

Comportamento del client

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>State Name</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Eseguire la chiamata</td>
<td>Eseguire la chiamata RPC
<ul>
<li>Alla riuscita andare a WS</li>
<li>All'eccezione Vai alla fine</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Push</td>
<td>Eseguire un push
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Alla riuscita andare a WS</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Attendi invio</td>
<td>Attendi notifica
<ul>
<li>In caso di errore di ricevere una notifica, passare a Can</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a PS</li>
<li>Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</li>
<li>Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> go comp</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Push 0 byte (push null)
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Alla riuscita andare a PL</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>Pull</td>
<td>Eseguire un pull
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Se il completamento è stato completato e sincrono con byte diversi da zero, leggi Vai a PL</li>
<li>Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) passare a WComp</li>
<li>In seguito all'esito positivo e al completamento asincrono (ERROR_IO_PENDING viene restituito) passare a WPL</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="even">
<td>WPL</td>
<td>Attendi pull</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a Can</li>
<li>Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a Can</li>
<li>Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, leggi Vai a pl</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte lettura Vai a comp</li>
<li>Se viene ricevuto un errore, Go può</li>
</ul>
Per avere esito negativo: passare a Can<br/></td>
</tr>
<tr class="odd">
<td>Capacità</td>
<td>Annulla la chiamata</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Vai a WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Attendi completamento</td>
<td>Attendere la notifica. È necessario ricevere una notifica CallComplete.<br/> Vai a comp<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Vai alla fine<br/></td>
</tr>
<tr class="even">
<td>Fine</td>


</tr>
</tbody>
</table>



 

Comportamento del server

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>State</th>
<th>State Name</th>
<th>Azione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>La chiamata viene inviata dal runtimeGo RPC a PL<br/> Per avere esito negativo (durante l'esecuzione sul thread RPC): Genera eccezione; Vai alla fine<br/> Per eseguire correttamente l'errore: passare a un<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>Pull</td>
<td>Eseguire un pull
<ul>
<li>In caso di errore Vai alla fine</li>
<li>Se il completamento è stato completato e sincrono con byte diversi da zero, leggi Vai a PL</li>
<li>Al completamento dell'operazione riuscita e sincrona con zero byte letti (pull null) andare a PS</li>
<li>In seguito all'esito positivo e al completamento asincrono (ERROR_IO_PENDING viene restituito) passare a WPL</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="odd">
<td>WPL</td>
<td>Attendi pull</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a</li>
<li>Se viene ricevuto un errore <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , passare a un</li>
<li>Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con byte diversi da zero, leggi Vai a pl</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con esito positivo con zero byte letti, vai a PS</li>
<li>Se viene ricevuto un errore, passare A</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Push</td>
<td>Eseguire un push
<ul>
<li>In riuscita passare a WPS</li>
<li>In caso di errore Vai alla fine</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="odd">
<td>WPS</td>
<td>Attendi push</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a</li>
<li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> di esito positivo ed è necessario inviare più dati, passare a PS</li>
<li>Se viene ricevuta una <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> con esito positivo e non è necessario inviare più dati, passare a NP</li>
<li>Se viene ricevuto un errore go comp</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Push null</td>
<td>Push 0 byte
<ul>
<li>in riuscita andare a WNP</li>
<li>in caso di errore Vai a comp</li>
</ul>
Per avere esito negativo: passare a un<br/></td>
</tr>
<tr class="odd">
<td>WNP</td>
<td>Attendi push null</td>
<td>Attendi notifica
<ul>
<li>In caso di errore per ottenere un completamento, passare a</li>
<li>Se viene ricevuto un errore go comp</li>
<li>Se viene ricevuta una riuscita, vai comp</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>Interrompi la chiamata</td>
<td>Chiama <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; Vai alla fine</td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; Vai alla fine</td>
</tr>
<tr class="even">
<td>Fine</td>


</tr>
</tbody>
</table>



 

 

 





