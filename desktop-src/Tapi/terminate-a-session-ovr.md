---
description: La chiusura della sessione può avere origine con una richiesta utente, disconnessione remota da parte dell'altra parte o per motivi specifici dell'applicazione.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Terminare una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319851"
---
# <a name="terminate-a-session"></a><span data-ttu-id="c2a48-103">Terminare una sessione</span><span class="sxs-lookup"><span data-stu-id="c2a48-103">Terminate a Session</span></span>

<span data-ttu-id="c2a48-104">La chiusura della sessione può avere origine con una richiesta utente, disconnessione remota da parte dell'altra parte o per motivi specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2a48-104">Session termination may originate with a user request, remote disconnection by the other party, or for application-specific reasons.</span></span> <span data-ttu-id="c2a48-105">Quando una sessione viene terminata, l' [identificatore di sessione](session-identifier-ovr.md) rimane valido fino a quando non viene rilasciato in modo specifico e può essere usato per raccogliere i dati di post-connessione.</span><span class="sxs-lookup"><span data-stu-id="c2a48-105">When a session is terminated, the [session identifier](session-identifier-ovr.md) remains valid until specifically released and can be used to gather post-connection data.</span></span>

<span data-ttu-id="c2a48-106">La chiusura della sessione viene completata deallocando e rilasciando le risorse associate alla sessione.</span><span class="sxs-lookup"><span data-stu-id="c2a48-106">Session termination is completed by deallocating and releasing the resources associated with the session.</span></span> <span data-ttu-id="c2a48-107">Se una sessione viene semplicemente eliminata o disconnessa, ma le risorse non vengono rilasciate, il risultato è una perdita di memoria nell'applicazione ed eventualmente anche nel provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="c2a48-107">If a session is merely dropped or disconnected but resources are not released, the result is a memory leak in the application and possibly in the service provider as well.</span></span>

<span data-ttu-id="c2a48-108">**TAPI 2. x:** Vedere [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span><span class="sxs-lookup"><span data-stu-id="c2a48-108">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span></span>

<span data-ttu-id="c2a48-109">**TAPI 3. x:** Vedere [**ITBasicCallControl::D Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), eseguire una versione com standard sul puntatore all'oggetto call.</span><span class="sxs-lookup"><span data-stu-id="c2a48-109">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), perform a standard COM release on the Call object pointer.</span></span>

 

 
