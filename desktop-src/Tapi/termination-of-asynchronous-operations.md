---
description: Quando un'applicazione chiama la funzione lineClose con una o più operazioni asincrone in attesa, TAPI può indirizzare il provider di servizi per terminare le operazioni asincrone associate a una chiamata.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Chiusura di operazioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ed2acb0f442e5f4f07427f0e224d7a288087d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319848"
---
# <a name="termination-of-asynchronous-operations"></a>Chiusura di operazioni asincrone

Quando un'applicazione chiama la funzione [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) con una o più operazioni asincrone in attesa, TAPI può indirizzare il provider di servizi per terminare le operazioni asincrone associate a una chiamata, a seconda che l'applicazione sia l'unico proprietario della chiamata e disponga dell'unico handle della chiamata.

Se l'applicazione è l'unico proprietario di una chiamata, TAPI chiama [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (a seconda del provider) per ogni chiamata. Il provider di servizi deve verificare la presenza di eventuali operazioni asincrone in sospeso associate alla chiamata eliminata. Se esiste un'operazione in sospeso, il provider di servizi deve intraprendere l'azione appropriata, eventualmente terminando l'operazione in corso.

Se l'applicazione ha l'unico handle per una chiamata, ovvero non sono presenti altri proprietari o monitoraggi, TAPI chiama la funzione [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Il provider di servizi deve considerare questa chiamata come indicazione assoluta che è necessario abbandonare le operazioni asincrone in sospeso. Il provider di servizi deve garantire un completamento ordinato della chiamata e deve chiamare la funzione di callback di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) per tutte le operazioni asincrone in attesa, specificando il \_ valore di errore OPERATIONFAILED di LINEERR. Se TAPI ha precedentemente chiamato la funzione [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) , chiama **TSPI \_ lineCloseCall** immediatamente dopo che il provider di servizi ha restituito l'altra chiamata. non attende il completamento dell'operazione asincrona associata alla funzione TSPI **\_ lineDrop** .

Se l'applicazione non è l'unico proprietario della chiamata, TAPI non chiama [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop). Se l'applicazione non ha l'unico handle per la chiamata, TAPI non chiama la funzione [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Se l'applicazione non è né l'unico proprietario né l'unico proprietario di un handle per la chiamata, TAPI non invia alcuna notifica al provider di servizi e pertanto tutte le operazioni asincrone in sospeso rimangono intatte. Ciò significa che tali applicazioni non possono terminare le operazioni asincrone avviate tramite la funzione [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) . Tuttavia, poiché ogni operazione asincrona richiede che l'applicazione chiamante sia un proprietario della chiamata, la probabilità che un'applicazione non sia in grado di terminare le operazioni asincrone è molto rara. In caso contrario, gli altri proprietari delle chiamate devono assumersi la responsabilità della disposizione delle chiamate (s).

Se TAPI chiama [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop), il provider di servizi deve inviare un \_ messaggio inattivo LINECALLSTATE per la chiamata associata (a meno che [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) non venga chiamato per primo) in modo che i monitoraggi della chiamata possano effettuare la pulizia. Quando l'ultimo monitoraggio ha chiamato la funzione [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) , TAPI chiama la funzione **TSPI \_ lineCloseCall** ; tutte le operazioni in sospeso devono essere completate o terminate e il [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) è stato chiamato, come descritto in precedenza.

 

 
