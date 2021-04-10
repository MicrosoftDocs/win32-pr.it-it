---
title: Procedure consigliate di WinRM
description: In questo argomento vengono illustrate alcune delle procedure consigliate per l'utilizzo delle varie funzionalità dell'API WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963135"
---
# <a name="winrm-best-practices"></a><span data-ttu-id="16c6b-103">Procedure consigliate di WinRM</span><span class="sxs-lookup"><span data-stu-id="16c6b-103">WinRM Best Practices</span></span>

<span data-ttu-id="16c6b-104">In questo argomento vengono illustrate alcune delle procedure consigliate per l'utilizzo delle varie funzionalità dell'API WinRM.</span><span class="sxs-lookup"><span data-stu-id="16c6b-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="16c6b-105">Quote</span><span class="sxs-lookup"><span data-stu-id="16c6b-105">Quotas</span></span>

<span data-ttu-id="16c6b-106">Quando viene raggiunta una quota, il servizio gestione remota Windows restituisce un errore al client.</span><span class="sxs-lookup"><span data-stu-id="16c6b-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="16c6b-107">Di conseguenza, la logica client deve ritentare in modo esplicito l'operazione in base all'errore restituito.</span><span class="sxs-lookup"><span data-stu-id="16c6b-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="16c6b-108">Sottoscrizioni di eventi</span><span class="sxs-lookup"><span data-stu-id="16c6b-108">Event subscriptions</span></span>

<span data-ttu-id="16c6b-109">Quando si utilizzano le sottoscrizioni avviate da agente di raccolta, limitare il numero di computer remoti a 500 e isolare il servizio [raccolta eventi Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) in un processo host separato.</span><span class="sxs-lookup"><span data-stu-id="16c6b-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="16c6b-110">Un errore di connessione conterrà un thread finché non si verifica il timeout. Un numero elevato di errori di connessione simultanei può causare l'esaurimento del pool di thread e il rendering del server che non risponde.</span><span class="sxs-lookup"><span data-stu-id="16c6b-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 