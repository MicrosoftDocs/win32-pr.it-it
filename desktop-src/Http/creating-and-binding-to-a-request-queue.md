---
title: Creazione e associazione a una coda di richieste
description: Una coda di richieste è una coda del servizio che include richieste in sospeso per un'applicazione specifica.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396470"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Creazione e associazione a una coda di richieste

Una coda di richieste è una coda del servizio che include richieste in sospeso per un'applicazione specifica. Un'applicazione crea la coda delle richieste indipendentemente dal gruppo di URL o dalla sessione del server chiamando la funzione [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) e imposta le proprietà della coda delle richieste chiamando la funzione [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) . Queste proprietà sono il livello di dettaglio delle risposte 503, la lunghezza massima della coda e lo stato dell'attività.

Per fare in modo che le richieste vengano instradate alla propria coda di richieste, l'applicazione associa il gruppo di URL creato come parte della configurazione della fase di [esecuzione](run-time-configuration.md) alla coda chiamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** specificato nel parametro *Property* . Le richieste in ingresso dagli URL nel gruppo vengono quindi indirizzate alla coda di richieste specificata.

 

 




