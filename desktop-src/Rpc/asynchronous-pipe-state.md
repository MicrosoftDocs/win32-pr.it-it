---
title: Stato della pipe asincrona
description: Questa pagina descrive lo stato della pipe asincrona per le chiamate RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35e54d9f86228cb4c957f53411c105e20e2109
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468168"
---
# <a name="asynchronous-pipe-state"></a>Stato della pipe asincrona

Questa pagina descrive lo stato della pipe asincrona per le chiamate RPC.

## <a name="in-pipe"></a>IN Pipe

Comportamento del client


| State | State Name | Azione | 
|-------|------------|--------|
| C | Effettuare la chiamata | Effettuare la chiamata RPC<ul><li>In esito positivo passare allo stato WS</li><li>In eccezione passare a Fine</li></ul>Per avere esito negativo: passare a Can<br /> | 
| P | Push | Eseguire un push<ul><li>In caso di errore passare a Fine</li><li>Al termine, passare a WS</li></ul>Per avere esito negativo: passare a Can<br /> | 
| WS | Attendere l'invio | Attendere la notifica<ul><li>Se non si ottiene una notifica, passare a Può</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e è necessario inviare altri dati, passare a P</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e non è necessario inviare altri dati, passare a NP</li><li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>errore RpcCallComplete,</strong></a> passare a Comp</li></ul>Per avere esito negativo: passare a Can<br /> | 
| NP | Null Push | Push di 0 byte (push Null)<ul><li>In caso di errore passare a Fine</li><li>Al termine, passare a WComp</li></ul>Per avere esito negativo: passare a Can<br /> | 
| Capacità | Annullare la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go a WComp<br /> | 
| WComp | Attendere il completamento | Attendere la ricezione della notificaCall-complete.<br /> Passare a Comp<br /> | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Fine | 




 

Comportamento del server


| State | State Name | Azione | 
|-------|------------|--------|
| D | Dispatch | La chiamata viene inviata dal runtime RPC Vai a P<br /> Per generare un errore irreversibile (durante l'esecuzione nel thread RPC): genera un'eccezione. vai a Fine<br /> Per eseguire correttamente l'errore: passare a A<br /> | 
| P | Pull | Eseguire un pull<ul><li>In caso di errore passare a Fine</li><li>In corrispondenza dell'esito positivo e del completamento sincrono con byte di lettura diverso da zero, passare a P</li><li>In caso di esito positivo e completamento sincrono con zero byte letti (pull Null) passare a Comp</li><li>In esito positivo e completamento asincrono (ERROR_IO_PENDING restituito) passare a WP</li></ul>Per avere esito negativo: passare ad A<br /> | 
| WP | Attendere il pull | Attendere la notifica<ul><li>In caso di esito negativo, passare ad A</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un errore RpcReceiveComplete,</strong></a> passare ad A</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcReceiveComplete</strong></a> con byte di lettura non pari a zero, passare a P</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcReceiveComplete</strong></a> con zero byte letti (pull Null) passare a Comp</li><li>Se viene ricevuto un errore, passare ad A</li></ul>Per avere esito negativo: passare ad A<br /> | 
| A | Interrompere la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End<br /> | 
| Comp | Completion | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Fine | 




 

## <a name="out-pipe"></a>OUT Pipe

Comportamento del client


| State | State Name | Azione | 
|-------|------------|--------|
| C | Effettuare la chiamata | Effettuare la chiamata RPC<ul><li>In esito positivo passare a P</li><li>In caso di errore passare a Comp</li></ul>Per avere esito negativo: passare a Can<br /> | 
| P | Pull | Eseguire un pull<ul><li>In caso di errore passare a Fine</li><li>In corrispondenza dell'esito positivo e del completamento sincrono con byte di lettura diverso da zero, passare a P</li><li>In caso di esito positivo e completamento sincrono con zero byte letti (pull Null) passare a WComp</li><li>In esito positivo e completamento asincrono (ERROR_IO_PENDING restituito) passare a WP</li></ul>Per avere esito negativo: passare a Can<br /> | 
| WP | Attendere il pull | Attendere la notifica<ul><li>In caso di esito negativo per ottenere un completamento, passare a Can</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un errore RpcReceiveComplete,</strong></a> passare a Can</li><li>Se viene ricevuto un esito positivo <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con byte non zero letti, passare a P</li><li>Se viene ricevuto un esito positivo <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> con zero byte letti (pull Null) passare a Comp</li><li>Se viene ricevuto un errore, è possibile</li></ul>Per esito negativo: passare a Can<br /> | 
| Capacità | Annullare la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go a WComp<br /> | 
| WComp | Attendere il completamento | Attendere la notifica. Deve essere ricevuta una notifica di completamento della chiamata.<br /> Passare a Comp<br /> | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Fine | 




 

Comportamento del server


| State | State Name | Azione | 
|-------|------------|--------|
| D | Dispatch | La chiamata viene inviata dal runtime RPC Vai a P<br /> Per generare un errore irreversibile (durante l'esecuzione sul thread RPC): genera eccezione. Vai a Fine<br /> Per eseguire correttamente l'errore: passare a A<br /> | 
| P | Push | Effettuare un push<ul><li>Se l'operazione ha esito positivo, passare a WP</li><li>In caso di errore passare a Fine</li></ul>Per esito negativo: passare a A<br /> | 
| WP | Attendere il push | Attendere la notifica<ul><li>In caso di esito negativo per ottenere un completamento, passare a A</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e è necessario inviare altri dati, passare a P</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e non è necessario inviare altri dati, passare a NP</li><li>Se viene ricevuto un errore, passare a Comp</li></ul>Per esito negativo: passare a A<br /> | 
| NP | Null Push | Push di 0 byte<ul><li>se l'operazione ha esito positivo, passare a WNP</li><li>in caso di errore passare a Comp</li></ul>Per esito negativo: passare a A<br /> | 
| WNP | Attendere il push Null | Attendere la notifica<ul><li>In caso di esito negativo per ottenere un completamento, passare a A</li><li>Se viene ricevuto un errore, passare a Comp</li><li>Se viene ricevuto un esito positivo, passare a Comp</li></ul> | 
| A | Interrompere la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; Vai a Fine | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; Vai a Fine | 
| Fine | 




 

## <a name="in-out-pipe"></a>IN-OUT Pipe

Comportamento del client


| State | State Name | Azione | 
|-------|------------|--------|
| C | Effettuare la chiamata | Effettuare la chiamata RPC<ul><li>Se l'operazione ha esito positivo, passare a WS</li><li>In eccezione passare a Fine</li></ul>Per esito negativo: passare a Can<br /> | 
| PS | Push | Effettuare un push<ul><li>In caso di errore passare a Fine</li><li>Se l'operazione ha esito positivo, passare a WS</li></ul>Per esito negativo: passare a Can<br /> | 
| WS | Attendere l'invio | Attendere la notifica<ul><li>Se non si ottiene una notifica, passare a Può</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un errore RpcSendComplete</strong></a> con esito positivo e è necessario inviare altri dati, passare a PS</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e non è necessario inviare altri dati, passare a NP</li><li>Se viene ricevuto un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>errore RpcCallComplete,</strong></a> passare a Comp</li></ul>Per esito negativo: passare a Can<br /> | 
| NP | Null Push | Push di 0 byte (push Null)<ul><li>In caso di errore passare a Fine</li><li>Se l'operazione ha esito positivo, passare a PL</li></ul>Per esito negativo: passare a Can<br /> | 
| PL | Pull | Effettuare un pull<ul><li>In caso di errore passare a Fine</li><li>Se l'operazione ha esito positivo e il completamento sincrono con byte non zero letti, passare a PL</li><li>In caso di esito positivo e completamento sincrono con zero byte letti (pull Null) passare a WComp</li><li>In base all'esito positivo e al completamento asincrono (ERROR_IO_PENDING restituito) passare a WPL</li></ul>Per esito negativo: passare a Can<br /> | 
| WPL | Attendere il pull | Attendere la notifica<ul><li>In caso di esito negativo, passare a Can</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un errore RpcReceiveComplete,</strong></a> passare a Can</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcReceiveComplete</strong></a> con byte di lettura diverso da zero, passare a PL</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcReceiveComplete</strong></a> con zero byte di lettura, passare a Comp</li><li>Se viene ricevuto un errore, è possibile</li></ul>Per avere esito negativo: passare a Can<br /> | 
| Capacità | Annullare la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go a WComp<br /> | 
| WComp | Attendere il completamento | Attendere la notifica. Deve essere ricevuta la notifica CallComplete.<br /> Passare a Comp<br /> | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End<br /> | 
| Fine | 




 

Comportamento del server


| State | State Name | Azione | 
|-------|------------|--------|
| D | Dispatch | La chiamata viene inviata dal runtime RPCGo to PL<br /> Per generare un errore irreversibile (durante l'esecuzione nel thread RPC): genera un'eccezione. vai a Fine<br /> Per eseguire correttamente l'errore: passare a A<br /> | 
| PL | Pull | Eseguire un pull<ul><li>In caso di errore passare a Fine</li><li>In corrispondenza dell'esito positivo e del completamento sincrono con byte di lettura diverso da zero, passare a PL</li><li>In caso di esito positivo e completamento sincrono con zero byte letti (pull Null) passare a PS</li><li>In esito positivo e completamento asincrono (ERROR_IO_PENDING restituito) passare a WPL</li></ul>Per avere esito negativo: passare ad A<br /> | 
| WPL | Attendere il pull | Attendere la notifica<ul><li>In caso di esito negativo, passare ad A</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un errore RpcReceiveComplete,</strong></a> passare ad A</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcReceiveComplete</strong></a> con byte di lettura diverso da zero, passare a PL</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcReceiveComplete</strong></a> con zero byte di lettura, passare a PS</li><li>Se viene ricevuto un errore, passare A</li></ul>Per avere esito negativo: passare ad A<br /> | 
| PS | Push | Eseguire un push<ul><li>Al termine, passare a WPS</li><li>In caso di errore passare a Fine</li></ul>Per avere esito negativo: passare ad A<br /> | 
| WPS | Attendere il push | Attendere la notifica<ul><li>In caso di esito negativo, passare ad A</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e è necessario inviare altri dati, passare a PS</li><li>Se viene ricevuto <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un esito positivo RpcSendComplete</strong></a> e non è necessario inviare altri dati, passare a NP</li><li>Se viene ricevuto un errore, passare a Comp</li></ul>Per avere esito negativo: passare ad A<br /> | 
| NP | Null Push | Push di 0 byte<ul><li>in esito positivo passare a WNP</li><li>in caso di errore passare a Comp</li></ul>Per avere esito negativo: passare ad A<br /> | 
| WNP | Attendere il push Null | Attendere la notifica<ul><li>In caso di esito negativo, passare ad A</li><li>Se viene ricevuto un errore, passare a Comp</li><li>Se viene ricevuto un esito positivo, fare clic su Comp</li></ul><br /> | 
| A | Interrompere la chiamata | Chiamare <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; vai a Fine | 
| Comp | Completion | Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; vai a Fine | 
| Fine | 




 

 

 





