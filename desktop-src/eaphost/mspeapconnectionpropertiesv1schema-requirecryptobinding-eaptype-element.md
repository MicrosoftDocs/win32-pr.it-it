---
title: Elemento RequireCryptoBinding (EapType)
description: Indica se eseguire l'autenticazione con i server che supportano la crittografia.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Elemento RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400837"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="c019e-104">Elemento RequireCryptoBinding (EapType)</span><span class="sxs-lookup"><span data-stu-id="c019e-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="c019e-105">L'elemento **RequireCryptoBinding (EapType)** indica se eseguire l'autenticazione con i server che supportano la crittografia.</span><span class="sxs-lookup"><span data-stu-id="c019e-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="c019e-106">L'elemento **RequireCryptoBinding** è definito dall'elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c019e-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c019e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c019e-107">Remarks</span></span>

<span data-ttu-id="c019e-108">Se l'elemento **RequireCryptoBinding** è true, PEAP eseguirà l'autenticazione con i server che non supportano Crypto; Se FALSE, PEAP eseguirà l'autenticazione solo con i server che supportano la crittografia.</span><span class="sxs-lookup"><span data-stu-id="c019e-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="c019e-109">L'elemento **RequireCryptoBinding** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c019e-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c019e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c019e-110">Requirements</span></span>



| <span data-ttu-id="c019e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c019e-111">Requirement</span></span> | <span data-ttu-id="c019e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c019e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c019e-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c019e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c019e-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c019e-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c019e-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c019e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c019e-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c019e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c019e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c019e-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c019e-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c019e-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c019e-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="c019e-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="c019e-120">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c019e-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c019e-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="c019e-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="c019e-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c019e-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c019e-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="c019e-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c019e-124">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c019e-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c019e-125">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c019e-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





