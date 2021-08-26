---
title: Ricezione della risposta asincrona
description: Dopo aver ricevuto una notifica che il server ha inviato una risposta, il client chiama RpcAsyncCompleteCall con l'handle asincrono in modo che possa ricevere la risposta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24500e176a7c5a36342b4188e687c557d48646deef1de39845257d8e04ff7c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018821"
---
# <a name="receiving-the-asynchronous-reply"></a>Ricezione della risposta asincrona

Dopo aver ricevuto una notifica che il server ha inviato una risposta, il client chiama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) con l'handle asincrono in modo che possa ricevere la risposta. Al **termine di RpcAsyncCompleteCall,** il *parametro Reply* punta a un buffer contenente il valore restituito della funzione remota. Tutti i buffer forniti dal programma client come out o in , i parametri out per la funzione remota asincrona \[ [](/windows/desktop/Midl/out-idl) \] contengono dati \[ [](/windows/desktop/Midl/in)  \] validi. Se il client chiama **RpcAsyncCompleteCall** prima che il server abbia inviato la risposta, tale chiamata avrà esito negativo e restituirà il valore RPC \_ S \_ ASYNC \_ CALL \_ PENDING.

Se il programma client usa porte o eventi di completamento I/O per la notifica, deve chiamare [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per rilasciare la porta o gestirla quando non ne ha più bisogno.

 

 