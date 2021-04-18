---
title: BUTTON. Sticky
description: L'attributo Sticky specifica o recupera un valore che indica se il pulsante è un interruttore, ovvero se si tratta di un pulsante a due Stati o di uno stato singolo.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON. Sticky Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325261"
---
# <a name="buttonsticky"></a><span data-ttu-id="f416e-104">BUTTON. Sticky</span><span class="sxs-lookup"><span data-stu-id="f416e-104">BUTTON.sticky</span></span>

<span data-ttu-id="f416e-105">L'attributo **Sticky** specifica o recupera un valore che indica se il **pulsante** è un interruttore, ovvero se si tratta di un **pulsante** a due Stati o di uno stato singolo.</span><span class="sxs-lookup"><span data-stu-id="f416e-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="f416e-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f416e-106">Possible Values</span></span>

<span data-ttu-id="f416e-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f416e-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="f416e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="f416e-108">Value</span></span> | <span data-ttu-id="f416e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f416e-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="f416e-110">true</span><span class="sxs-lookup"><span data-stu-id="f416e-110">true</span></span>  | <span data-ttu-id="f416e-111">Il **pulsante** è appiccicoso.</span><span class="sxs-lookup"><span data-stu-id="f416e-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="f416e-112">false</span><span class="sxs-lookup"><span data-stu-id="f416e-112">false</span></span> | <span data-ttu-id="f416e-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f416e-113">Default.</span></span> <span data-ttu-id="f416e-114">Il **pulsante** non è appiccicoso.</span><span class="sxs-lookup"><span data-stu-id="f416e-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f416e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f416e-115">Remarks</span></span>

<span data-ttu-id="f416e-116">Se **Sticky** è impostato su true, il **pulsante** passerà allo stato inattivo quando si fa clic e rimarrà in tale stato fino a quando non si fa clic di nuovo su.</span><span class="sxs-lookup"><span data-stu-id="f416e-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="f416e-117">Quando il **pulsante** è nello stato di inattività, l'attributo **Down** sarà true e verrà visualizzato **downImage** .</span><span class="sxs-lookup"><span data-stu-id="f416e-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f416e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f416e-118">Requirements</span></span>



| <span data-ttu-id="f416e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f416e-119">Requirement</span></span> | <span data-ttu-id="f416e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f416e-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f416e-121">Versione</span><span class="sxs-lookup"><span data-stu-id="f416e-121">Version</span></span><br/> | <span data-ttu-id="f416e-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="f416e-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f416e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f416e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f416e-124">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="f416e-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="f416e-125">**PULSANTE in basso**</span><span class="sxs-lookup"><span data-stu-id="f416e-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="f416e-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="f416e-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





