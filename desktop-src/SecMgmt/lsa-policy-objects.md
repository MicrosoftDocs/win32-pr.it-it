---
description: LSA archivia le informazioni sui criteri di sicurezza locali in un set di oggetti. L'applicazione può eseguire query o modificare i criteri di sicurezza locali accedendo a questi oggetti.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Oggetti criteri LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967613"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="7b919-104">Oggetti criteri LSA</span><span class="sxs-lookup"><span data-stu-id="7b919-104">LSA Policy Objects</span></span>

<span data-ttu-id="7b919-105">LSA archivia le informazioni sui criteri di sicurezza locali in un set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7b919-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="7b919-106">L'applicazione può eseguire query o modificare i criteri di sicurezza locali accedendo a questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="7b919-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="7b919-107">Il set è costituito dai quattro oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7b919-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="7b919-108">Il [criterio](policy-object.md) contiene informazioni sui criteri globali.</span><span class="sxs-lookup"><span data-stu-id="7b919-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="7b919-109">[TrustedDomain](trusteddomain-object.md) contiene informazioni su un dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="7b919-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="7b919-110">L' [account](account-object.md) contiene informazioni su un account utente, gruppo o gruppo locale.</span><span class="sxs-lookup"><span data-stu-id="7b919-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="7b919-111">[I dati privati](private-data-object.md) contengono informazioni protette, ad esempio le password degli account server.</span><span class="sxs-lookup"><span data-stu-id="7b919-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="7b919-112">Queste informazioni vengono archiviate come stringhe crittografate.</span><span class="sxs-lookup"><span data-stu-id="7b919-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="7b919-113">Per ulteriori informazioni sull'utilizzo delle funzioni dei criteri LSA per gestire le informazioni archiviate in questi oggetti, vedere [utilizzo dei criteri LSA](using-lsa-policy.md).</span><span class="sxs-lookup"><span data-stu-id="7b919-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



