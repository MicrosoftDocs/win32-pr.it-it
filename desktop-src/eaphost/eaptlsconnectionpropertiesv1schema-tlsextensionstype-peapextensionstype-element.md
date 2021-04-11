---
title: AcceptServerName
description: Indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234768"
---
# <a name="acceptservername"></a><span data-ttu-id="e7940-105">AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="e7940-105">AcceptServerName</span></span>

<span data-ttu-id="e7940-106">L'elemento **AcceptServerName (EapType)** indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento [**serverNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e7940-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="e7940-107">L'elemento è definito dall'elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e7940-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7940-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7940-108">Remarks</span></span>

<span data-ttu-id="e7940-109">L'elemento **AcceptServerName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e7940-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7940-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7940-110">Requirements</span></span>



| <span data-ttu-id="e7940-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7940-111">Requirement</span></span> | <span data-ttu-id="e7940-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e7940-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e7940-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7940-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e7940-114">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7940-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e7940-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7940-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e7940-116">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7940-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7940-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7940-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7940-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e7940-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e7940-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e7940-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e7940-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e7940-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e7940-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e7940-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="e7940-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e7940-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e7940-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="e7940-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e7940-124">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e7940-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e7940-125">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e7940-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e7940-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="e7940-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





