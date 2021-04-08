---
title: Thread safety
description: Tutte le funzioni in questa API sono sicure da chiamare simultaneamente da thread diversi. Tuttavia, ogni oggetto passato come parametro alle funzioni ha un comportamento di threading specifico, come descritto di seguito.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Servizi Web di thread safety per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734850"
---
# <a name="thread-safety"></a>Thread safety

Tutte le funzioni in questa API sono sicure da chiamare simultaneamente da thread diversi. Tuttavia, ogni oggetto passato come parametro alle funzioni ha un comportamento di threading specifico, come descritto di seguito.


Gli handle seguenti sono a thread singolo e non supportano operazioni simultanee per una particolare istanza:

-   [\_heap WS](ws-heap.md)
-   [\_messaggio WS](ws-message.md)
-   [\_buffer WS XML \_](ws-xml-buffer.md)
-   [\_lettore XML \_ WS](ws-xml-reader.md)
-   [\_writer XML \_ WS](ws-xml-writer.md)
-   [\_errore WS](ws-error.md)
-   [\_contesto dell'operazione WS \_](ws-operation-context.md)
-   [\_criteri WS](ws-policy.md)
-   [\_metadati WS](ws-metadata.md)
-   [\_token di sicurezza WS \_](ws-security-token.md)
-   [\_contesto di sicurezza WS \_](ws-security-context.md)

Gli handle seguenti sono a thread libero e supportano operazioni simultanee per una particolare istanza:

-   [\_canale WS](ws-channel.md)
-   [\_listener WS](ws-listener.md)
-   [\_host del servizio WS \_](ws-service-host.md)
-   [\_proxy servizio \_ WS](ws-service-proxy.md)

Per tutti questi handle, il Threading viene definito in termini di operazioni (non chiamate di funzione). Un'operazione è definita diversamente per le funzioni richiamate in modo sincrono rispetto alle funzioni richiamate in modo asincrono

-   Per le funzioni richiamate in modo sincrono, l'operazione è in sospeso durante l'esecuzione della funzione.
-   Per le funzioni richiamate in modo asincrono, se la funzione restituisce un codice restituito diverso da **WS \_ S \_ Async** , l'operazione è in sospeso durante l'esecuzione della funzione. Se la funzione restituisce **WS \_ S \_ Async** , tuttavia, l'operazione è in sospeso fino a quando non viene richiamato il [**\_ \_ callback di WS asincrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) . Per ulteriori informazioni sulla chiamata di funzioni in modo asincrono, vedere l'argomento relativo al [modello asincrono](asynchronous-model.md) . Per i codici di errore, vedere [valori restituiti dei servizi Web Windows](windows-web-services-return-values.md).

Il mancato completamento del contratto di threading per un oggetto comporterà un comportamento indefinito.

 

 




