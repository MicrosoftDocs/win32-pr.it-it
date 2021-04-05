---
title: Enumerazione dei membri in un gruppo
description: I membri di un gruppo vengono archiviati in un attributo multivalore denominato member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerazione dei membri in un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117562"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="e9522-104">Enumerazione dei membri in un gruppo</span><span class="sxs-lookup"><span data-stu-id="e9522-104">Enumerating Members in a Group</span></span>

<span data-ttu-id="e9522-105">I membri di un gruppo vengono archiviati in un attributo multivalore denominato **member**.</span><span class="sxs-lookup"><span data-stu-id="e9522-105">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="e9522-106">Per i gruppi con appartenenza di dimensioni medio-piccole, usare il metodo [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) per ottenere un puntatore a un oggetto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) che contiene l'elenco di tutti i membri.</span><span class="sxs-lookup"><span data-stu-id="e9522-106">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="e9522-107">Usare quindi [**IADsMembers:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) per ottenere un oggetto enumeratore che può essere usato per enumerare i membri.</span><span class="sxs-lookup"><span data-stu-id="e9522-107">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="e9522-108">Se l'appartenenza al gruppo prevista sarà di 1000 o più membri, utilizzare la funzione che consente di recuperare gli utenti un intervallo alla volta.</span><span class="sxs-lookup"><span data-stu-id="e9522-108">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="e9522-109">Per ulteriori informazioni sull'utilizzo di ranging per enumerare i membri, vedere [enumerazione dei gruppi che contengono molti membri](enumerating-groups-that-contain-many-members.md).</span><span class="sxs-lookup"><span data-stu-id="e9522-109">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 