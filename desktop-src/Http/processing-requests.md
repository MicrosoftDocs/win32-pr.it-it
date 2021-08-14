---
title: Elaborazione delle richieste
description: L'elaborazione delle richieste include quattro passaggi.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea69ca4e431a4ff1841f08913b33bcb7dd57128f327aaeeac158fb62ea7a7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996251"
---
# <a name="processing-requests"></a>Elaborazione delle richieste

L'elaborazione delle richieste include quattro passaggi:

-   Ricezione di una richiesta
-   Gestione della richiesta
-   Invio della risposta
-   Annullamento di richieste che non possono essere elaborate

![Diagramma che mostra il ciclo di richieste di processo.](images/processloop.png)

## <a name="receiving-a-request"></a>Ricezione di una richiesta

L'API del server HTTP fornisce una struttura di richiesta per archiviare la richiesta in ingresso analizzata. Questa struttura viene allocata dall'applicazione e inizializzata quando viene ricevuta una richiesta in ingresso. L'applicazione chiama [**la funzione HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) per ricevere la richiesta. Se il buffer delle richieste è troppo piccolo per ricevere la richiesta, l'applicazione può aumentare le dimensioni del buffer e chiamare di nuovo **HttpReceiveHttpRequest** per ricevere l'intera richiesta.

Se la richiesta include i dati del corpo dell'entità da ricevere, le applicazioni chiamano [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con l'ID richiesta restituito nel *parametro pRequestBuffer* durante la chiamata a [**HttpReceiveHttpRequest.**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)

## <a name="handling-the-request"></a>Gestione della richiesta

L'applicazione esegue l'elaborazione specifica dell'applicazione della richiesta e formula una risposta. L'API del server HTTP non impone alcun timeout per questo processo.

## <a name="sending-the-response"></a>Invio della risposta

Al termine della gestione della richiesta e della formulazione della risposta, l'applicazione chiama la funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) per inviare la risposta. Se la risposta include i dati del corpo dell'entità da inviare, l'applicazione chiama [anche HttpSendResponseEntityBody.](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

## <a name="canceling-requests"></a>Annullamento di richieste

Dopo che l'applicazione ha ricevuto un ID richiesta dalla chiamata a [**HttpReceiveHttpRequest,**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)può annullare la richiesta in qualsiasi momento chiamando [HttpCancelHttpRequest.](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)

 

 




