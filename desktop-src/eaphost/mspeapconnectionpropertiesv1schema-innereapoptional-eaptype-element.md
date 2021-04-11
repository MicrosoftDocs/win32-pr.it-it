---
title: Elemento InnerEapOptional (EapType)
description: Informazioni sull'elemento InnerEapOptional (EapType). Questo elemento indica se eseguire l'accesso GUEST.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Elemento InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118443"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="b31b4-105">Elemento InnerEapOptional (EapType)</span><span class="sxs-lookup"><span data-stu-id="b31b4-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="b31b4-106">L'elemento **InnerEapOptional (EapType)** indica se eseguire l'accesso guest.</span><span class="sxs-lookup"><span data-stu-id="b31b4-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="b31b4-107">L'elemento **InnerEapOptional** è definito dall'elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b31b4-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b31b4-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="b31b4-108">Remarks</span></span>

<span data-ttu-id="b31b4-109">Se l'elemento **InnerEapOptional** è true, è necessario che l'elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) sia presente e descriva il metodo interno e la relativa configurazione. Se FALSE, PEAP eseguirà l'accesso GUEST.</span><span class="sxs-lookup"><span data-stu-id="b31b4-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="b31b4-110">L'elemento **InnerEapOptional** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b31b4-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b31b4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b31b4-111">Requirements</span></span>



| <span data-ttu-id="b31b4-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="b31b4-112">Role</span></span> | <span data-ttu-id="b31b4-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="b31b4-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b31b4-114">Client</span><span class="sxs-lookup"><span data-stu-id="b31b4-114">Client</span></span><br/> | <span data-ttu-id="b31b4-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b31b4-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b31b4-116">Server</span><span class="sxs-lookup"><span data-stu-id="b31b4-116">Server</span></span><br/> | <span data-ttu-id="b31b4-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b31b4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b31b4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b31b4-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="b31b4-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b31b4-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b31b4-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="b31b4-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="b31b4-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b31b4-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b31b4-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="b31b4-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="b31b4-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b31b4-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="b31b4-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="b31b4-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b31b4-125">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b31b4-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b31b4-126">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b31b4-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





