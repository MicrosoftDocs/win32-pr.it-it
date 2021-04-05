---
title: Callback di avviso di interfaccia errato
description: Dopo che il server d'avanzamento del kernel riceve i dati multicast da un'origine specifica sull'interfaccia non corretta, invia una notifica al gestore del gruppo multicast.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713912"
---
# <a name="wrong-interface-alert-callbacks"></a><span data-ttu-id="eb8c2-103">Callback di avviso di interfaccia errato</span><span class="sxs-lookup"><span data-stu-id="eb8c2-103">Wrong Interface Alert Callbacks</span></span>

<span data-ttu-id="eb8c2-104">Dopo che il server d'avanzamento del kernel riceve i dati multicast da un'origine specifica sull'interfaccia non corretta, invia una notifica al gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="eb8c2-104">After the kernel forwarder receives multicast data from a specific source on the wrong interface, it notifies the multicast group manager.</span></span> <span data-ttu-id="eb8c2-105">Il gestore del gruppo multicast richiama quindi il [**PMGM \_ errato \_ se \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback callback al protocollo di routing che possiede l'interfaccia su cui sono stati ricevuti i dati in modo errato.</span><span class="sxs-lookup"><span data-stu-id="eb8c2-105">The multicast group manager then invokes the [**PMGM\_WRONG\_IF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback to the routing protocol that owns the interface on which the data incorrectly arrived.</span></span>

> [!Note]  
> <span data-ttu-id="eb8c2-106">Questo callback non è attualmente implementato in questa versione dell'API MGM.</span><span class="sxs-lookup"><span data-stu-id="eb8c2-106">This callback is not currently implemented in this version of the MGM API.</span></span>

 

 

 




