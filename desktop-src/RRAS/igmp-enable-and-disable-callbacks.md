---
title: Abilitazione e disabilitazione di callback IGMP
description: Il gestore del gruppo multicast utilizza due callback a IGMP per coordinare le modifiche alla proprietà dell'interfaccia da IGMP a un protocollo di routing e da un protocollo di routing a IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa58e9b65c67ac5946f5f5e54e611565e59d8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872821"
---
# <a name="igmp-enable-and-disable-callbacks"></a>Abilitazione e disabilitazione di callback IGMP

Il gestore del gruppo multicast utilizza due callback a IGMP per coordinare le modifiche alla proprietà dell'interfaccia da IGMP a un protocollo di routing e da un protocollo di routing a IGMP. I callback consentono a IGMP di coesistere su un'interfaccia con un altro protocollo di routing, ad esempio DVMRP.

Dopo che la proprietà di un'interfaccia è stata modificata, il gestore del gruppo multicast richiama per prima cosa il callback di [**\_ \_ \_ callback IGMP PMGM Disable**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . IGMP deve interrompere l'aggiunta e l'eliminazione delle appartenenze ai gruppi nell'interfaccia specificata fino a quando il gestore del gruppo multicast richiama il callback di [**\_ \_ \_ callback IGMP di PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) .

Il gestore del gruppo multicast richiama il callback [**PMGM \_ enable \_ IGMP \_ callback**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) dopo il completamento della modifica della proprietà dell'interfaccia.

 

 