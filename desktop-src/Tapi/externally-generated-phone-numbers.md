---
description: Un provider di servizi può indicare numeri di telefono generati esternamente impostando i membri della struttura LINECALLINFO durante l'elaborazione della \_ funzione LINEGETCALLINFO TSPI.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Numeri di telefono generati esternamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751615"
---
# <a name="externally-generated-phone-numbers"></a>Numeri di telefono generati esternamente

Un provider di servizi può indicare i numeri di telefono generati esternamente, ovvero i numeri per le chiamate in uscita generate esternamente al computer, impostando i membri **DisplayableAddress**, **CalledParty** o [Comment](./comment-ovr.md) nella struttura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) durante l'elaborazione della funzione [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) . Se TAPI non ha salvato i propri dati per questi membri, lascia invariati i dati impostati dal provider di servizi. Se TAPI ha dati memorizzati nella cache per questi membri, TAPI aggiunge il testo alla fine della parte variabile della struttura **LINECALLINFO** e sovrascrive le dimensioni e l'offset che il provider di servizi ha inserito nella parte fissa.

Un provider di servizi può anche copiare un numero in uscita nel membro **CalledID** . Pertanto, le applicazioni di registrazione devono verificare il membro **CalledID** nelle chiamate in uscita se i membri **DisplayableAddress** e **CalledParty** sono vuoti.

 

 
