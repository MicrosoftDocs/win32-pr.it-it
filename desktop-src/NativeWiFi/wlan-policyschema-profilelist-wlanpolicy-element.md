---
description: 'Elemento profileList (WLANPolicy): contiene un elenco di profili da applicare a livello di dominio o computer.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Elemento profileList (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109199"
---
# <a name="profilelist-wlanpolicy-element"></a><span data-ttu-id="6661a-103">Elemento profileList (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="6661a-103">profileList (WLANPolicy) Element</span></span>

<span data-ttu-id="6661a-104">L'elemento profileList (WLANPolicy) contiene un elenco di profili da applicare a livello di dominio o computer.</span><span class="sxs-lookup"><span data-stu-id="6661a-104">The profileList (WLANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="6661a-105">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6661a-105">This element is optional.</span></span> <span data-ttu-id="6661a-106">Se questo elemento è presente, deve contenere almeno un profilo.</span><span class="sxs-lookup"><span data-stu-id="6661a-106">If this element is present, it must contain at least one profile.</span></span>

<span data-ttu-id="6661a-107">I profili devono essere basati sullo [ \_ schema del profilo WLAN](wlan-profileschema-schema.md), con un elemento radice [**di WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="6661a-107">Profiles should be based on the [WLAN\_profile schema](wlan-profileschema-schema.md), with a root element of [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).</span></span>

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6661a-108">**L'elemento profileList** è definito dall'elemento [**WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)</span><span class="sxs-lookup"><span data-stu-id="6661a-108">The **profileList** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6661a-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6661a-109">Requirements</span></span>



| <span data-ttu-id="6661a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6661a-110">Requirement</span></span> | <span data-ttu-id="6661a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6661a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6661a-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6661a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6661a-113">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6661a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6661a-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6661a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6661a-115">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6661a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6661a-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6661a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="6661a-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="6661a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6661a-118">**Criteri WLAN**</span><span class="sxs-lookup"><span data-stu-id="6661a-118">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="6661a-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="6661a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6661a-120">**Criteri WLAN**</span><span class="sxs-lookup"><span data-stu-id="6661a-120">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




