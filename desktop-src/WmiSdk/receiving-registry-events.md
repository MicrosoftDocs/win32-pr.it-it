---
description: Il provider del registro di sistema tenta di inviare una notifica per ogni evento che si verifica.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Ricezione degli eventi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049761"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="e9180-103">Ricezione degli eventi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e9180-103">Receiving Registry Events</span></span>

<span data-ttu-id="e9180-104">Il provider del registro di sistema tenta di inviare una notifica per ogni evento che si verifica.</span><span class="sxs-lookup"><span data-stu-id="e9180-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="e9180-105">Tuttavia, il provider del registro di sistema non garantisce che il consumer riceverà uno o tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="e9180-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="e9180-106">L'eccezione è che il provider del registro di sistema garantisce che un consumer riceva una notifica per ogni registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="e9180-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="e9180-107">Si supponga, ad esempio, che un consumer registri per due eventi di modifica della struttura ad albero, richiedendo notifiche per le istanze [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) .</span><span class="sxs-lookup"><span data-stu-id="e9180-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="e9180-108">Ogni registrazione ha lo stesso valore hive (sottoalbero), ma un valore RootPath diverso.</span><span class="sxs-lookup"><span data-stu-id="e9180-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="e9180-109">Se le chiavi di entrambi i percorsi cambiano più volte, il provider del registro di sistema garantisce che il consumer riceva una notifica per ogni percorso.</span><span class="sxs-lookup"><span data-stu-id="e9180-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="e9180-110">A seconda del tempo di risposta del registro di sistema e del provider del registro di sistema, il consumer può ricevere il numero di notifiche che si sono verificate in presenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="e9180-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9180-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9180-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9180-112">Registrazione per eventi registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e9180-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
