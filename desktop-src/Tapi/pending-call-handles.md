---
description: Un provider di servizi è necessario per creare uno o più handle di chiamata (variabili di tipo HDRVCALL) ogni volta che TAPI chiama una delle funzioni seguenti.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Handle di chiamata in sospeso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d082c0b9111d6d58debacec01d20ffe9af2d024aafd61b3f1085267e62d3d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518590"
---
# <a name="pending-call-handles"></a>Handle di chiamata in sospeso

Un provider di servizi è necessario per creare uno o più handle di chiamata (variabili di tipo [HDRVCALL)](hdrvline.md)ogni volta che TAPI chiama una di queste funzioni: [**TSPI \_ lineMakeCall,**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) [**TSPI \_ lineCompleteTransfer,**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer) [**TSPI \_ lineForward,**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward) [**TSPI \_ linePickup,**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup) [**TSPI \_ linePrepareAddToConference,**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference) [**TSPI \_ lineSetupConference,**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference) [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)e [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Quando un provider di servizi riceve una chiamata di questo tipo, deve impostare la variabile fornita da TAPI sul valore dell'handle prima di restituire dalla chiamata. TAPI considera questo "handle di chiamata in sospeso" come provvisoriamente valido. Quando il provider di servizi crea effettivamente la chiamata, deve chiamare il callback [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) per convalidare formalmente l'handle.

Se TAPI chiama la funzione [**\_ lineCloseCall TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) prima che il provider di servizi convalidi formalmente un handle di chiamata in sospeso, il provider di servizi deve arrestare tutte le ulteriori elaborazioni associate all'handle di chiamata e chiamare la funzione di callback [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) usando il valore di errore LINEERR \_ OPERATIONFAILED.

 

 
