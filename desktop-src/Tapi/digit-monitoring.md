---
description: Il monitoraggio delle cifre monitora la chiamata per le cifre.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Monitoraggio delle cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306331"
---
# <a name="digit-monitoring"></a>Monitoraggio delle cifre

Il monitoraggio delle cifre monitora la chiamata per le cifre. TAPI consente la segnalazione di cifre in base a due metodi (modalità digit):

-   Le cifre a impulsi vengono segnalate come sequenze impulsi o rotanti. Per il rilevamento, questi impulsi si manifestano come nient'altro che sequenze di clic acustici. Le cifre di impulso valide sono comprese tra' 0' è 9'.
-   Le cifre DTMF vengono segnalate come toni DTMF (Dual Tone Multiple Frequency). Le cifre DTMF valide sono comprese tra' 0' è 9',' A '. ' B ',' c',' d',' \* ' è \# '. È possibile monitorare sia l'inizio che il bordo inferiore delle cifre DTMF.

Un'applicazione può abilitare o disabilitare il monitoraggio delle cifre per una chiamata specificata con [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits). Quando il monitoraggio dei numeri è abilitato, le cifre rilevate fanno sì che l'applicazione riceva una notifica con il messaggio di [**riga \_ MONITORDIGITS**](line-monitordigits.md) . Questo messaggio fornisce l'handle di chiamata su cui è stata rilevata la cifra, nonché il valore della cifra e la modalità di cifra. L'ambito del monitoraggio delle cifre è associato alla durata della chiamata. Il monitoraggio delle cifre su una chiamata termina non appena la chiamata si *disconnette* o diventa *inattiva*.

 

 



