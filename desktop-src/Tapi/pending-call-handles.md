---
description: Un provider di servizi è necessario per creare uno o più handle di chiamata (variabili di tipo HDRVCALL) ogni volta che TAPI chiama una delle funzioni seguenti.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Handle di chiamata in sospeso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c021ff10f2a1a812c46fb77663ac1a3a3a8d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306511"
---
# <a name="pending-call-handles"></a>Handle di chiamata in sospeso

Un provider di servizi è necessario per creare uno o più handle di chiamata (variabili di tipo [HDRVCALL](hdrvline.md)) ogni volta che TAPI chiama una di queste funzioni: [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), TSPI lineForward, [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), TSPI [**linePrepareAddToConference, TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), TSPI [**lineSetupTransfer e \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference) [**TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark) [**lineUnpark. \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer) [**\_**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward) Quando un provider di servizi riceve una chiamata di questo tipo, il provider di servizi deve impostare la variabile fornita da TAPI sul valore dell'handle prima di restituire la chiamata. Il valore di "handle di chiamata in sospeso" è considerato provvisoriamente valido. Quando il provider di servizi crea effettivamente la chiamata, deve chiamare il callback di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) per convalidare formalmente l'handle.

Se TAPI chiama la funzione [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) prima che il provider di servizi convalidi formalmente un handle di chiamata in sospeso, il provider di servizi deve arrestare tutte le altre elaborazioni associate all'handle di chiamata e chiamare la funzione di callback di [**\_ completamento asincrono**](/windows/win32/api/tspi/nc-tspi-async_completion) usando il valore di errore LINEERR \_ OPERATIONFAILED.

 

 
