---
title: Esecuzione di query per i gruppi in un dominio
description: I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Esecuzione di query per i gruppi in un dominio Active Directory
- Gruppi di Active Directory, esecuzione di query per i gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872265"
---
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="66e60-105">Esecuzione di query per i gruppi in un dominio</span><span class="sxs-lookup"><span data-stu-id="66e60-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="66e60-106">I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio.</span><span class="sxs-lookup"><span data-stu-id="66e60-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="66e60-107">È possibile che i gruppi non siano sempre presenti in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="66e60-107">Groups may not always be in one container.</span></span> <span data-ttu-id="66e60-108">Pertanto, è necessario eseguire la ricerca nell'intero dominio per trovare tutti i gruppi nel dominio.</span><span class="sxs-lookup"><span data-stu-id="66e60-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="66e60-109">Per cercare tutti i gruppi in un dominio, impostare il punto di inizio della ricerca sulla radice del dominio, impostare l'ambito di ricerca su sottoalbero e cercare tutti gli oggetti che hanno un valore [**objectClass**](/windows/desktop/ADSchema/a-objectclass) di "Group".</span><span class="sxs-lookup"><span data-stu-id="66e60-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="66e60-110">Se è necessario trovare i gruppi che contengono determinati valori di [**\_ \_ \_ enumerazione di tipo gruppo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) , è possibile usare il **bit della regola di corrispondenza LDAP \_ \_ \_ \_ e** l'operatore della regola di corrispondenza per cercare i gruppi con determinati bit impostati nell'attributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="66e60-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="66e60-111">Per ulteriori informazioni sull'utilizzo delle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="66e60-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="66e60-112">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire la ricerca di gruppi in un dominio, vedere il [codice di esempio per la ricerca di gruppi in un dominio](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="66e60-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 