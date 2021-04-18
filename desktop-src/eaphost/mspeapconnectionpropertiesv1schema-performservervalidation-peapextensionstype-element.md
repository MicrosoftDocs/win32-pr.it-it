---
title: Elemento PerformServerValidation (PeapExtensionsType) (schema v1)
description: Informazioni sull'elemento PerformServerValidation (PeapExtensionsType). Questo elemento indica se viene eseguita la convalida del server. | Elemento PerformServerValidation (PeapExtensionsType) (schema v1)
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321279"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="3554b-106">Elemento PerformServerValidation (PeapExtensionsType) (schema v1)</span><span class="sxs-lookup"><span data-stu-id="3554b-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="3554b-107">L'elemento **PerformServerValidation (PeapExtensionsType)** indica se viene eseguita la convalida del server.</span><span class="sxs-lookup"><span data-stu-id="3554b-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="3554b-108">L'elemento è definito dall'elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3554b-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3554b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3554b-109">Remarks</span></span>

<span data-ttu-id="3554b-110">L'elemento **PerformServerValidation** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3554b-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3554b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3554b-111">Requirements</span></span>



| <span data-ttu-id="3554b-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="3554b-112">Role</span></span> | <span data-ttu-id="3554b-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="3554b-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3554b-114">Client</span><span class="sxs-lookup"><span data-stu-id="3554b-114">Client</span></span><br/> | <span data-ttu-id="3554b-115">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3554b-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3554b-116">Server</span><span class="sxs-lookup"><span data-stu-id="3554b-116">Server</span></span><br/> | <span data-ttu-id="3554b-117">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3554b-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3554b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3554b-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3554b-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="3554b-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3554b-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="3554b-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="3554b-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="3554b-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3554b-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="3554b-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="3554b-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3554b-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3554b-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="3554b-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3554b-125">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3554b-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3554b-126">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3554b-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3554b-127">**PerformServerValidation(PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="3554b-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





