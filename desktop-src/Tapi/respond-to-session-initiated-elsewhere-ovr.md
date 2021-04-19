---
description: Quando arriva una nuova sessione di comunicazione, le applicazioni TAPI che hanno registrato un interesse per l'indirizzo e il tipo di supporto riceveranno una notifica degli eventi.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Rispondere a una sessione avviata altrove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319868"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Rispondere a una sessione avviata altrove

Quando arriva una nuova sessione di comunicazione, le applicazioni TAPI che hanno registrato un interesse per l' [Indirizzo](address-ovr.md) e il [tipo di supporto](media-type-ovr.md) riceveranno una [notifica degli eventi](event-notification.md). Alla sessione verranno offerti [privilegi](privilege-ovr.md) di proprietà a una sola applicazione. Questa applicazione non può rifiutare la sessione.

Lo stato di chiamata iniziale di una sessione in ingresso è offering. Mentre la chiamata è nello stato dell'offerta, un'applicazione può ottenere informazioni, ad esempio la modalità di porta e il motivo della chiamata, se i provider di servizi hanno fornito queste informazioni e sono disponibili. Alcune informazioni sulle chiamate potrebbero non essere immediatamente disponibili, ad esempio l'ID chiamante.

Sono disponibili sei risposte di base a una sessione offerta [: risposta](answer-ovr.md), [accettazione](accept-ovr.md), [consegna, rilascio](drop-ovr.md), [invio](forward-ovr.md)e [Reindirizzamento](redirect-ovr.md). [](handoffs-ovr.md) A seconda del provider di servizi, il set completo di queste operazioni potrebbe non essere disponibile.

 

 



