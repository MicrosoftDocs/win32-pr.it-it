---
description: Contiene un elenco di profili da applicare a livello di dominio o di computer.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento Profiler (LANPolicy)
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
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314760"
---
# <a name="profilelist-lanpolicy-element"></a><span data-ttu-id="4afe0-103">Elemento Profiler (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="4afe0-103">profileList (LANPolicy) Element</span></span>

<span data-ttu-id="4afe0-104">L'elemento Profiler (LANPolicy) contiene un elenco di profili da applicare a livello di dominio o di computer.</span><span class="sxs-lookup"><span data-stu-id="4afe0-104">The profileList (LANPolicy) element contains a list of profiles to be applied at the domain or machine level.</span></span> <span data-ttu-id="4afe0-105">I profili devono essere basati sullo [ \_ schema del profilo LAN](lan-profileschema-schema.md), con un elemento radice di [**LANProfile**](lan-profileschema-lanprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="4afe0-105">Profiles must be based on the [LAN\_profile schema](lan-profileschema-schema.md), with a root element of [**LANProfile**](lan-profileschema-lanprofile-element.md).</span></span> <span data-ttu-id="4afe0-106">I profili basati su qualsiasi altro schema verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="4afe0-106">Profiles based on any other schema will be ignored.</span></span>

<span data-ttu-id="4afe0-107">Quando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) è impostato su false, questo elemento non deve essere presente in un profilo criteri LAN.</span><span class="sxs-lookup"><span data-stu-id="4afe0-107">When [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) is set to FALSE, this element must not be present in a LAN policy profile.</span></span> <span data-ttu-id="4afe0-108">Quando **enableAutoConfig** è impostato su true, questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4afe0-108">When **enableAutoConfig** is set to TRUE, then this element is required.</span></span>

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

<span data-ttu-id="4afe0-109">L'elemento **Profiler** è definito dall'elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4afe0-109">The **profileList** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4afe0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4afe0-110">Remarks</span></span>

<span data-ttu-id="4afe0-111">Questo elemento deve contenere esattamente un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="4afe0-111">This element should contain exactly one network profile.</span></span> <span data-ttu-id="4afe0-112">Se nei criteri è specificato più di un profilo, verrà applicata solo la prima rete.</span><span class="sxs-lookup"><span data-stu-id="4afe0-112">If more than one profile is specified in the policy, only the first network will be applied.</span></span>

## <a name="requirements"></a><span data-ttu-id="4afe0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4afe0-113">Requirements</span></span>



| <span data-ttu-id="4afe0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4afe0-114">Requirement</span></span> | <span data-ttu-id="4afe0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4afe0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4afe0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4afe0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4afe0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4afe0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4afe0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4afe0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4afe0-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4afe0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4afe0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4afe0-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4afe0-121">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="4afe0-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4afe0-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="4afe0-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="4afe0-123">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="4afe0-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4afe0-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="4afe0-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




