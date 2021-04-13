---
title: Ricezione della risposta asincrona
description: Dopo la notifica che il server ha inviato una risposta, il client chiama RpcAsyncCompleteCall con l'handle asincrono in modo che possa ricevere la risposta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399601"
---
# <a name="receiving-the-asynchronous-reply"></a>Ricezione della risposta asincrona

Dopo la notifica che il server ha inviato una risposta, il client chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) con l'handle asincrono in modo che possa ricevere la risposta. Quando **RpcAsyncCompleteCall** è stato completato correttamente, il parametro *Reply* punta a un buffer che contiene il valore restituito della funzione remota. Tutti i buffer forniti dal programma client come \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ [**in**](/windows/desktop/Midl/in), i parametri **out** \] per la funzione remota asincrona contengono dati validi. Se il client chiama **RpcAsyncCompleteCall** prima dell'invio della risposta da parte del server, la chiamata avrà esito negativo e restituirà un valore della \_ \_ chiamata asincrona RPC \_ \_ in sospeso.

Se il programma client usa porte o eventi di completamento di I/O per la notifica, deve chiamare [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per rilasciare la porta o il punto di gestione quando non è più necessario.

 

 