---
description: Il monitoraggio delle cifre monitora la chiamata per le cifre.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Monitoraggio delle cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6768aa73cde3e9eaf05ea27ef1bb01bbd9c19787c01931d0640737bf365ee6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866749"
---
# <a name="digit-monitoring"></a>Monitoraggio delle cifre

Il monitoraggio delle cifre monitora la chiamata per le cifre. TAPI consente di segnalare le cifre in base a due metodi (modalità cifra):

-   Le cifre di pulsazione vengono segnalate come sequenze di pulsazioni o di numeri di sequenza. Per il rilevamento, questi pulsazioni si manifestano solo come sequenze di clic udibili. Le cifre di pulsazione valide sono comprese tra '0' e '9'.
-   Le cifre DTMF vengono segnalate come toni DTMF (Dual Tone Multiple Frequency). Le cifre DTMF valide sono comprese tra '0' e '9', 'A'. 'B', 'C', 'D', \* ' ' e ' \# '. È possibile monitorare sia l'inizio che il bordo inferiore delle cifre DTMF.

Un'applicazione può abilitare o disabilitare il monitoraggio delle cifre in una chiamata specificata [**con lineMonitorDigits.**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) Quando il monitoraggio delle cifre è abilitato, le cifre rilevate determinano la notifica dell'applicazione con il [**messaggio LINE \_ MONITORDIGITS.**](line-monitordigits.md) Questo messaggio fornisce l'handle di chiamata in cui è stata rilevata la cifra, nonché il valore della cifra e la modalità cifra. L'ambito del monitoraggio delle cifre è associato alla durata della chiamata. Il monitoraggio delle cifre in una chiamata termina non appena la chiamata *si disconnette* o diventa *inattiva.*

 

 



