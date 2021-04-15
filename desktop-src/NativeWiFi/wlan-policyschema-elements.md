---
description: Un profilo di criteri di rete LAN wireless (WLAN) nativo è costituito dagli elementi dello schema seguenti.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Elementi dello schema WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525764"
---
# <a name="wlan_policy-schema-elements"></a><span data-ttu-id="02937-103">\_Elementi dello schema del criterio WLAN</span><span class="sxs-lookup"><span data-stu-id="02937-103">WLAN\_policy Schema Elements</span></span>

<span data-ttu-id="02937-104">Un profilo di criteri di rete LAN wireless (WLAN) nativo è costituito dagli elementi dello schema seguenti.</span><span class="sxs-lookup"><span data-stu-id="02937-104">A Native Wifi wireless LAN (WLAN) policy profile is composed of the following schema elements.</span></span> <span data-ttu-id="02937-105">Tutti gli elementi denominati si trovano nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="02937-105">All of the named elements are in the namespace `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

<span data-ttu-id="02937-106">Nell'elenco seguente vengono illustrati gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo.</span><span class="sxs-lookup"><span data-stu-id="02937-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="02937-107">Viene applicato l'ordinamento degli elementi.</span><span class="sxs-lookup"><span data-stu-id="02937-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="02937-108">Non tutti gli elementi sono in tutti i profili, perché alcuni elementi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="02937-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="02937-109">Questo elenco non Mostra tutti i possibili elementi che possono essere visualizzati in un profilo, perché è possibile aggiungere elementi in **xs: qualsiasi** punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="02937-109">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="02937-110">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="02937-110">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
    -   [<span data-ttu-id="02937-111">**nome (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="02937-111">**name (WLANPolicy)**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)
    -   [<span data-ttu-id="02937-112">**Descrizione (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="02937-112">**description (WLANPolicy)**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)
    -   [<span data-ttu-id="02937-113">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="02937-113">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [<span data-ttu-id="02937-114">**enableAutoConfig (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="02937-114">**enableAutoConfig (globalFlags)**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [<span data-ttu-id="02937-115">**showDeniedNetwork (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="02937-115">**showDeniedNetwork (globalFlags)**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [<span data-ttu-id="02937-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span><span class="sxs-lookup"><span data-stu-id="02937-116">**allowEveryoneToCreateAllUserProfiles (globalFlags)**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [<span data-ttu-id="02937-117">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="02937-117">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [<span data-ttu-id="02937-118">**Allow (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="02937-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [<span data-ttu-id="02937-119">**rete (Consenti)**</span><span class="sxs-lookup"><span data-stu-id="02937-119">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
                -   [<span data-ttu-id="02937-120">**NetworkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="02937-120">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="02937-121">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="02937-121">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="02937-122">**blocco (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="02937-122">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [<span data-ttu-id="02937-123">**rete (blocco)**</span><span class="sxs-lookup"><span data-stu-id="02937-123">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
                -   [<span data-ttu-id="02937-124">**NetworkName (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="02937-124">**networkName (networkItemType)**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [<span data-ttu-id="02937-125">**networkType (networkItemType)**</span><span class="sxs-lookup"><span data-stu-id="02937-125">**networkType (networkItemType)**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [<span data-ttu-id="02937-126">**denyAllIBSS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="02937-126">**denyAllIBSS (networkFilter)**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [<span data-ttu-id="02937-127">**denyAllESS (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="02937-127">**denyAllESS (networkFilter)**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [<span data-ttu-id="02937-128">**profilatura (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="02937-128">**profileList (WLANPolicy)**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



