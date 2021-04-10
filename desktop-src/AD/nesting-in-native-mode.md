---
title: Annidamento in modalità nativa
description: Nell'elenco seguente viene descritto il possibile contenuto di un gruppo esistente in un dominio in modalità nativa.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Annidamento in modalità nativa di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855398"
---
# <a name="nesting-in-native-mode"></a><span data-ttu-id="c059a-104">Annidamento in modalità nativa</span><span class="sxs-lookup"><span data-stu-id="c059a-104">Nesting in Native Mode</span></span>

<span data-ttu-id="c059a-105">Nell'elenco seguente viene descritto il possibile contenuto di un gruppo esistente in un dominio in modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="c059a-105">The following list describes what can be contained in a group that exists in a native-mode domain.</span></span> <span data-ttu-id="c059a-106">Questo stesso elenco si applica anche ai gruppi di distribuzione nei domini in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="c059a-106">This same list also applies to distribution groups in mixed-mode domains.</span></span> <span data-ttu-id="c059a-107">L'ambito del gruppo determina queste regole di contenimento.</span><span class="sxs-lookup"><span data-stu-id="c059a-107">The scope of the group determines these containment rules.</span></span>

-   <span data-ttu-id="c059a-108">Un gruppo universale può contenere altri gruppi universali, gruppi e account globali di qualsiasi dominio all'interno della foresta in cui risiede questo gruppo universale.</span><span class="sxs-lookup"><span data-stu-id="c059a-108">A universal group can contain other universal groups, global groups and accounts from any domain within the forest in which this Universal Group resides.</span></span>
-   <span data-ttu-id="c059a-109">Un gruppo globale può contenere altri gruppi e account globali dello stesso dominio a cui appartiene il gruppo.</span><span class="sxs-lookup"><span data-stu-id="c059a-109">A global group can contain other global groups and accounts from the same domain that the group belongs to.</span></span> <span data-ttu-id="c059a-110">Un gruppo globale non può contenere gruppi universali o qualsiasi account o gruppo globale di un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="c059a-110">A global group cannot contain any universal groups, or any global group or account from another domain.</span></span>
-   <span data-ttu-id="c059a-111">Un gruppo locale di dominio può contenere gruppi universali, gruppi globali e account di qualsiasi dominio o foresta.</span><span class="sxs-lookup"><span data-stu-id="c059a-111">A domain local group can contain universal groups, global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="c059a-112">Un gruppo locale di dominio può inoltre contenere altri gruppi locali di dominio dello stesso dominio a cui appartiene il gruppo.</span><span class="sxs-lookup"><span data-stu-id="c059a-112">A domain local group can also contain other domain local groups from the same domain that the group belongs to.</span></span> <span data-ttu-id="c059a-113">Un gruppo locale di dominio non può contenere altri gruppi locali di dominio da qualsiasi altro dominio o insieme di strutture.</span><span class="sxs-lookup"><span data-stu-id="c059a-113">A domain local group cannot contain other domain local groups from any other domain or forest.</span></span>

 

 




