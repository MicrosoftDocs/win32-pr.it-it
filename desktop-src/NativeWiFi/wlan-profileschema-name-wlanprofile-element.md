---
description: Contiene il nome di un profilo LAN wireless.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Elemento Name (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527787"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="e18ce-103">Elemento Name (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="e18ce-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="e18ce-104">L'elemento Name (WLANProfile) contiene il nome di un profilo LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="e18ce-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="e18ce-105">L'elemento **Name** viene definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e18ce-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e18ce-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="e18ce-106">Remarks</span></span>

<span data-ttu-id="e18ce-107">I nomi fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e18ce-107">Names are case-sensitive.</span></span>

<span data-ttu-id="e18ce-108">Per Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2), l'elemento Name viene ignorato quando il profilo viene salvato nell'archivio profili.</span><span class="sxs-lookup"><span data-stu-id="e18ce-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="e18ce-109">Il nome del profilo deriva dall'SSID della rete.</span><span class="sxs-lookup"><span data-stu-id="e18ce-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="e18ce-110">Per i profili di rete dell'infrastruttura, il nome del profilo è il SSID della rete.</span><span class="sxs-lookup"><span data-stu-id="e18ce-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="e18ce-111">Per i profili di rete ad hoc, il nome del profilo è il SSID della rete ad hoc seguita da `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="e18ce-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="e18ce-112">I caratteri di escape XML, ad esempio &, non vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="e18ce-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="e18ce-113">Evitare di utilizzare caratteri di escape XML nei nomi SSID per i profili distribuiti in Windows XP con SP3 o l'API LAN wireless per Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="e18ce-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="e18ce-114">Per qualsiasi profilo di rete destinato a essere utilizzato solo in Windows Vista o Windows Server 2008, il nome può essere qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="e18ce-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="e18ce-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="e18ce-115">Examples</span></span>

<span data-ttu-id="e18ce-116">Per visualizzare i profili di esempio che usano l'elemento **Name** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e18ce-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e18ce-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e18ce-117">Requirements</span></span>



| <span data-ttu-id="e18ce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e18ce-118">Requirement</span></span> | <span data-ttu-id="e18ce-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e18ce-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e18ce-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e18ce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e18ce-121">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e18ce-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e18ce-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e18ce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e18ce-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e18ce-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e18ce-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e18ce-124">Redistributable</span></span><br/>          | <span data-ttu-id="e18ce-125">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="e18ce-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e18ce-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e18ce-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e18ce-127">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e18ce-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e18ce-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="e18ce-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="e18ce-129">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e18ce-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e18ce-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="e18ce-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




