---
title: Contrassegno delle route per lo stato Hold-Down
description: Alcuni client, ad esempio i protocolli per vettori di distanza come RIP e DVMRP, richiedono che le destinazioni siano annunciate come irraggiungibili per un determinato periodo di tempo dopo l'eliminazione dell'ultima route alla destinazione.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955563"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Contrassegno delle route per lo stato Hold-Down

Alcuni client, ad esempio i protocolli per vettori di distanza come RIP e DVMRP, richiedono che le destinazioni siano annunciate come irraggiungibili per un determinato periodo di tempo dopo l'eliminazione dell'ultima route alla destinazione. L'ultima route eliminata deve essere annunciata come irraggiungibile anche se le route più recenti arrivano nel frattempo. L'ultima route eliminata è contrassegnata come in uno *stato di attesa*. Il processo di attesa impedisce la formazione dei cicli di routing. I cicli di routing vengono causati quando un protocollo di routing annuncia informazioni di routing obsolete. Quando il periodo di attesa scade, questi protocolli riprendono l'annuncio con la nuova route migliore.

Un protocollo che implementa gli Stati di attesa indica che una destinazione si trova in uno stato di attesa tramite la funzione [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) . Il client chiama questa funzione quando annuncia la route migliore a questa destinazione. Se in seguito vengono eliminate tutte le route a questa destinazione, l'ultima route eliminata viene mantenuta in uno stato di attesa per il periodo di tempo specificato nella chiamata precedente a **RtmHoldDestination**.

Quando un protocollo annuncia una destinazione, le informazioni sulla route utilizzate variano a seconda che il protocollo usi gli Stati di attesa e se è presente una route nello stato di attesa per la destinazione.

I protocolli che non utilizzano gli Stati di attesa possono ignorare le informazioni relative alla route correlate agli Stati di attesa per una destinazione e annunciare sempre la migliore route.

Per il codice di esempio che illustra come usare queste funzioni, vedere [usare lo stato Hold-Down Route](use-the-route-hold-down-state.md).

 

 




