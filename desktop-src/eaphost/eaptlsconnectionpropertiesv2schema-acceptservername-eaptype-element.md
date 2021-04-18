---
title: Elemento AcceptServerName
description: Indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento ServerNames (ServerValidationParameters). | Elemento AcceptServerName
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Elemento AcceptServerName EAPHost
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
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321440"
---
# <a name="acceptservername-element"></a><span data-ttu-id="f45cf-105">Elemento AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="f45cf-105">AcceptServerName element</span></span>

<span data-ttu-id="f45cf-106">L'elemento **AcceptServerName (EapType)** indica se il nome del server viene convalidato in base alla stringa del nome specificata nell'elemento [**serverNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f45cf-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="f45cf-107">L'elemento **AcceptServerName** è definito dall'elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f45cf-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f45cf-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f45cf-108">Remarks</span></span>

<span data-ttu-id="f45cf-109">L'elemento **AcceptServerName** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f45cf-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f45cf-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f45cf-110">Requirements</span></span>



| <span data-ttu-id="f45cf-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f45cf-111">Requirement</span></span> | <span data-ttu-id="f45cf-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f45cf-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f45cf-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f45cf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f45cf-114">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f45cf-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f45cf-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f45cf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f45cf-116">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f45cf-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f45cf-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f45cf-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="f45cf-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="f45cf-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f45cf-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="f45cf-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="f45cf-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="f45cf-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f45cf-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="f45cf-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="f45cf-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f45cf-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f45cf-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="f45cf-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f45cf-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f45cf-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f45cf-125">Elementi dello schema eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f45cf-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f45cf-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="f45cf-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





