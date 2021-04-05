---
description: A partire da Windows 8, Microsoft ha iniziato a distribuire i provider che consentono di condividere in modo sicuro i segreti e i messaggi crittografati tra i computer.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Provider di protezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967186"
---
# <a name="protection-providers"></a><span data-ttu-id="c430e-103">Provider di protezione</span><span class="sxs-lookup"><span data-stu-id="c430e-103">Protection Providers</span></span>

<span data-ttu-id="c430e-104">A partire da Windows 8, Microsoft ha iniziato a distribuire i provider che consentono di condividere in modo sicuro i segreti e i messaggi crittografati tra i computer.</span><span class="sxs-lookup"><span data-stu-id="c430e-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="c430e-105">Attualmente sono disponibili due provider di protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="c430e-105">There are currently two key protection providers.</span></span> <span data-ttu-id="c430e-106">Il provider Microsoft Key Protection consente di proteggere il contenuto di un gruppo in una foresta Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c430e-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="c430e-107">Il provider Microsoft client Key Protection consente di proteggere il contenuto di un set di credenziali Web.</span><span class="sxs-lookup"><span data-stu-id="c430e-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="c430e-108">La protezione corretta da usare viene scelta automaticamente quando la funzione [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analizza la stringa della regola del descrittore di protezione fornita come input.</span><span class="sxs-lookup"><span data-stu-id="c430e-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="c430e-109">Il provider Microsoft Key Protection viene scelto per le stringhe di regole che iniziano con SID, SDDL e LOCAL.</span><span class="sxs-lookup"><span data-stu-id="c430e-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="c430e-110">Il provider Microsoft client Key Protection analizza le stringhe delle regole che iniziano con webcredentials.</span><span class="sxs-lookup"><span data-stu-id="c430e-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="c430e-111">Per ulteriori informazioni sulle stringhe delle regole, vedere [descrittori di protezione](protection-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="c430e-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="c430e-112">I provider personalizzati non sono attualmente consentiti. [DPAPI CNG](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="c430e-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c430e-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c430e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c430e-114">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="c430e-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="c430e-115">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c430e-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="c430e-116">Descrittori di protezione</span><span class="sxs-lookup"><span data-stu-id="c430e-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



