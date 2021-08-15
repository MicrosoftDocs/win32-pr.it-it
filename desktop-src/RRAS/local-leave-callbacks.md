---
title: Callback di lasciare locale
description: Dopo che il gestore del gruppo multicast viene informato da IGMP che non sono presenti altri ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback DI CALLBACK LOCAL LEAVE PMGM al protocollo di routing su tale interfaccia, se \_ \_ \_ presente. Questo callback notifica al protocollo di routing la modifica.
ms.assetid: 47696533-603c-459f-9aa7-3ce42fff3332
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4cd346ac3d84a5c763c7f8f866e21a1bffa2af533e5710c86ec8826ad7db45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790641"
---
# <a name="local-leave-callbacks"></a>Callback di lasciare locale

Dopo che il gestore del gruppo multicast viene informato da IGMP che non sono presenti altri ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback DI CALLBACK [**\_ LOCAL \_ LEAVE \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) al protocollo di routing su tale interfaccia, se presente. Questo callback notifica al protocollo di routing la modifica.

Questo callback e il callback [**PMGM \_ LOCAL JOIN \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) vengono usati per sincronizzare l'inoltro tra IGMP e i protocolli di routing.

 

 




