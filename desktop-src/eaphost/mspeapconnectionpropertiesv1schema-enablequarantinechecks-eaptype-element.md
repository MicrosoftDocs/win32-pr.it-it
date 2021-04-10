---
title: Elemento EnableQuarantineChecks (EapType)
description: Informazioni sull'elemento EnableQuarantineChecks (EapType). Questo elemento indica se eseguire i controlli di protezione accesso alla rete (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Elemento EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963475"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="73f07-105">Elemento EnableQuarantineChecks (EapType)</span><span class="sxs-lookup"><span data-stu-id="73f07-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="73f07-106">L'elemento **EnableQuarantineChecks (EapType)** indica se eseguire i controlli di protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="73f07-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="73f07-107">L'elemento **EnableQuarantineChecks** è definito dall'elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="73f07-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="73f07-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="73f07-108">Remarks</span></span>

<span data-ttu-id="73f07-109">Se l'elemento **EnableQuarantineChecks** è true, PEAP eseguirà i controlli NAP; Se FALSE, PEAP non eseguirà controlli NAP.</span><span class="sxs-lookup"><span data-stu-id="73f07-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="73f07-110">L'elemento **EnableQuarantineChecks** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="73f07-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f07-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73f07-111">Requirements</span></span>



| <span data-ttu-id="73f07-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="73f07-112">Role</span></span> | <span data-ttu-id="73f07-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="73f07-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="73f07-114">Client</span><span class="sxs-lookup"><span data-stu-id="73f07-114">Client</span></span><br/> | <span data-ttu-id="73f07-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73f07-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73f07-116">Server</span><span class="sxs-lookup"><span data-stu-id="73f07-116">Server</span></span><br/> | <span data-ttu-id="73f07-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73f07-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73f07-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73f07-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="73f07-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="73f07-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="73f07-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="73f07-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="73f07-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="73f07-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="73f07-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="73f07-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="73f07-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="73f07-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="73f07-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="73f07-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="73f07-125">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="73f07-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="73f07-126">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="73f07-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





