---
description: Indica se connettersi a una rete nascosta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Elemento nonbroadcast (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308882"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="d48c9-103">Elemento nonbroadcast (SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="d48c9-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="d48c9-104">L'elemento nonbroadcast (SSIDConfig) indica se connettersi a una rete nascosta.</span><span class="sxs-lookup"><span data-stu-id="d48c9-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="d48c9-105">Se una rete non trasmette il proprio SSID, è nota come rete nascosta.</span><span class="sxs-lookup"><span data-stu-id="d48c9-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="d48c9-106">Se all'interno del profilo sono impostati più SSID, è necessario che tutti abbiano lo stesso valore non broadcast.</span><span class="sxs-lookup"><span data-stu-id="d48c9-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="d48c9-107">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su **ESS**, questo valore può essere "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="d48c9-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="d48c9-108">Se questo elemento non è presente, il valore predefinito è "false".</span><span class="sxs-lookup"><span data-stu-id="d48c9-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="d48c9-109">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su **IBSS**, questo valore deve essere "false".</span><span class="sxs-lookup"><span data-stu-id="d48c9-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="d48c9-110">Se questo elemento non è presente, il valore predefinito è "false".</span><span class="sxs-lookup"><span data-stu-id="d48c9-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="d48c9-111">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d48c9-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="d48c9-112">L'elemento è definito dall'elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d48c9-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d48c9-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="d48c9-113">Examples</span></span>

<span data-ttu-id="d48c9-114">Per visualizzare un profilo di esempio che usa l'elemento non **broadcast** , vedere [esempio di profilo non broadcast](non-broadcast-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d48c9-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d48c9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d48c9-115">Requirements</span></span>



| <span data-ttu-id="d48c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d48c9-116">Requirement</span></span> | <span data-ttu-id="d48c9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d48c9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d48c9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d48c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d48c9-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d48c9-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d48c9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d48c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d48c9-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d48c9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d48c9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d48c9-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="d48c9-123">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d48c9-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d48c9-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="d48c9-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d48c9-125">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d48c9-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d48c9-126">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="d48c9-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




