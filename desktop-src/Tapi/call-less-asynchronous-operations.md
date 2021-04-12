---
description: Sono disponibili cinque operazioni asincrone che non sono correlate a una particolare chiamata.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Operazioni asincrone senza chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345696"
---
# <a name="call-less-asynchronous-operations"></a>Operazioni asincrone senza chiamata

Sono disponibili cinque operazioni asincrone che non sono correlate a una particolare chiamata. Le funzioni [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)e [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) di TAPI 2. x avviano queste operazioni. Se un'applicazione avvia una di queste operazioni asincrone e chiama [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), il provider di servizi potrebbe non ricevere alcuna indicazione che la funzione è stata abbandonata dall'applicazione. Questo problema può verificarsi se l'applicazione non è l'unica applicazione a cui è stata aperta la riga. Se l'applicazione chiama **lineClose** con una di queste operazioni in sospeso ed è l'unica applicazione con un handle alla riga, TAPI chiama la funzione [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) e il provider di servizi deve terminare l'operazione asincrona, chiamando la funzione di [*callback \_ proc proc*](/windows/win32/api/tspi/nc-tspi-async_completion) per ogni operazione in sospeso con il valore di \_ errore LINEERR OPERATIONFAILED.

 

 
