---
description: I messaggi del dispositivo sono messaggi di sistema che notificano le applicazioni e altre funzionalità degli eventi di modifica del dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Messaggi del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305084"
---
# <a name="device-messages"></a>Messaggi del dispositivo

I messaggi del dispositivo sono messaggi di sistema che notificano le applicazioni e altre funzionalità degli eventi di modifica del dispositivo. Questi eventi si verificano ogni volta che il sistema rileva una modifica all'hardware del sistema, ad esempio quando l'utente ancora e Disancora un computer portatile, oppure inserisce o rimuove un dispositivo, ad esempio una scheda PCMCIA. Gli eventi del dispositivo possono verificarsi mentre il sistema è in esecuzione o quando il sistema riprende l'operazione dopo la sospensione temporanea.

Per garantire che le applicazioni non perdano i dati quando i dispositivi non sono più disponibili, il sistema monitora la configurazione hardware e invia messaggi al dispositivo alle applicazioni per notificare le modifiche e fornire loro la possibilità di preparare le modifiche prima che si verifichino.

Per ogni evento del dispositivo, il sistema trasmette un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) a tutte le applicazioni. In questo messaggio, il parametro *wParam* identifica il [tipo di evento del dispositivo](device-event-types.md) e il parametro *lParam* è un puntatore a dati specifici dell'evento.

 

 



