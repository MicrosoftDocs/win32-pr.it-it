---
description: La specifica TSPI è strettamente correlata alle specifiche per TAPI 2,2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Confronto generale con TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce81d569d042cdd3eeb87088b1b7027858ca806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312716"
---
# <a name="overall-comparison-with-tapi"></a>Confronto generale con TAPI

La specifica TSPI è strettamente correlata alle specifiche per TAPI 2,2 (TAPI/C). La maggior parte delle funzioni in una ha una funzione corrispondente nell'altra. La corrispondenza consueta è la seguente:

-   Le funzioni TSPI hanno gli stessi nomi delle funzioni TAPI, con la differenza che vengono anteposti a "**TSPI \_**". Ad esempio, la funzione TAPI [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) corrisponde alla funzione TSPI [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept).
-   Le routine che consentono l'operazione asincrona inseriscono un parametro *dwRequestID* di tipo [drv \_ RequestId](drv-requestid.md) come primo parametro. Questo parametro specifica il valore da restituire per indicare l'operazione asincrona e per segnalare il completamento asincrono.
-   i parametri *hCall* di tipo hCall vengono sostituiti con parametri *HdCall* di tipo [HDRVCALL](hdrvline.md), che indicano l'handle del provider di servizi per la chiamata.
-   i parametri *hLine* di tipo hLine vengono sostituiti con parametri *HdLine* di tipo [HDRVLINE](hdrvline.md), che indica l'handle del provider di servizi per la riga.
-   i parametri *hPhone* di tipo hPhone vengono sostituiti con parametri *HdPhone* di tipo [HDRVPHONE](hdrvphone.md), che indica l'handle del provider di servizi per il telefono.
-   Le procedure che creano una nuova chiamata, ad esempio [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), sostituiscono un singolo parametro *lphCall* con due parametri: un *htCall* di tipo [HTAPICALL](htapicall.md) parametro che passa l'handle TAPI per la chiamata e un *lphdCall* di tipo LPHDRVCALL che indica la posizione in cui il provider di servizi deve scrivere il nuovo handle per la chiamata. Una suddivisione simile di parametri si verifica in [**TSPI \_ LineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   A livello di TSPI, non esiste alcuna nozione di "privilegio" associato agli handle del dispositivo. Inoltre, a livello di API, ogni applicazione che dispone di un handle di dispositivo o di chiamata ha un handle diverso, ma TAPI li unisce in un singolo handle nel lato del provider di servizi. Di conseguenza, i codici di errore e i messaggi di stato relativi ai privilegi e al numero di client che usano un dispositivo non vengono visualizzati a livello di TSPI.

Il set di funzioni TAPI non esegue il mapping uno a uno nel set di funzioni TSPI. In particolare, le funzioni correlate al privilegio, alla conversione dei numeri di telefono e alla comunicazione tra applicazioni vengono gestite da TAPI e non hanno funzione corrispondente in TSPI. Altre funzioni, ad esempio quelle usate per la configurazione e l'inizializzazione del provider di servizi, non hanno funzioni corrispondenti in TAPI.

 

 
