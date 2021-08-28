---
description: Quando un'applicazione chiama la funzione lineClose con una o più operazioni asincrone in sospeso, TAPI può indirizzare il provider di servizi a terminare le operazioni asincrone associate a una chiamata.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Terminazione di operazioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d026754af75743314fbdbf7a2a3c82f9935f9b053f2a7186f095e4f452a0bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773001"
---
# <a name="termination-of-asynchronous-operations"></a>Terminazione di operazioni asincrone

Quando un'applicazione chiama la funzione [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) con una o più operazioni asincrone in sospeso, TAPI può indicare al provider di servizi di terminare le operazioni asincrone associate a una chiamata, a seconda che l'applicazione sia l'unico proprietario della chiamata e abbia l'unico handle per la chiamata.

Se l'applicazione è l'unico proprietario di una chiamata, TAPI chiama [**TSPI \_ lineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (a seconda del provider) per ogni chiamata. Il provider di servizi deve verificare la presenza di eventuali operazioni asincrone in sospeso associate alla chiamata da eliminare. Se esiste un'operazione in sospeso, il provider di servizi deve eseguire l'azione appropriata, eventualmente terminando l'operazione in corso.

Se l'applicazione ha l'unico handle per una chiamata , ovvero non sono presenti altri proprietari o monitoraggi, TAPI chiama la funzione [**\_ lineCloseCall TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) Il provider di servizi deve considerare questa chiamata come l'indicazione assoluta che le operazioni asincrone in sospeso devono essere abbandonate. Il provider di servizi deve garantire il completamento ordinato della chiamata e chiamare la funzione di callback [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) per tutte le operazioni asincrone in sospeso, specificando il valore di errore LINEERR \_ OPERATIONFAILED. Se TAPI chiama in precedenza la funzione [**\_ lineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop,**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) chiama **\_ lineCloseCall TSPI** immediatamente dopo che il provider di servizi viene restituito dall'altra chiamata. Non attende il completamento dell'operazione asincrona associata alla funzione **\_ lineDrop TSPI.**

Se l'applicazione non è l'unico proprietario della chiamata, TAPI non chiama [**\_ lineDropOnClose**](./tspi-linedroponclose.md) o [**\_ lineDrop TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) Se l'applicazione non ha l'unico handle per la chiamata, TAPI non chiama la [**funzione \_ lineCloseCall TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) Se l'applicazione non è l'unico proprietario né l'unico proprietario di un handle per la chiamata, TAPI non invia alcuna notifica al provider di servizi e pertanto tutte le operazioni asincrone in sospeso rimangono intatte. Ciò significa che tali applicazioni non possono terminare le operazioni asincrone avviate tramite la [**funzione lineClose.**](/windows/win32/api/tapi/nf-tapi-lineclose) Tuttavia, poiché ogni operazione asincrona richiede che l'applicazione che richiama sia un proprietario della chiamata, la probabilità che un'applicazione non sia in grado di terminare le operazioni asincrone è molto rara. In questo caso, gli altri proprietari delle chiamate devono assumersi la responsabilità della disposizione delle chiamate.

Se TAPI chiama [**TSPI \_ lineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop,**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)il provider di servizi deve inviare un messaggio LINECALLSTATE IDLE per la chiamata associata (a meno che non venga chiamato per primo \_ [**\_ lineCloseCall TSPI)**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) in modo che i monitoraggi nella chiamata possano eseguire la pulizia. Quando l'ultimo monitoraggio ha chiamato la funzione [**lineDeallocateCall,**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) TAPI chiama la funzione **\_ lineCloseCall TSPI.** Tutte le operazioni in sospeso devono essere completate o terminate e [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) chiamato, come descritto in precedenza.

 

 
