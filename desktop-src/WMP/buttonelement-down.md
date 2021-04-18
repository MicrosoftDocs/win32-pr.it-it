---
title: BUTTONelement. Down
description: L'attributo Down specifica o recupera un valore che indica se l'elemento Button si trova nella posizione verso l'alto o verso il basso.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONelement. Down Media Player di Windows
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329087"
---
# <a name="buttonelementdown"></a><span data-ttu-id="21ed9-104">BUTTONelement. Down</span><span class="sxs-lookup"><span data-stu-id="21ed9-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="21ed9-105">L'attributo **Down** specifica o recupera un valore che indica se l'elemento Button si trova nella posizione verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="21ed9-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="21ed9-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="21ed9-106">Possible Values</span></span>

<span data-ttu-id="21ed9-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="21ed9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="21ed9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="21ed9-108">Value</span></span> | <span data-ttu-id="21ed9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21ed9-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="21ed9-110">true</span><span class="sxs-lookup"><span data-stu-id="21ed9-110">true</span></span>  | <span data-ttu-id="21ed9-111">Indica che il **pulsante** è nella posizione in giù.</span><span class="sxs-lookup"><span data-stu-id="21ed9-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="21ed9-112">false</span><span class="sxs-lookup"><span data-stu-id="21ed9-112">false</span></span> | <span data-ttu-id="21ed9-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="21ed9-113">Default.</span></span> <span data-ttu-id="21ed9-114">Indica che il **pulsante** è nella posizione verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="21ed9-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="21ed9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="21ed9-115">Remarks</span></span>

<span data-ttu-id="21ed9-116">Affinché un elemento Button rimanga nella posizione in giù, **Sticky** deve essere impostato su true.</span><span class="sxs-lookup"><span data-stu-id="21ed9-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="21ed9-117">Per impostazione predefinita, **Sticky** è false e qualsiasi tentativo **di impostare il valore su** true verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="21ed9-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="21ed9-118">Se viene specificato un valore non valido, viene mantenuto lo stato precedente.</span><span class="sxs-lookup"><span data-stu-id="21ed9-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ed9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21ed9-119">Requirements</span></span>



| <span data-ttu-id="21ed9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ed9-120">Requirement</span></span> | <span data-ttu-id="21ed9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="21ed9-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="21ed9-122">Versione</span><span class="sxs-lookup"><span data-stu-id="21ed9-122">Version</span></span><br/> | <span data-ttu-id="21ed9-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="21ed9-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21ed9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21ed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ed9-125">**BUTTONelement (elemento)**</span><span class="sxs-lookup"><span data-stu-id="21ed9-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="21ed9-126">**BUTTONelement. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="21ed9-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





