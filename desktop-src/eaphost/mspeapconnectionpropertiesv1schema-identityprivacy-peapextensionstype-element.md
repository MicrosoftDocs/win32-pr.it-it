---
title: Elemento IdentityPrivacy (PeapExtensionsType)
description: Indica se viene inviata un'identità vera o anonima dell'utente. | Elemento IdentityPrivacy (PeapExtensionsType)
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- elemento EAPHost
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
ms.openlocfilehash: ed566e9be0b9e194d24106f1c82d9a9d6d1a199d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321615"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="c9c37-105">Elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="c9c37-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="c9c37-106">L'elemento **IdentityPrivacy (PeapExtensionsType)** indica se viene inviata un'identità true o un'identità anonima dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c9c37-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="c9c37-107">L'elemento è definito dall'elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c37-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c37-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9c37-108">Remarks</span></span>

<span data-ttu-id="c9c37-109">L'elemento **IdentityPrivacy** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9c37-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c37-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9c37-110">Requirements</span></span>



| <span data-ttu-id="c9c37-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9c37-111">Requirement</span></span> | <span data-ttu-id="c9c37-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c9c37-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c9c37-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9c37-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c9c37-114">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c9c37-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c9c37-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9c37-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c9c37-116">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9c37-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9c37-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9c37-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9c37-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c9c37-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c9c37-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="c9c37-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="c9c37-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c9c37-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c9c37-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="c9c37-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="c9c37-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c9c37-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c9c37-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="c9c37-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c9c37-124">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c9c37-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c9c37-125">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c9c37-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c9c37-126">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="c9c37-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





