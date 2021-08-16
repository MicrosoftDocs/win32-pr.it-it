---
title: Contrassegno delle route per lo Hold-Down stato
description: Alcuni client, ad esempio i protocolli di vettore di distanza come RIP e DVMRP, richiedono che le destinazioni siano annunciate come non raggiungibili per un determinato periodo di tempo dopo l'eliminazione dell'ultima route verso la destinazione.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833f41da08c45d8f9bbe9419360f4d1857b2a52fb92ee0be341b56bc8362536e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790489"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Contrassegno delle route per lo Hold-Down stato

Alcuni client, ad esempio i protocolli di vettore di distanza come RIP e DVMRP, richiedono che le destinazioni siano annunciate come non raggiungibili per un determinato periodo di tempo dopo l'eliminazione dell'ultima route verso la destinazione. L'ultima route eliminata deve essere annunciata come non raggiungibile anche se nel frattempo arrivano route più nuove. L'ultima route eliminata è contrassegnata come in *stato di blocco.* Il processo di blocco impedisce la formazione di cicli di routing. I cicli di routing vengono causati quando un protocollo di routing annuncia informazioni di routing obsolete. Alla scadenza del blocco, questi protocolli riprendono l'annuncio con la nuova route migliore.

Un protocollo che implementa gli stati di blocco indica che una destinazione si trova in uno stato di blocco usando la [**funzione RtmHoldDestination.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) Il client chiama questa funzione quando annuncia la route migliore per questa destinazione. Se tutte le route a questa destinazione vengono eliminate in un secondo momento, l'ultima route eliminata viene mantenuta in uno stato di blocco per il periodo di tempo specificato nella chiamata precedente a **RtmHoldDestination**.

Quando un protocollo annuncia una destinazione, le informazioni sulla route usate dipendono dal fatto che il protocollo usi gli stati di blocco e se esiste una route nello stato di blocco per la destinazione.

I protocolli che non usano gli stati di blocco possono ignorare le informazioni sulla route correlate agli stati di blocco per una destinazione e annunciare sempre la route migliore.

Per il codice di esempio che illustra come usare queste funzioni, vedere [Usare la](use-the-route-hold-down-state.md)route Hold-Down stato .

 

 




