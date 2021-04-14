---
title: Località temporale
description: La località temporale è una strategia di prevenzione che riduce la finestra per gli aggiornamenti parziali.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470835"
---
# <a name="temporal-locality"></a>Località temporale

La *località temporale* è una strategia di prevenzione che riduce la finestra per gli aggiornamenti parziali. La replica delle modifiche da una replica di origine specificata continua in ordine crescente di USN. Le Scritture che si verificano in un periodo di tempo ravvicinato avranno USNs che si avvicinano tra loro e verranno propagate insieme nel tempo. Le applicazioni che creano o aggiornano più oggetti correlati devono scrivere gli oggetti più vicini nel tempo possibile. Ad esempio, l'applicazione può raccogliere tutti gli input necessari dall'utente e applicarli alla directory quando l'utente fa clic su un pulsante "applica".

La località temporale riduce anche le probabilità di risoluzione dei conflitti introducendo incoerenze intra-Object.

 

 




