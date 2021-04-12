---
title: Funzioni di gestione gruppi multicast
description: Le funzioni seguenti vengono utilizzate per eseguire la registrazione con il gestore del gruppo multicast
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332124"
---
# <a name="multicast-group-manager-functions"></a><span data-ttu-id="fc0f4-103">Funzioni di gestione gruppi multicast</span><span class="sxs-lookup"><span data-stu-id="fc0f4-103">Multicast Group Manager Functions</span></span>

<span data-ttu-id="fc0f4-104">Per eseguire la registrazione con il gestore del gruppo multicast vengono utilizzate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc0f4-104">The following functions are used to register with the multicast group manager:</span></span>

[<span data-ttu-id="fc0f4-105">**MgmRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-105">**MgmRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[<span data-ttu-id="fc0f4-106">**MgmDeRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-106">**MgmDeRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

<span data-ttu-id="fc0f4-107">Per gestire la proprietà dell'interfaccia vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc0f4-107">The following functions are used to manage interface ownership:</span></span>

[<span data-ttu-id="fc0f4-108">**MgmGetProtocolOnInterface**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-108">**MgmGetProtocolOnInterface**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[<span data-ttu-id="fc0f4-109">**MgmTakeInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-109">**MgmTakeInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[<span data-ttu-id="fc0f4-110">**MgmReleaseInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-110">**MgmReleaseInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

<span data-ttu-id="fc0f4-111">Per gestire l'appartenenza al gruppo vengono utilizzate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc0f4-111">The following functions are used to manage group membership:</span></span>

[<span data-ttu-id="fc0f4-112">**MgmAddGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-112">**MgmAddGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[<span data-ttu-id="fc0f4-113">**MgmDeleteGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-113">**MgmDeleteGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

<span data-ttu-id="fc0f4-114">Le funzioni seguenti vengono utilizzate per ottenere le statistiche di inoltring multicast (MFE) e MFE:</span><span class="sxs-lookup"><span data-stu-id="fc0f4-114">The following functions are used to obtain multicast forwarding entries (MFEs) and MFE statistics:</span></span>

[<span data-ttu-id="fc0f4-115">**MgmGetFirstMfe**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-115">**MgmGetFirstMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[<span data-ttu-id="fc0f4-116">**MgmGetNextMfe**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-116">**MgmGetNextMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[<span data-ttu-id="fc0f4-117">**MgmGetMfe**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-117">**MgmGetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[<span data-ttu-id="fc0f4-118">**MgmGetFirstMfeStats**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-118">**MgmGetFirstMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[<span data-ttu-id="fc0f4-119">**MgmGetNextMfeStats**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-119">**MgmGetNextMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[<span data-ttu-id="fc0f4-120">**MgmGetMfeStats**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-120">**MgmGetMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

<span data-ttu-id="fc0f4-121">Per modificare MFE, viene usata la funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="fc0f4-121">The following function is used to modify MFEs:</span></span>

[<span data-ttu-id="fc0f4-122">**MgmSetMfe**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-122">**MgmSetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

<span data-ttu-id="fc0f4-123">Vengono usate le funzioni seguenti per ottenere un elenco di gruppi che sono stati aggiunti:</span><span class="sxs-lookup"><span data-stu-id="fc0f4-123">The following functions are used obtain a list of groups that have been joined:</span></span>

[<span data-ttu-id="fc0f4-124">**MgmGroupEnumerationStart**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-124">**MgmGroupEnumerationStart**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[<span data-ttu-id="fc0f4-125">**MgmGroupEnumerationGetNext**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-125">**MgmGroupEnumerationGetNext**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[<span data-ttu-id="fc0f4-126">**MgmGroupEnumerationEnd**</span><span class="sxs-lookup"><span data-stu-id="fc0f4-126">**MgmGroupEnumerationEnd**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




