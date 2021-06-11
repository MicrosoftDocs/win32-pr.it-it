---
title: Elemento AcceptServerName (PeapExtensionsType)
description: L'elemento AcceptServerName (PeapExtensionsType) indica se il nome del server viene convalidato rispetto alla stringa del nome specificata in ServerNames nello schema mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Elemento AcceptServerName EAPHost
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
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989476"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="aa1da-104">Elemento AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="aa1da-104">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="aa1da-105">**L'elemento AcceptServerName (PeapExtensionsType)** indica se il nome del server viene convalidato rispetto alla stringa del nome specificata nell'elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)</span><span class="sxs-lookup"><span data-stu-id="aa1da-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="aa1da-106">**L'elemento AcceptServerName** è definito dall'elemento [**PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="aa1da-106">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa1da-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa1da-107">Remarks</span></span>

<span data-ttu-id="aa1da-108">**L'elemento AcceptServerName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="aa1da-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1da-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa1da-109">Requirements</span></span>



| <span data-ttu-id="aa1da-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa1da-110">Requirement</span></span> | <span data-ttu-id="aa1da-111">Valore</span><span class="sxs-lookup"><span data-stu-id="aa1da-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="aa1da-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa1da-112">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1da-113">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa1da-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="aa1da-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa1da-114">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1da-115">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa1da-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa1da-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa1da-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa1da-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="aa1da-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="aa1da-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="aa1da-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="aa1da-119">**Possibile elemento padre diretto nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="aa1da-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="aa1da-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="aa1da-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="aa1da-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="aa1da-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="aa1da-122">Schema EAPHost e legacy</span><span class="sxs-lookup"><span data-stu-id="aa1da-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="aa1da-123">Schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="aa1da-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="aa1da-124">Elementi dello schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="aa1da-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





