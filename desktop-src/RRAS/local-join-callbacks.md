---
title: Callback di join locale
description: Dopo che il gestore del gruppo multicast riceve una notifica da IGMP che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback DI JOIN LOCALE PMGM al protocollo di routing proprietario dell'interfaccia, se \_ \_ \_ presente.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b3464aa645a6ab110acef09f238ffca97f781a38cc6c2602a39e7c66316490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074071"
---
# <a name="local-join-callbacks"></a>Callback di join locale

Dopo che il gestore del gruppo multicast riceve una notifica da IGMP che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback DI JOIN [**\_ LOCALE \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) al protocollo di routing proprietario dell'interfaccia, se presente. Questo callback notifica al protocollo di routing la modifica.

Questo callback e il callback [**PMGM \_ LOCAL LEAVE \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) vengono usati per sincronizzare l'inoltro tra IGMP e i protocolli di routing.

 

 




