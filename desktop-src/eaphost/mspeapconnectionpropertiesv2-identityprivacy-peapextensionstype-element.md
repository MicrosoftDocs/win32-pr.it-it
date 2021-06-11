---
title: Elemento IdentityPrivacy (PeapExtensionsType)
description: L'elemento IdentityPrivacy (PeapExtensionsType) indica se la vera identità di un utente viene inviata nello schema mspeapconnectionpropertiesv2.
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Elemento IdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988947"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="1acb4-104">Elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="1acb4-104">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="1acb4-105">**L'elemento IdentityPrivacy (PeapExtensionsType)** indica se viene inviata la vera identità di un utente o un'identità anonima.</span><span class="sxs-lookup"><span data-stu-id="1acb4-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="1acb4-106">**L'elemento IdentityPrivacy** è definito dall'elemento [**PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="1acb4-106">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="1acb4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1acb4-107">Remarks</span></span>

<span data-ttu-id="1acb4-108">**L'elemento IdentityPrivacy** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1acb4-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1acb4-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1acb4-109">Requirements</span></span>



| <span data-ttu-id="1acb4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1acb4-110">Requirement</span></span> | <span data-ttu-id="1acb4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1acb4-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1acb4-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acb4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1acb4-113">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1acb4-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1acb4-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acb4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1acb4-115">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1acb4-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1acb4-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1acb4-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="1acb4-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="1acb4-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1acb4-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="1acb4-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="1acb4-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="1acb4-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1acb4-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="1acb4-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="1acb4-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1acb4-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1acb4-122">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="1acb4-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1acb4-123">Schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1acb4-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1acb4-124">Elementi dello schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1acb4-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





