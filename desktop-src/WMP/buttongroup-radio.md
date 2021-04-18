---
title: BUTTONGROUP. radio
description: L'attributo radio specifica o recupera un valore che indica se BUTTONGROUP è costituito da pulsanti di opzione.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- Media Player BUTTONGROUP. Radio Windows
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330254"
---
# <a name="buttongroupradio"></a><span data-ttu-id="601bd-104">BUTTONGROUP. radio</span><span class="sxs-lookup"><span data-stu-id="601bd-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="601bd-105">L'attributo **Radio** specifica o recupera un valore che indica se **ButtonGroup** è costituito da pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="601bd-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="601bd-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="601bd-106">Possible Values</span></span>

<span data-ttu-id="601bd-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="601bd-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="601bd-108">Valore</span><span class="sxs-lookup"><span data-stu-id="601bd-108">Value</span></span> | <span data-ttu-id="601bd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="601bd-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="601bd-110">true</span><span class="sxs-lookup"><span data-stu-id="601bd-110">true</span></span>  | <span data-ttu-id="601bd-111">**ButtonGroup** è uno stile radio.</span><span class="sxs-lookup"><span data-stu-id="601bd-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="601bd-112">false</span><span class="sxs-lookup"><span data-stu-id="601bd-112">false</span></span> | <span data-ttu-id="601bd-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="601bd-113">Default.</span></span> <span data-ttu-id="601bd-114">Il **ButtonGroup** non è di tipo radio.</span><span class="sxs-lookup"><span data-stu-id="601bd-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="601bd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="601bd-115">Remarks</span></span>

<span data-ttu-id="601bd-116">Se **Radio** è impostato su true, tutti gli elementi **ButtonElement** in **ButtonGroup** saranno permanenti, ma solo un pulsante alla volta sarà nello stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="601bd-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="601bd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="601bd-117">Requirements</span></span>



| <span data-ttu-id="601bd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="601bd-118">Requirement</span></span> | <span data-ttu-id="601bd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="601bd-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="601bd-120">Versione</span><span class="sxs-lookup"><span data-stu-id="601bd-120">Version</span></span><br/> | <span data-ttu-id="601bd-121">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="601bd-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="601bd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="601bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601bd-123">**BUTTONelement. Sticky**</span><span class="sxs-lookup"><span data-stu-id="601bd-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="601bd-124">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="601bd-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





