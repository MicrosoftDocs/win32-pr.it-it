---
description: I messaggi del dispositivo sono messaggi di sistema che notificano alle applicazioni e ad altre funzionalità degli eventi di modifica del dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Messaggi del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a26666ab0f7675da02e70d53ffd8aec5040a0482a0a2cdc71279fcaeca8ca92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053510"
---
# <a name="device-messages"></a>Messaggi del dispositivo

I messaggi del dispositivo sono messaggi di sistema che notificano alle applicazioni e ad altre funzionalità degli eventi di modifica del dispositivo. Questi eventi si verificano ogni volta che il sistema rileva una modifica all'hardware del sistema, ad esempio quando l'utente ancora e disanca un computer portatile oppure inserisce o rimuove un dispositivo, ad esempio una scheda PCMCIA. Gli eventi del dispositivo possono verificarsi durante l'esecuzione del sistema o quando il sistema riprende l'operazione dopo la sospensione temporanea.

Per garantire che le applicazioni non perdano i dati quando i dispositivi diventano non disponibili, il sistema monitora la configurazione hardware e invia messaggi del dispositivo alle applicazioni per notificare le modifiche e offrire loro la possibilità di prepararsi per le modifiche prima che si verifichino.

Per ogni evento del dispositivo, il sistema trasmette un [**messaggio \_ DEVICECHANGE WM**](wm-devicechange.md) a tutte le applicazioni. In questo messaggio il *parametro wParam* identifica il tipo di evento [del](device-event-types.md) dispositivo e il *parametro lParam* è un puntatore a dati specifici dell'evento.

 

 



