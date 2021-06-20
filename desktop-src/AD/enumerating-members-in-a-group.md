---
title: Enumerazione dei membri in un gruppo
description: Informazioni sull'enumerazione dei membri in un Azure Active Directory gruppo. I membri di un gruppo vengono archiviati in un attributo multivalore denominato member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerazione dei membri in un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407424"
---
# <a name="enumerating-members-in-a-group"></a><span data-ttu-id="443e4-105">Enumerazione dei membri in un gruppo</span><span class="sxs-lookup"><span data-stu-id="443e4-105">Enumerating Members in a Group</span></span>

<span data-ttu-id="443e4-106">I membri di un gruppo vengono archiviati in un attributo multivalore denominato **membro**.</span><span class="sxs-lookup"><span data-stu-id="443e4-106">The members of a group are stored in a multi-value attribute called **member**.</span></span> <span data-ttu-id="443e4-107">Per i gruppi con appartenenza da piccola a media, usare il metodo [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) per ottenere un puntatore a un oggetto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) che contiene l'elenco di tutti i membri.</span><span class="sxs-lookup"><span data-stu-id="443e4-107">For groups with a small to medium-sized membership, use the [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) method to get a pointer to an [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) object that contains the list of all members.</span></span> <span data-ttu-id="443e4-108">Usare quindi [**IADsMembers::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) per ottenere un oggetto enumeratore che è possibile usare per enumerare i membri.</span><span class="sxs-lookup"><span data-stu-id="443e4-108">Then use the [**IADsMembers::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) to get an enumerator object that you can use to enumerate the members.</span></span>

<span data-ttu-id="443e4-109">Se l'appartenenza al gruppo prevista sarà di 1000 o più membri, usare ranging per recuperare gli utenti un intervallo alla volta.</span><span class="sxs-lookup"><span data-stu-id="443e4-109">If the anticipated group membership will be 1000 or more members, use ranging to retrieve users one range at a time.</span></span> <span data-ttu-id="443e4-110">Per altre informazioni sull'uso di ranging per enumerare i membri, vedere [Enumerazione di gruppi che contengono molti membri.](enumerating-groups-that-contain-many-members.md)</span><span class="sxs-lookup"><span data-stu-id="443e4-110">For more information about using ranging to enumerate members, see [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).</span></span>

 

 