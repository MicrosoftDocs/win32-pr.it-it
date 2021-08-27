---
description: Quando arriva una nuova sessione di comunicazione, alle applicazioni TAPI che hanno registrato un interesse per l'indirizzo e il tipo di supporto verrà inviata una notifica dell'evento.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Rispondere alla sessione avviata altrove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74554b48919f7532561bfdf0bab7a163a58fbeb3734dc15e4a8d7e0869dad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072851"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Rispondere alla sessione avviata altrove

Quando arriva una nuova sessione di comunicazione, alle [](address-ovr.md) applicazioni [](media-type-ovr.md) TAPI che hanno registrato un interesse per l'indirizzo e il tipo di supporto verrà inviata una [notifica dell'evento](event-notification.md). A una sola applicazione verranno offerti privilegi [di proprietà](privilege-ovr.md) per la sessione. Questa applicazione non può rifiutare la sessione.

Viene offerto lo stato di chiamata iniziale di una sessione in ingresso. Mentre la chiamata è nello stato di offerta, un'applicazione può ottenere informazioni come la modalità di accesso e il motivo della chiamata, se i provider di servizi hanno fornito queste informazioni ed è disponibile. Alcune informazioni sulle chiamate potrebbero non essere immediatamente disponibili, ad esempio l'ID chiamante.

Sono disponibili sei risposte di base a una sessione offerta: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff,](handoffs-ovr.md) [drop,](drop-ovr.md) [forward](forward-ovr.md)e [redirect](redirect-ovr.md). A seconda del provider di servizi, il set completo di queste operazioni potrebbe non essere disponibile.

 

 



