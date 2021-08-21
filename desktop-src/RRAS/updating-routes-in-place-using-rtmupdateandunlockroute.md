---
title: Aggiornamento delle route sul posto tramite RtmUpdateAndUnlockRoute
description: L'aggiornamento sul posto è in genere più efficiente rispetto all'aggiornamento della tabella di routing con un metodo indiretto, ad esempio quello usato dalla funzione RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfcfdc7abd355cd70bb1295af6ce8b4fb4749dfed6c55af4d1fd06ca8257170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073701"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Aggiornamento delle route sul posto tramite RtmUpdateAndUnlockRoute

L'aggiornamento sul posto è in genere più efficiente rispetto all'aggiornamento della tabella di routing con un metodo indiretto, ad esempio quello usato dalla funzione [**RtmAddRouteToDest.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) Questo metodo è più efficiente perché il client non è necessario per ottenere un handle né per passare la struttura [**\_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) a e dal gestore tabelle di routing. Questo metodo richiede anche meno tempo. Tuttavia, l'aggiornamento diretto della tabella di routing può essere rischioso, poiché il gestore tabelle di routing non funziona come intermediario.

Per il codice di esempio che illustra come usare queste funzioni, vedere Aggiornare una route sul posto [usando RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).

 

 




