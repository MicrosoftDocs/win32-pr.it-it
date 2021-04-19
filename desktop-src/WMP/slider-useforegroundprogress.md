---
title: SLIDER. useForegroundProgress
description: L'attributo useForegroundProgress specifica o recupera un valore che indica se verrà utilizzato l'indicatore di stato in primo piano.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Media Player Windows SLIDER. useForegroundProgress
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325581"
---
# <a name="slideruseforegroundprogress"></a><span data-ttu-id="a489f-104">SLIDER. useForegroundProgress</span><span class="sxs-lookup"><span data-stu-id="a489f-104">SLIDER.useForegroundProgress</span></span>

<span data-ttu-id="a489f-105">L'attributo **useForegroundProgress** specifica o recupera un valore che indica se verrà utilizzato l'indicatore di stato in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a489f-105">The **useForegroundProgress** attribute specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="a489f-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a489f-106">Possible Values</span></span>

<span data-ttu-id="a489f-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a489f-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a489f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a489f-108">Value</span></span> | <span data-ttu-id="a489f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a489f-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="a489f-110">true</span><span class="sxs-lookup"><span data-stu-id="a489f-110">true</span></span>  | <span data-ttu-id="a489f-111">USA stato in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a489f-111">Use foreground progress.</span></span>                 |
| <span data-ttu-id="a489f-112">false</span><span class="sxs-lookup"><span data-stu-id="a489f-112">false</span></span> | <span data-ttu-id="a489f-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a489f-113">Default.</span></span> <span data-ttu-id="a489f-114">Non usare lo stato in primo piano.</span><span class="sxs-lookup"><span data-stu-id="a489f-114">Do not use foreground progress.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a489f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a489f-115">Remarks</span></span>

<span data-ttu-id="a489f-116">Questo attributo consente di usare l'attributo **foregroundProgress** , che viene usato principalmente per tenere traccia dello stato di avanzamento del download di un file multimediale, monitorando contemporaneamente la posizione di riproduzione corrente del file usando l'attributo **value** .</span><span class="sxs-lookup"><span data-stu-id="a489f-116">This attribute allows the use of the **foregroundProgress** attribute, which is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="a489f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a489f-117">Requirements</span></span>



| <span data-ttu-id="a489f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a489f-118">Requirement</span></span> | <span data-ttu-id="a489f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a489f-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a489f-120">Versione</span><span class="sxs-lookup"><span data-stu-id="a489f-120">Version</span></span><br/> | <span data-ttu-id="a489f-121">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a489f-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a489f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a489f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a489f-123">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="a489f-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="a489f-124">**SLIDER. foregroundProgress**</span><span class="sxs-lookup"><span data-stu-id="a489f-124">**SLIDER.foregroundProgress**</span></span>](slider-foregroundprogress.md)
</dt> <dt>

[<span data-ttu-id="a489f-125">**SLIDER. Value**</span><span class="sxs-lookup"><span data-stu-id="a489f-125">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





