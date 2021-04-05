---
title: Costanti dell'agente di raccolta eventi Windows (Evcoll. h)
description: Windows Event Collector SDK contiene le costanti seguenti.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739743"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="d3e3c-103">Costanti dell'agente di raccolta eventi Windows</span><span class="sxs-lookup"><span data-stu-id="d3e3c-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="d3e3c-104">Windows Event Collector SDK contiene le costanti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="d3e3c-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_maschera di \_ tipo \_ variante EC**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="d3e3c-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-107">Utilizzato per mascherare il bit della matrice dalla proprietà **Type** di una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) per estrarre il tipo del valore Variant.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e3c-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_matrice di \_ tipi \_ Variant EC**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-109">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="d3e3c-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-110">Quando questo bit viene impostato nella proprietà **Type** di una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), la variante contiene un puntatore a una matrice di valori, anziché il valore stesso.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e3c-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_accesso in lettura EC \_**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-112">1</span><span class="sxs-lookup"><span data-stu-id="d3e3c-112">1</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-113">Autorizzazione di controllo di accesso in lettura che consente di leggere le informazioni dall'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e3c-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_accesso in scrittura EC \_**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-115">2</span><span class="sxs-lookup"><span data-stu-id="d3e3c-115">2</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-116">Autorizzazione di controllo di accesso in scrittura che consente la scrittura di informazioni nell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e3c-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ aperto \_ sempre**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-118">0</span><span class="sxs-lookup"><span data-stu-id="d3e3c-118">0</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-119">Apre una sottoscrizione esistente o crea la sottoscrizione, se non esiste.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="d3e3c-120">Utilizzato dal metodo [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="d3e3c-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e3c-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ Crea \_ nuovo**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-122">1</span><span class="sxs-lookup"><span data-stu-id="d3e3c-122">1</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-123">Flag passato alla funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) che specifica che deve essere creata una nuova sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3e3c-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ aperto \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="d3e3c-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e3c-125">2</span><span class="sxs-lookup"><span data-stu-id="d3e3c-125">2</span></span>
</dt> <dt>



<span data-ttu-id="d3e3c-126">Flag passato alla funzione [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) che specifica che deve essere aperta una sottoscrizione esistente.</span><span class="sxs-lookup"><span data-stu-id="d3e3c-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3e3c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3e3c-127">Requirements</span></span>



| <span data-ttu-id="d3e3c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e3c-128">Requirement</span></span> | <span data-ttu-id="d3e3c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d3e3c-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e3c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3e3c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e3c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3e3c-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="d3e3c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3e3c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e3c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3e3c-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="d3e3c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3e3c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e3c-135"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e3c-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





