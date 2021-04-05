---
title: Callback di gestione gruppi multicast
description: Il gestore del gruppo multicast usa i callback seguenti per notificare ai client (in genere, protocolli di routing) gli eventi e le modifiche di stato
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872738"
---
# <a name="multicast-group-manager-callbacks"></a>Callback di gestione gruppi multicast

Il gestore del gruppo multicast utilizza i callback seguenti per notificare ai client (in genere, protocolli di routing) gli eventi e le modifiche di stato:

[**\_ \_ callback avviso di creazione PMGM \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**\_ \_ callback avviso PMGM \_ join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**\_ \_ callback avviso di eliminazione \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**\_callback di \_ join \_ locale di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**\_callback di \_ Leave \_ locale di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**\_callback RPF di PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ errato \_ se \_ callback**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

Il gestore del gruppo multicast utilizza i callback seguenti per notificare l'evento IGMP degli eventi e delle modifiche di stato:

[**PMGM \_ Disabilita \_ \_ callback IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ Abilita \_ \_ callback IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 