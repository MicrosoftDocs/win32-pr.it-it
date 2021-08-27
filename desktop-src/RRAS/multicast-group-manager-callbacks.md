---
title: Callback di Gestione gruppi multicast
description: Il gestore di gruppi multicast usa i callback seguenti per notificare ai client (in genere protocolli di routing) eventi e modifiche dello stato
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037281a2cb636b337c5133c2c3a261e2c435a136a30d0ccfdcf0407a9b62509b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036651"
---
# <a name="multicast-group-manager-callbacks"></a>Callback di Gestione gruppi multicast

Il gestore di gruppi multicast usa i callback seguenti per notificare ai client (in genere, protocolli di routing) eventi e modifiche dello stato:

[**CALLBACK DI AVVISO \_ DI \_ CREAZIONE PMGM \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**CALLBACK DI AVVISO \_ DI \_ JOIN PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**CALLBACK DI \_ AVVISO PMGM PRUNE \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**CALLBACK DI JOIN LOCALE PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**CALLBACK DI LASCIARE LOCALE PMGM \_ \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**PMGM \_ RPF \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ WRONG \_ IF \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

Il gestore del gruppo multicast usa i callback seguenti per notificare a IGMP gli eventi e le modifiche di stato:

[**PMGM \_ DISABLE \_ IGMP \_ CALLBACK**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ ENABLE \_ IGMP \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 