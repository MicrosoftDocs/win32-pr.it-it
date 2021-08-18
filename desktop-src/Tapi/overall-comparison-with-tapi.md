---
description: La specifica TSPI è strettamente correlata alle specifiche per TAPI 2.2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Confronto generale con TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecedd5a53fd30e2a49b6d44e90d30f86ff8469f002166ca3328f3146a2748b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002809"
---
# <a name="overall-comparison-with-tapi"></a>Confronto generale con TAPI

La specifica TSPI è strettamente correlata alle specifiche per TAPI 2.2 (TAPI/C). La maggior parte delle funzioni in una ha una funzione corrispondente nell'altra. La corrispondenza consueta è la seguente:

-   Le funzioni TSPI hanno gli stessi nomi delle funzioni TAPI, ad eccezione del fatto che sono precedute da "**TSPI \_**". Ad esempio, la riga della funzione [**TAPIAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) corrisponde alla funzione [**TSPI \_ TSPI lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept).
-   Le procedure che consentono l'operazione asincrona inseriscono un parametro *dwRequestID* di tipo [DRV \_ REQUESTID](drv-requestid.md) come primo parametro. Questo parametro specifica il valore da restituire per indicare l'operazione asincrona e per segnalare il completamento asincrono.
-   *I parametri hCall* di tipo HCALL vengono sostituiti con i parametri *hdCall* di tipo [HDRVCALL,](hdrvline.md)che indicano l'handle del provider di servizi per la chiamata.
-   *I parametri hLine* di tipo HLINE vengono sostituiti con i parametri *hdLine* di tipo [HDRVLINE,](hdrvline.md)che indicano l'handle del provider di servizi per la riga.
-   *I parametri hPhone* di tipo HPHONE vengono sostituiti con i parametri *hdPhone* di tipo [HDRVPHONE,](hdrvphone.md)che indicano l'handle del provider di servizi per il telefono.
-   Le procedure che creano una nuova chiamata, ad esempio [**\_ lineMakeCall TSPI,**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)sostituiscono un singolo parametro *lphCall* con due parametri: *un parametro htCall* di tipo [HTAPICALL](htapicall.md) che passa l'handle TAPI per la chiamata e un *lphdCall* di tipo LPHDRVCALL che indica la posizione in cui il provider di servizi deve scrivere il nuovo handle per la chiamata. Una suddivisione simile dei parametri si verifica in [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   A livello TSPI, non esiste alcuna nozione di "privilegio" associato agli handle del dispositivo. Inoltre, a livello di API, ogni applicazione che dispone di un handle di dispositivo o di chiamata ha un handle diverso, ma TAPI li unisce in un unico handle sul lato provider di servizi. Di conseguenza, i codici di errore e i messaggi di stato relativi ai privilegi e al numero di client che usano un dispositivo non vengono visualizzati a livello TSPI.

Il set di funzioni TAPI non esegue il mapping uno a uno al set di funzioni TSPI. In particolare, le funzioni correlate ai privilegi, alla traduzione dei numeri di telefono e alla comunicazione tra applicazioni vengono gestite da TAPI e non hanno alcuna funzione corrispondente in TSPI. Altre funzioni, ad esempio quelle usate per la configurazione e l'inizializzazione del provider di servizi, non hanno funzioni corrispondenti in TAPI.

 

 
