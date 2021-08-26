---
title: Callback di avviso di interfaccia non corretto
description: Dopo che il server d'inoltro del kernel riceve i dati multicast da un'origine specifica sull'interfaccia errata, invia una notifica al gestore del gruppo multicast.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3354b1355cbcb1654b41a61ab046e74ec41b8dc716de6d50f7d9d52b18d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024651"
---
# <a name="wrong-interface-alert-callbacks"></a>Callback di avviso di interfaccia non corretto

Dopo che il server d'inoltro del kernel riceve i dati multicast da un'origine specifica sull'interfaccia errata, invia una notifica al gestore del gruppo multicast. Il gestore del gruppo multicast richiama quindi il callback [**PMGM \_ WRONG IF \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) al protocollo di routing proprietario dell'interfaccia sulla quale sono arrivati erroneamente i dati.

> [!Note]  
> Questo callback non è attualmente implementato in questa versione dell'API MGM.

 

 

 




