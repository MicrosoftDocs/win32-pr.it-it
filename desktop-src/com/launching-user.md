---
title: Avvio dell'utente
description: Avvio dell'utente
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872994"
---
# <a name="launching-user"></a><span data-ttu-id="011b9-103">Avvio dell'utente</span><span class="sxs-lookup"><span data-stu-id="011b9-103">Launching User</span></span>

<span data-ttu-id="011b9-104">Si tratta dell'impostazione predefinita per l'identità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="011b9-104">This is the default setting for the application identity.</span></span> <span data-ttu-id="011b9-105">Quando si sceglie l'utente di avvio per l'identità dell'applicazione, ogni account client ottiene una nuova istanza del server e ogni server ottiene la propria [finestra di Windows](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="011b9-105">When the launching user is chosen for the application's identity, each client account gets a new instance of the server and each server gets its own [window station](/windows/desktop/winstation/window-stations).</span></span> <span data-ttu-id="011b9-106">A causa delle istanze del server separate, l'avvio dell'utente è l'impostazione di identità di protezione di livello più alto.</span><span class="sxs-lookup"><span data-stu-id="011b9-106">Because of the separate server instances, launching user is the highest-level security protection identity setting.</span></span> <span data-ttu-id="011b9-107">Tuttavia, esistono limiti limitati al consumo di risorse.</span><span class="sxs-lookup"><span data-stu-id="011b9-107">However, there are finite limits on resource consumption.</span></span> <span data-ttu-id="011b9-108">Inoltre, tutte le GUI visualizzate dal server non saranno visualizzate dal client.</span><span class="sxs-lookup"><span data-stu-id="011b9-108">Also, any GUI the server displays will not be seen by the client.</span></span>

<span data-ttu-id="011b9-109">Se l'applicazione ha l'identità dell'utente che ha eseguito l'avvio, viene eseguita con un token di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="011b9-109">If the application has the identity of the launching user, it runs with an impersonation token.</span></span> <span data-ttu-id="011b9-110">Per ulteriori informazioni sui token di accesso e di rappresentazione, vedere [livelli di rappresentazione](impersonation-levels.md) e [mascheramento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="011b9-110">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="011b9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="011b9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="011b9-112">Identità applicazione</span><span class="sxs-lookup"><span data-stu-id="011b9-112">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="011b9-113">Utente interattivo</span><span class="sxs-lookup"><span data-stu-id="011b9-113">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="011b9-114">Identità del servizio</span><span class="sxs-lookup"><span data-stu-id="011b9-114">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="011b9-115">Utente specificato</span><span class="sxs-lookup"><span data-stu-id="011b9-115">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 