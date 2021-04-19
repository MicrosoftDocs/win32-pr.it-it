---
title: BUTTONGROUP. showBackground
description: L'attributo showBackground specifica o recupera un valore che indica se BUTTONGROUP Visualizza solo i pulsanti oppure Visualizza la bitmap completa specificata nell'attributo Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- Media Player Windows BUTTONGROUP. showBackground
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326481"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="890be-104">BUTTONGROUP. showBackground</span><span class="sxs-lookup"><span data-stu-id="890be-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="890be-105">L'attributo **showBackground** specifica o recupera un valore che indica se **ButtonGroup** Visualizza solo i pulsanti oppure Visualizza la bitmap completa specificata nell'attributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="890be-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="890be-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="890be-106">Possible Values</span></span>

<span data-ttu-id="890be-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="890be-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="890be-108">Valore</span><span class="sxs-lookup"><span data-stu-id="890be-108">Value</span></span> | <span data-ttu-id="890be-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="890be-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="890be-110">true</span><span class="sxs-lookup"><span data-stu-id="890be-110">true</span></span>  | <span data-ttu-id="890be-111">Vengono visualizzati i pulsanti e l'area non occupata dai pulsanti viene disegnata dalla bitmap dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="890be-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="890be-112">false</span><span class="sxs-lookup"><span data-stu-id="890be-112">false</span></span> | <span data-ttu-id="890be-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="890be-113">Default.</span></span> <span data-ttu-id="890be-114">Vengono visualizzati solo i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="890be-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="890be-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="890be-115">Remarks</span></span>

<span data-ttu-id="890be-116">Quando **showBackground** è true, l'intera **immagine** principale sarà visibile.</span><span class="sxs-lookup"><span data-stu-id="890be-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="890be-117">Quando **showBackground** è false, verrà eseguito il rendering solo delle aree corrispondenti ai colori **mappingImage** assegnati.</span><span class="sxs-lookup"><span data-stu-id="890be-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="890be-118">In altre parole, sarà visibile solo **BUTTONELEMENTs** con la loro **mappingColor** assegnata.</span><span class="sxs-lookup"><span data-stu-id="890be-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="890be-119">Se viene specificato un valore non valido, viene mantenuto lo stato precedente.</span><span class="sxs-lookup"><span data-stu-id="890be-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="890be-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="890be-120">Requirements</span></span>



| <span data-ttu-id="890be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="890be-121">Requirement</span></span> | <span data-ttu-id="890be-122">Valore</span><span class="sxs-lookup"><span data-stu-id="890be-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="890be-123">Versione</span><span class="sxs-lookup"><span data-stu-id="890be-123">Version</span></span><br/> | <span data-ttu-id="890be-124">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="890be-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="890be-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="890be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="890be-126">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="890be-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="890be-127">**BUTTONelement. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="890be-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="890be-128">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="890be-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="890be-129">**BUTTONGROUP. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="890be-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





