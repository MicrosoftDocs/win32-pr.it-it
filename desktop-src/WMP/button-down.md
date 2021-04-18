---
title: PULSANTE in basso
description: L'attributo Down specifica o recupera un valore che indica se il pulsante si trova nella posizione verso l'alto o verso il basso.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BUTTON. Down Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328893"
---
# <a name="buttondown"></a><span data-ttu-id="14b1a-104">PULSANTE in basso</span><span class="sxs-lookup"><span data-stu-id="14b1a-104">BUTTON.down</span></span>

<span data-ttu-id="14b1a-105">L'attributo **Down** specifica o recupera un valore che indica se il **pulsante** si trova nella posizione verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="14b1a-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="14b1a-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="14b1a-106">Possible Values</span></span>

<span data-ttu-id="14b1a-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="14b1a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="14b1a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="14b1a-108">Value</span></span> | <span data-ttu-id="14b1a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14b1a-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="14b1a-110">true</span><span class="sxs-lookup"><span data-stu-id="14b1a-110">true</span></span>  | <span data-ttu-id="14b1a-111">Indica che il **pulsante** si trova nella posizione in giù.</span><span class="sxs-lookup"><span data-stu-id="14b1a-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="14b1a-112">false</span><span class="sxs-lookup"><span data-stu-id="14b1a-112">false</span></span> | <span data-ttu-id="14b1a-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="14b1a-113">Default.</span></span> <span data-ttu-id="14b1a-114">Indica che il **pulsante** si trova nella posizione verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="14b1a-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14b1a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="14b1a-115">Remarks</span></span>

<span data-ttu-id="14b1a-116">Affinché un **pulsante** rimanga nella posizione in giù, **Sticky** deve essere impostato su true.</span><span class="sxs-lookup"><span data-stu-id="14b1a-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="14b1a-117">Per impostazione predefinita, **Sticky** è false e qualsiasi tentativo **di impostare il valore su** true verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="14b1a-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="14b1a-118">Se viene specificato un valore non valido, viene mantenuto lo stato precedente.</span><span class="sxs-lookup"><span data-stu-id="14b1a-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b1a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14b1a-119">Requirements</span></span>



| <span data-ttu-id="14b1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b1a-120">Requirement</span></span> | <span data-ttu-id="14b1a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="14b1a-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="14b1a-122">Versione</span><span class="sxs-lookup"><span data-stu-id="14b1a-122">Version</span></span><br/> | <span data-ttu-id="14b1a-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="14b1a-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14b1a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14b1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b1a-125">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="14b1a-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="14b1a-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="14b1a-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="14b1a-127">**BUTTON. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="14b1a-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





