---
title: Modifica dell'ambito o del tipo di un gruppo
description: In questo argomento viene illustrato come modificare l'ambito o il tipo di un gruppo in domini in modalità nativa.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- gruppi di Active Directory, modifica dell'ambito o del tipo di un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707207"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="ff23b-104">Modifica dell'ambito o del tipo di un gruppo</span><span class="sxs-lookup"><span data-stu-id="ff23b-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="ff23b-105">La modifica di un ambito o di un tipo di gruppo non è consentita nei domini in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="ff23b-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="ff23b-106">Tuttavia, le conversioni seguenti sono consentite nei domini in modalità nativa:</span><span class="sxs-lookup"><span data-stu-id="ff23b-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="ff23b-107">Gruppo globale-gruppo universale: questa operazione è consentita solo se il gruppo globale non è un membro di un altro gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="ff23b-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="ff23b-108">Gruppo locale di dominio in gruppo universale: il gruppo locale di dominio da convertire non può contenere un altro gruppo locale di dominio.</span><span class="sxs-lookup"><span data-stu-id="ff23b-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="ff23b-109">Dal gruppo universale al gruppo locale di dominio o globale: per la conversione in un gruppo globale, il gruppo universale convertito non può contenere utenti o gruppi globali di un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="ff23b-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="ff23b-110">Per la conversione in un gruppo locale di dominio, il gruppo universale convertito non può essere membro di un gruppo universale o di un gruppo locale di dominio di un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="ff23b-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="ff23b-111">In modalità nativa, un tipo di gruppo può essere convertito liberamente tra i gruppi di sicurezza e i gruppi di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ff23b-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="ff23b-112">Tenere presente che se un gruppo viene usato per impostare il controllo di accesso, la modifica dell'ambito o del tipo può influire sulle voci di controllo di accesso (ACE) che contengono tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="ff23b-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="ff23b-113">Il sistema di sicurezza ignorerà le voci ACE contenenti gruppi che non sono gruppi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ff23b-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




