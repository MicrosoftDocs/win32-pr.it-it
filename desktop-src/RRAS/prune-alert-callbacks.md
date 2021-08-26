---
title: Eliminare i callback degli avvisi
description: Quando il gestore del gruppo multicast riceve una notifica che indica che i ricevitori lasciano un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback PMGM \_ PRUNE \_ ALERT \_ CALLBACK.
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5aa4d95742a2976ea46367b0f1af9442528c2821dc9d27b09b9e1c29eee6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036400"
---
# <a name="prune-alert-callbacks"></a>Eliminare i callback degli avvisi

Quando il gestore del gruppo multicast riceve una notifica che indica che i ricevitori lasciano un gruppo in un'interfaccia, il gestore del gruppo multicast richiama il callback [**PMGM \_ PRUNE \_ ALERT \_ CALLBACK.**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) Questo callback notifica ai protocolli di routing che i client non appartengono più al gruppo specificato. Pertanto, i protocolli di routing devono interrompere la richiesta di dati multicast per i gruppi specificati.

Il gestore di gruppi multicast dispone di un set predefinito di regole utilizzate per determinare quando viene richiamato questo callback. Queste regole si basano sia sul tipo di richiesta di eliminazione inviata dal client che sull'ordine in cui sono state ricevute le richieste di eliminazione.

## <a name="wildcard-prune-requests"></a>Richieste di eliminazione con caratteri jolly

Quando viene ricevuto un carattere jolly per un gruppo ( , g) e l'interfaccia finale viene rimossa per il secondo o l'ultimo client (ovvero quando rimangono le interfacce per un solo client), il gestore del gruppo multicast richiama il callback DI CALLBACK DI AVVISO \* [**\_ PRUNE \_ \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) per il client rimanente. Dopo che l'interfaccia finale è stata rimossa per l'ultimo client ,ovvero quando non rimangono altre interfacce, questo callback viene richiamato per tutti gli altri client registrati con il gestore di gruppi multicast.

## <a name="source-specific-prune-requests"></a>Source-Specific le richieste di eliminazione

Quando viene ricevuta un'eliminazione specifica dell'origine per un gruppo (s, g), il gestore del gruppo multicast richiama il callback DI CALLBACK DELL'AVVISO [**PMGM \_ PRUNE \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) solo per il client proprietario dell'interfaccia in ingresso verso le origini.

 

 




