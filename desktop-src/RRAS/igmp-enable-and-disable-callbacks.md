---
title: Abilitare e disabilitare i callback IGMP
description: Il gestore di gruppi multicast usa due callback a IGMP per coordinare le modifiche nella proprietà dell'interfaccia da IGMP a un protocollo di routing e da un protocollo di routing a IGMP.
ms.assetid: e4b2be85-6c67-4801-9905-eb1990d4bbb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103a0f9abb4d2a78b2b87fde3cb5832b4e88eb2677851d9fe703e5162263642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791144"
---
# <a name="igmp-enable-and-disable-callbacks"></a>Abilitare e disabilitare i callback IGMP

Il gestore di gruppi multicast usa due callback a IGMP per coordinare le modifiche nella proprietà dell'interfaccia da IGMP a un protocollo di routing e da un protocollo di routing a IGMP. I callback consentono a IGMP di coesistere su un'interfaccia con un altro protocollo di routing, ad esempio DVMRP.

Dopo che la proprietà di un'interfaccia è cambiata, il gestore di gruppi multicast richiama innanzitutto il callback [**\_ CALLBACK \_ IGMP \_ DISABLE DI PMGM.**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) IGMP deve interrompere l'aggiunta e l'eliminazione delle appartenenze ai gruppi nell'interfaccia specificata finché il gestore di gruppi multicast non richiama il callback [**CALLBACK \_ \_ IGMP \_ ENABLE PMGM.**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

Il gestore di gruppi multicast richiama il callback [**\_ CALLBACK \_ IGMP ENABLE IGMP \_ PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) al termine della modifica della proprietà dell'interfaccia.

 

 