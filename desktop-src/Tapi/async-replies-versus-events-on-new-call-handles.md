---
description: TSPI include una serie di operazioni che avviano la durata di un handle di chiamata.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Risposte asincrone rispetto agli eventi sui nuovi handle di chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883246"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a>Risposte asincrone rispetto agli eventi sui nuovi handle di chiamata

TSPI include una serie di operazioni che avviano la durata di un handle di chiamata. Se il provider di servizi restituisce l'ESITo positivo di tale operazione, deve compilare l'handle opaco di tipo **HDRVCALL**, che usa per la nuova chiamata prima che venga restituito. TAPI non esegue mai operazioni sulla chiamata prima della ricezione [*del \_ processo di completamento*](/windows/win32/api/tspi/nc-tspi-async_completion) corrispondente. Se il provider di servizi restituisce un errore, l'handle diventa automaticamente non valido (ovvero senza [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)). In pratica, TAPI considera l'handle come "non ancora valido" fino al completamento asincrono.

Il provider di servizi deve anche considerare l'handle come "non ancora valido" fino a quando non viene ricevuta la procedura di [*completamento \_*](/windows/win32/api/tspi/nc-tspi-async_completion) corrispondente. In altre parole, non deve eseguire alcuna funzione [*di \_ evento line*](/windows/win32/api/tspi/nc-tspi-lineevent) per la nuova chiamata o includerla nei conteggi delle chiamate nei messaggi o nelle strutture dei dati di stato per la riga.

Il livello TAPI è conforme anche a queste restrizioni del ciclo di vita; un nuovo handle di chiamata non viene restituito né valido fino a quando non viene inviato il messaggio di [**\_ risposta alla riga**](./line-reply.md) corrispondente e nessun evento per la nuova chiamata viene recapitato all'applicazione fino al termine del messaggio di risposta della riga \_ .

Di seguito sono riportate le operazioni TSPI a cui si applica questo principio di "durata iniziale":

-   [**\_LINECOMPLETETRANSFER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**\_LINEFORWARD TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**\_LINEMAKECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**\_LINEPICKUP TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**\_LINEPREPAREADDTOCONFERENCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**\_LINESETUPCONFERENCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**\_LINESETUPTRANSFER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**\_LINEUNPARK TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
