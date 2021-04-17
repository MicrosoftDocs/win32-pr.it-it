---
title: Elemento per riconnessione rapida (EapType)
description: Informazioni sull'elemento per riconnessione rapida (EapType). Questo elemento indica se eseguire una riconnessione rapida.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento per riconnessione rapida EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300438"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="5020c-105">Elemento per riconnessione rapida (EapType)</span><span class="sxs-lookup"><span data-stu-id="5020c-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="5020c-106">L'elemento **per riconnessione rapida (EapType)** indica se eseguire una riconnessione rapida.</span><span class="sxs-lookup"><span data-stu-id="5020c-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="5020c-107">L'elemento **per riconnessione rapida** è definito dall'elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5020c-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5020c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5020c-108">Remarks</span></span>

<span data-ttu-id="5020c-109">Se l'elemento **per riconnessione rapida** è true, PEAP tenta di eseguire una riconnessione rapida. Se FALSE, PEAP esegue l'autenticazione completa.</span><span class="sxs-lookup"><span data-stu-id="5020c-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="5020c-110">L'elemento **per riconnessione rapida** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5020c-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5020c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5020c-111">Requirements</span></span>



| <span data-ttu-id="5020c-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="5020c-112">Role</span></span> | <span data-ttu-id="5020c-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="5020c-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="5020c-114">Client</span><span class="sxs-lookup"><span data-stu-id="5020c-114">Client</span></span><br/> | <span data-ttu-id="5020c-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5020c-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5020c-116">Server</span><span class="sxs-lookup"><span data-stu-id="5020c-116">Server</span></span><br/> | <span data-ttu-id="5020c-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5020c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5020c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5020c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="5020c-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="5020c-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5020c-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="5020c-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="5020c-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="5020c-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5020c-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="5020c-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="5020c-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5020c-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5020c-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="5020c-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5020c-125">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5020c-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5020c-126">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5020c-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





