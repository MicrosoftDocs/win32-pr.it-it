---
title: Elemento AcceptServerName (PeapExtensionsType)
description: Indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | Elemento AcceptServerName (PeapExtensionsType)
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c877819fd559cb26cd93c5d5456631a93a49545
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058530"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="c853d-105">Elemento AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="c853d-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="c853d-106">L'elemento **AcceptServerName (PeapExtensionsType)** indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c853d-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="c853d-107">L'elemento è definito dall'elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c853d-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c853d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c853d-108">Remarks</span></span>

<span data-ttu-id="c853d-109">L'elemento **AcceptServerName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c853d-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c853d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c853d-110">Requirements</span></span>



| <span data-ttu-id="c853d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c853d-111">Requirement</span></span> | <span data-ttu-id="c853d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c853d-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c853d-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c853d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c853d-114">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c853d-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c853d-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c853d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c853d-116">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c853d-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c853d-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c853d-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c853d-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c853d-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c853d-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="c853d-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="c853d-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c853d-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c853d-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="c853d-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="c853d-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c853d-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c853d-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="c853d-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c853d-124">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c853d-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c853d-125">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c853d-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c853d-126">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="c853d-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





