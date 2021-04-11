---
title: Richiamate avviso di eliminazione
description: Quando viene notificato al gestore del gruppo multicast che i ricevitori lasciano un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il \_ callback di callback dell'avviso di eliminazione PMGM \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045248"
---
# <a name="prune-alert-callbacks"></a>Richiamate avviso di eliminazione

Quando viene notificato al gestore del gruppo multicast che i ricevitori lasciano un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback di [**\_ callback dell' \_ avviso \_ di eliminazione PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) . Questo callback notifica ai protocolli di routing che i client non appartengono più al gruppo specificato. Pertanto, i protocolli di routing devono interrompere la richiesta di dati multicast per i gruppi specificati.

Il gestore del gruppo multicast dispone di un set predefinito di regole utilizzate per determinare quando questo callback viene richiamato. Queste regole sono basate sul tipo di richiesta di eliminazione inviata dal client e sull'ordine in cui sono state ricevute le richieste di eliminazione.

## <a name="wildcard-prune-requests"></a>Richieste di eliminazione con caratteri jolly

Quando viene ricevuta una potatura con caratteri jolly per un gruppo ( \* , g) e l'interfaccia finale viene rimossa per il client penultimo (ovvero, quando le interfacce per un solo client rimangono), il gestore del gruppo multicast richiama il callback di [**\_ \_ \_ callback dell'avviso di eliminazione PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) al client rimanente. Una volta rimossa l'interfaccia finale per l'ultimo client (ovvero, quando non restano altre interfacce), questo callback viene richiamato per tutti gli altri client registrati con il gestore del gruppo multicast.

## <a name="source-specific-prune-requests"></a>Richieste di eliminazione Source-Specific

Quando viene ricevuta una potatura specifica dell'origine per un gruppo (s, g), il gestore del gruppo multicast richiama il callback di [**\_ callback dell' \_ avviso \_ di eliminazione PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) solo per il client proprietario dell'interfaccia in ingresso verso l'origine.

 

 




