---
description: L'installazione di un nuovo provider di servizi è altamente specifica del dispositivo e del sistema operativo, quindi i dettagli non sono inclusi nell'ambito di questo SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installazione e inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15dc5d9d93ce33ac13a04aec3abd7d49fec3ed2ece3cce691d47c0d617bacd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003539"
---
# <a name="installation-and-initialization"></a>Installazione e inizializzazione

L'installazione di un nuovo provider di servizi è altamente specifica del dispositivo e del sistema operativo, quindi i dettagli non sono inclusi nell'ambito di questo SDK. In generale, l'obiettivo dell'installazione è la configurazione del provider di servizi per l'ambiente di comunicazione corrente. Ciò comporta in genere voci del Registro di sistema e l'impostazione delle dipendenze del servizio.

L'inizializzazione di un provider di servizi di telefonia inizia con la negoziazione della versione. Per [una descrizione della negoziazione della](tspi-versioning.md) versione e della versione corrente, vedere Controllo delle versioni TSPI.

TAPI chiama quindi [**\_ providerInit TSPI,**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)che passa al provider un puntatore a una funzione di callback usata per segnalare lo stato di avanzamento delle funzioni asincrone. Il provider di servizi di configurazione restituisce un conteggio dei dispositivi line e phone associati all'identificatore del dispositivo corrente.

In genere, il passaggio successivo sarà l'inventario delle risorse, eseguito da TAPI richiamando [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) e [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). È previsto che il provider di servizi inserisca gli elementi delle strutture di dati coinvolte che riguardano le funzionalità del dispositivo e della sessione supportate.

TAPI raccoglie informazioni dalle varie applicazioni relative ai requisiti di notifica degli eventi e indica al TSP di usare [**\_ lineSetDefaultMediaDetection TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) per indicare quali tipi di supporti rilevare per una riga e [**\_ lineSetStatusMessages TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) per indicare quali eventi di riga e indirizzo devono essere segnalati.

 

 
