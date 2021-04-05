---
title: Le chiamate remote al protocollo RPC SAM sono limitate solo agli amministratori locali
description: Il protocollo RPC SAM viene limitato. Ciò significa che solo i membri del gruppo Administrators locale possono effettuare chiamate remote ai metodi in questo protocollo. Active Directory comportamento del controller di dominio non è interessato.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116933"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="3f048-105">Le chiamate remote al protocollo RPC SAM sono limitate solo agli amministratori locali</span><span class="sxs-lookup"><span data-stu-id="3f048-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="3f048-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3f048-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3f048-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3f048-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3f048-108">Il protocollo RPC SAM viene limitato.</span><span class="sxs-lookup"><span data-stu-id="3f048-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="3f048-109">Ciò significa che solo i membri del gruppo Administrators locale possono effettuare chiamate remote ai metodi in questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="3f048-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="3f048-110">Active Directory comportamento del controller di dominio non è interessato.</span><span class="sxs-lookup"><span data-stu-id="3f048-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="3f048-111">Soluzioni di prevenzione</span><span class="sxs-lookup"><span data-stu-id="3f048-111">Mitigations</span></span>

<span data-ttu-id="3f048-112">Assicurarsi che gli utenti corretti siano impostati come amministratori nel computer.</span><span class="sxs-lookup"><span data-stu-id="3f048-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="3f048-113">L'ACL usato per il controllo di accesso è configurabile tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="3f048-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 




