---
description: L'installazione di un nuovo provider di servizi è molto specifica per i dispositivi e il sistema operativo, quindi i dettagli non rientrano nell'ambito di questo SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installazione e inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317652"
---
# <a name="installation-and-initialization"></a>Installazione e inizializzazione

L'installazione di un nuovo provider di servizi è molto specifica per i dispositivi e il sistema operativo, quindi i dettagli non rientrano nell'ambito di questo SDK. In generale, l'obiettivo dell'installazione è la configurazione del provider di servizi per l'ambiente di comunicazione corrente. Questo in genere riguarda le voci del registro di sistema e l'impostazione delle dipendenze del servizio.

L'inizializzazione di un provider di servizi di telefonia inizia con la negoziazione della versione. Per una descrizione della negoziazione della versione e della versione corrente, vedere [controllo delle versioni di TSPI](tspi-versioning.md) .

TAPI chiama quindi [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), che passa al provider un puntatore a una funzione di callback utilizzata per segnalare lo stato di avanzamento delle funzioni asincrone. Il TSP restituisce un conteggio dei dispositivi line e Phone associati all'identificatore del dispositivo corrente.

In genere, il passaggio successivo sarà l'inventario delle risorse, condotto da TAPI che richiama [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) e [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Si prevede che il provider di servizi compilerà gli elementi delle strutture di dati che riguardano le funzionalità del dispositivo e della sessione supportate.

TAPI raccoglie informazioni dalle diverse applicazioni relative ai requisiti di notifica degli eventi e indica al TSP usando [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) di indicare quali tipi di supporti rilevare per una riga e [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) per indicare quali eventi di riga e di indirizzo devono essere segnalati.

 

 
