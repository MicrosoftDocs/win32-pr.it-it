---
title: Elaborazione delle richieste
description: Le richieste di elaborazione includono quattro passaggi.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "103885901"
---
# <a name="processing-requests"></a>Elaborazione delle richieste

Le richieste di elaborazione includono quattro passaggi:

-   Ricezione di una richiesta
-   Gestione della richiesta
-   Invio della risposta
-   Annullamento di richieste che non possono essere elaborate

![Diagramma che mostra il ciclo di richiesta di elaborazione.](images/processloop.png)

## <a name="receiving-a-request"></a>Ricezione di una richiesta

L'API server HTTP fornisce una struttura di richiesta per archiviare la richiesta in ingresso analizzata. Questa struttura viene allocata dall'applicazione e inizializzata quando viene ricevuta una richiesta in ingresso. L'applicazione chiama la funzione [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) per ricevere la richiesta. Se il buffer di richiesta è troppo piccolo per ricevere la richiesta, l'applicazione può aumentare le dimensioni del buffer e chiamare di nuovo **HttpReceiveHttpRequest** per ricevere l'intera richiesta.

Se la richiesta include dati del corpo dell'entità da ricevere, le applicazioni chiamano [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con l'ID richiesta restituito nel parametro *pRequestBuffer* durante la chiamata a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).

## <a name="handling-the-request"></a>Gestione della richiesta

L'applicazione esegue l'elaborazione della richiesta specifica dell'applicazione e formula una risposta. L'API server HTTP non impone alcun timeout per questo processo.

## <a name="sending-the-response"></a>Invio della risposta

Al termine della gestione della richiesta e della formulazione della risposta, l'applicazione chiama la funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) per inviare la risposta. Se la risposta include i dati del corpo dell'entità da inviare, l'applicazione chiama anche [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

## <a name="canceling-requests"></a>Annullamento di richieste

Dopo che l'applicazione ha ricevuto un ID richiesta dalla relativa chiamata a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), può in qualsiasi momento annullare la richiesta chiamando [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).

 

 




