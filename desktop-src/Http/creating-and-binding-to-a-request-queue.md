---
title: Creazione e associazione a una coda di richieste
description: Una coda di richieste è una coda del servizio che contiene le richieste in sospeso per un'applicazione specifica.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c3a36fbbb9a8bcaa1c4e708240e99c276b09448ca56615df7da3d2cdf26836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914281"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Creazione e associazione a una coda di richieste

Una coda di richieste è una coda del servizio che contiene le richieste in sospeso per un'applicazione specifica. Un'applicazione crea la coda di richieste indipendentemente dal gruppo di URL o dalla sessione del server chiamando la funzione [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) e imposta le proprietà della coda di richiesta chiamando la [**funzione HttpSetRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) Queste proprietà sono il livello di dettaglio di 503 risposte, la lunghezza massima della coda e lo stato dell'attività.

Per fare in modo che le richieste siano indirizzate alla coda di [](run-time-configuration.md) richieste, l'applicazione associa il gruppo di URL creato come parte della configurazione in fase di esecuzione alla coda chiamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** specificato nel parametro *Property.* Le richieste in ingresso dagli URL nel gruppo vengono quindi indirizzate alla coda di richieste specificata.

 

 




