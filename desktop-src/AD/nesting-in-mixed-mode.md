---
title: Annidamento in modalità mista
description: Questo argomento elenca le restrizioni dei gruppi di sicurezza in un dominio in modalità mista.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Annidamento in modalità mista AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855401"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="4791e-104">Annidamento in modalità mista</span><span class="sxs-lookup"><span data-stu-id="4791e-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="4791e-105">Questo argomento elenca le restrizioni dei gruppi di sicurezza in un dominio in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="4791e-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="4791e-106">I gruppi di sicurezza in un dominio in modalità mista presentano le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4791e-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="4791e-107">Non è possibile creare gruppi universali in domini in modalità mista perché l'ambito universale è supportato solo nei domini in modalità nativa di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4791e-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="4791e-108">Un gruppo globale può contenere account dello stesso dominio a cui appartiene il gruppo.</span><span class="sxs-lookup"><span data-stu-id="4791e-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="4791e-109">Un gruppo globale non può contenere gruppi universali, gruppi globali o un account di un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="4791e-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="4791e-110">Un gruppo locale di dominio può contenere gruppi e account globali di qualsiasi dominio o foresta.</span><span class="sxs-lookup"><span data-stu-id="4791e-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="4791e-111">Un gruppo locale di dominio non può contenere altri gruppi locali di dominio.</span><span class="sxs-lookup"><span data-stu-id="4791e-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="4791e-112">Tenere presente che i gruppi di distribuzione possono essere annidati in base alle regole di annidamento per la modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="4791e-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




