---
title: Callback di avviso di join
description: Quando al gestore del gruppo multicast viene notificato che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il \_ callback di callback di avviso di PMGM join \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044930"
---
# <a name="join-alert-callbacks"></a>Callback di avviso di join

Quando al gestore del gruppo multicast viene notificato che sono presenti nuovi ricevitori per un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback di [**\_ callback di \_ avviso \_ di PMGM join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) . Questo callback notifica ai protocolli di routing che i nuovi host sono stati aggiunti ai gruppi specificati. Pertanto, i protocolli di routing devono richiedere dati multicast per i gruppi specificati dal callback.

Il gestore del gruppo multicast utilizza un set predefinito di regole utilizzate per determinare quando viene richiamato il callback. Questo set di regole è basato sul tipo di richiesta di join inviato dal client e sull'ordine con cui sono state ricevute le richieste di join.

## <a name="wildcard-join-requests"></a>Richieste di join con caratteri jolly

Quando viene ricevuto un join con caratteri jolly per un gruppo ( \* , g) dal primo client, il gestore del gruppo multicast richiama il callback di [**\_ callback di \_ avviso \_ di PMGM join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) a tutti gli altri client registrati. Quando viene ricevuto un join con caratteri jolly per un gruppo dal secondo client, il gestore del gruppo multicast richiama questo callback al primo client per l'aggiunta al gruppo.

## <a name="source-specific-join-requests"></a>Richieste di join Source-Specific

Il gestore del gruppo multicast non richiama questo callback per i successivi join al gruppo.

Quando viene ricevuto un join specifico dell'origine per un gruppo (s, g), il gestore del gruppo multicast richiama il callback di [**\_ callback dell' \_ avviso \_ di join PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) solo per il client proprietario dell'interfaccia in ingresso verso l'origine s.

 

 




