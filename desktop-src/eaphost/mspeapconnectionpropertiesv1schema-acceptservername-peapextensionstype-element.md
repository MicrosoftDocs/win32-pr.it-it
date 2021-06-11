---
title: Elemento AcceptServerName (PeapExtensionsType) (EAPHost)
description: L'elemento AcceptServerName (PeapExtensionsType) indica se il nome del server viene convalidato rispetto alla stringa del nome specificata in ServerNames nello schema mspeapconnectionpropertiesv1.
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
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989096"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="479c6-104">Elemento AcceptServerName (PeapExtensionsType) (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="479c6-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="479c6-105">**L'elemento AcceptServerName (PeapExtensionsType)** indica se il nome del server viene convalidato rispetto alla stringa del nome specificata nell'elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)</span><span class="sxs-lookup"><span data-stu-id="479c6-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="479c6-106">L'elemento è definito [**dall'elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="479c6-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="479c6-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="479c6-107">Remarks</span></span>

<span data-ttu-id="479c6-108">**L'elemento AcceptServerName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="479c6-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="479c6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="479c6-109">Requirements</span></span>



| <span data-ttu-id="479c6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="479c6-110">Requirement</span></span> | <span data-ttu-id="479c6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="479c6-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="479c6-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="479c6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="479c6-113">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="479c6-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="479c6-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="479c6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="479c6-115">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="479c6-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="479c6-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="479c6-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="479c6-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="479c6-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="479c6-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="479c6-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="479c6-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="479c6-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="479c6-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="479c6-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="479c6-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="479c6-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="479c6-122">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="479c6-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="479c6-123">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="479c6-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="479c6-124">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="479c6-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="479c6-125">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="479c6-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





