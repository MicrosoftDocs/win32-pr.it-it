---
title: Thread safety
description: Tutte le funzioni in questa API sono sicure da chiamare contemporaneamente da thread diversi. Tuttavia, ogni oggetto passato come parametro alle funzioni ha un comportamento di threading specifico, come descritto di seguito.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Servizi Web thread safety per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25528f3315fcfae95d07d973d4743548eb35ec84bf754fdaafe067bcaccc56f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054461"
---
# <a name="thread-safety"></a>Thread safety

Tutte le funzioni in questa API sono sicure da chiamare contemporaneamente da thread diversi. Tuttavia, ogni oggetto passato come parametro alle funzioni ha un comportamento di threading specifico, come descritto di seguito.


Gli handle seguenti sono a thread singolo e non supportano operazioni simultanee per una determinata istanza:

-   [WS \_ HEAP](ws-heap.md)
-   [MESSAGGIO \_ WS](ws-message.md)
-   [WS \_ XML \_ BUFFER](ws-xml-buffer.md)
-   [LETTORE \_ XML WS \_](ws-xml-reader.md)
-   [WS \_ XML \_ WRITER](ws-xml-writer.md)
-   [ERRORE \_ WS](ws-error.md)
-   [CONTESTO \_ DELL'OPERAZIONE WS \_](ws-operation-context.md)
-   [CRITERI \_ WS](ws-policy.md)
-   [METADATI \_ WS](ws-metadata.md)
-   [TOKEN DI SICUREZZA WS \_ \_](ws-security-token.md)
-   [CONTESTO DI \_ SICUREZZA WS \_](ws-security-context.md)

Gli handle seguenti sono a thread libero e supportano operazioni simultanee per una determinata istanza:

-   [CANALE \_ WS](ws-channel.md)
-   [WS \_ LISTENER](ws-listener.md)
-   [HOST DEL SERVIZIO WS \_ \_](ws-service-host.md)
-   [PROXY DEL SERVIZIO WS \_ \_](ws-service-proxy.md)

Per tutti questi handle, il threading è definito in termini di operazioni (non chiamate di funzione). Un'operazione viene definita in modo diverso per le funzioni richiamate in modo sincrono rispetto alle funzioni richiamate in modo asincrono:

-   Per le funzioni richiamate in modo sincrono, l'operazione è in sospeso durante l'esecuzione della funzione.
-   Per le funzioni richiamate in modo asincrono, se la funzione restituisce un codice restituito diverso da **WS \_ S \_ ASYNC,** l'operazione è in sospeso durante l'esecuzione della funzione. Se la funzione restituisce **WS \_ S \_ ASYNC,** tuttavia, l'operazione è in sospeso fino a quando non viene richiamato [**WS \_ ASYNC \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) Per altre informazioni sulla chiamata asincrona delle funzioni, vedere [l'argomento Modello asincrono.](asynchronous-model.md) Per i codici di errore, [vedere Windows valori restituiti dei servizi Web.](windows-web-services-return-values.md)

La mancata esecuzione del contratto di threading per un oggetto comporta un comportamento non definito.

 

 




