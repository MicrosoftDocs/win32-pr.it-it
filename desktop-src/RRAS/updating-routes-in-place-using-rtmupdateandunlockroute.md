---
title: Aggiornamento delle route sul posto mediante RtmUpdateAndUnlockRoute
description: L'aggiornamento sul posto è in genere più efficiente rispetto all'aggiornamento della tabella di routing con un metodo indiretto, ad esempio quello usato dalla funzione RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044873"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Aggiornamento delle route sul posto mediante RtmUpdateAndUnlockRoute

L'aggiornamento sul posto è in genere più efficiente rispetto all'aggiornamento della tabella di routing con un metodo indiretto, ad esempio quello usato dalla funzione [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) . Questo metodo è più efficiente perché il client non è necessario per ottenere un handle, né per passare la struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) da e verso gestione tabelle di routing. Questo metodo richiede anche meno tempo. Tuttavia, l'aggiornamento diretto della tabella di routing può essere rischioso, perché il servizio di gestione delle tabelle di routing non funziona come intermediario.

Per il codice di esempio che illustra come usare queste funzioni, vedere [aggiornare una route sul posto usando RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).

 

 




