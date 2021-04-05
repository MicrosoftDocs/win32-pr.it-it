---
title: Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo
description: Il metodo IADsGroup. IsValid può essere utilizzato per determinare se un oggetto è un membro di un gruppo.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo AD
- gruppi di Active Directory, determinazione dell'appartenenza di un utente o di un gruppo a un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046523"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a><span data-ttu-id="b4c14-105">Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo</span><span class="sxs-lookup"><span data-stu-id="b4c14-105">Determining a User's or Group's Membership in a Group</span></span>

<span data-ttu-id="b4c14-106">Il metodo [**IADsGroup.**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) IsValid può essere utilizzato per determinare se un oggetto è un membro di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="b4c14-106">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method can be used to determine if an object is a member of a group.</span></span> <span data-ttu-id="b4c14-107">Questo metodo restituisce **true** se l'oggetto specificato è un membro diretto del gruppo, ovvero la proprietà del membro del gruppo contiene l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="b4c14-107">This method returns **TRUE** if the specified object is a direct member of the group, that is, the group's member property contains the specified object.</span></span>

<span data-ttu-id="b4c14-108">Un gruppo può contenere altri gruppi.</span><span class="sxs-lookup"><span data-stu-id="b4c14-108">A group can contain other groups.</span></span> <span data-ttu-id="b4c14-109">Il metodo [**IADsGroup.**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) IsValid non verifica in modo ricorsivo i membri dei gruppi nella proprietà del membro, i gruppi all'interno di tali gruppi e così via.</span><span class="sxs-lookup"><span data-stu-id="b4c14-109">The [**IADsGroup.IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) method does not recursively verify the members of groups in its member property, groups within those groups, and so on.</span></span> <span data-ttu-id="b4c14-110">Per verificare in modo ricorsivo che un oggetto sia membro di un gruppo, enumerare i gruppi nella proprietà del membro, verificare i membri di tali gruppi per verificare se l'oggetto è un membro e se tali gruppi contengono altri gruppi, verificarne i membri e così via.</span><span class="sxs-lookup"><span data-stu-id="b4c14-110">To recursively verify that an object is a member of a group, enumerate the groups in the member property, verify the members of those groups to see if the object is a member, and if those groups contain other groups, check their members, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="b4c14-111">Poiché i gruppi possono essere annidati, l'appartenenza al gruppo può avere cicli.</span><span class="sxs-lookup"><span data-stu-id="b4c14-111">Since groups can be nested, group membership may have loops.</span></span> <span data-ttu-id="b4c14-112">Qualsiasi script che enumera in molti gruppi deve tenere un elenco interno di gruppi per terminare la ricorsione se è già stato visitato un gruppo.</span><span class="sxs-lookup"><span data-stu-id="b4c14-112">Any script that enumerates over many groups should keep an internal list of groups to end recursion if a group has already been visited.</span></span>

 

 

 