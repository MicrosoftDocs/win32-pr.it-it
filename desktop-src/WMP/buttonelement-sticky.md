---
title: BUTTONelement. Sticky
description: L'attributo Sticky specifica o recupera un valore che indica se BUTTONelement è un interruttore, ovvero se si tratta di un pulsante a due Stati o di uno stato singolo.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONelement. Sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329205"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="f34b9-104">BUTTONelement. Sticky</span><span class="sxs-lookup"><span data-stu-id="f34b9-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="f34b9-105">L'attributo **Sticky** specifica o recupera un valore che indica se **ButtonElement** è un interruttore, ovvero se si tratta di un pulsante a due Stati o di uno stato singolo.</span><span class="sxs-lookup"><span data-stu-id="f34b9-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="f34b9-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f34b9-106">Possible Values</span></span>

<span data-ttu-id="f34b9-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f34b9-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="f34b9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f34b9-108">Value</span></span> | <span data-ttu-id="f34b9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f34b9-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="f34b9-110">true</span><span class="sxs-lookup"><span data-stu-id="f34b9-110">true</span></span>  | <span data-ttu-id="f34b9-111">**ButtonElement** è appiccicoso.</span><span class="sxs-lookup"><span data-stu-id="f34b9-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="f34b9-112">false</span><span class="sxs-lookup"><span data-stu-id="f34b9-112">false</span></span> | <span data-ttu-id="f34b9-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f34b9-113">Default.</span></span> <span data-ttu-id="f34b9-114">**ButtonElement** non è appiccicoso.</span><span class="sxs-lookup"><span data-stu-id="f34b9-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f34b9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f34b9-115">Remarks</span></span>

<span data-ttu-id="f34b9-116">Se l'attributo **Sticky** è impostato su true, l'elemento Button passerà allo stato inattivo quando si fa clic su di esso e rimarrà in tale stato fino a quando non si fa clic di nuovo su.</span><span class="sxs-lookup"><span data-stu-id="f34b9-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="f34b9-117">Quando l'elemento Button si trova nello stato inattivo, l'attributo **Down** sarà true e verrà visualizzata la parte appropriata del gruppo di pulsanti **downImage** .</span><span class="sxs-lookup"><span data-stu-id="f34b9-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f34b9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f34b9-118">Requirements</span></span>



| <span data-ttu-id="f34b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f34b9-119">Requirement</span></span> | <span data-ttu-id="f34b9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f34b9-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f34b9-121">Versione</span><span class="sxs-lookup"><span data-stu-id="f34b9-121">Version</span></span><br/> | <span data-ttu-id="f34b9-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="f34b9-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f34b9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f34b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34b9-124">**BUTTONelement (elemento)**</span><span class="sxs-lookup"><span data-stu-id="f34b9-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="f34b9-125">**BUTTONelement. Down**</span><span class="sxs-lookup"><span data-stu-id="f34b9-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="f34b9-126">**BUTTONGROUP. downImage**</span><span class="sxs-lookup"><span data-stu-id="f34b9-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





