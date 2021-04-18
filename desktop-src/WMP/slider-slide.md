---
title: SLIDER. Slide
description: L'attributo Slide specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo o viene rivelata gradualmente in una posizione statica sull'immagine di sfondo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Media Player SLIDER. Slide Windows
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330720"
---
# <a name="sliderslide"></a><span data-ttu-id="6ef21-104">SLIDER. Slide</span><span class="sxs-lookup"><span data-stu-id="6ef21-104">SLIDER.slide</span></span>

<span data-ttu-id="6ef21-105">L'attributo **Slide** specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo o viene rivelata gradualmente in una posizione statica sull'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="6ef21-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="6ef21-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6ef21-106">Possible Values</span></span>

<span data-ttu-id="6ef21-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6ef21-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="6ef21-108">Valore</span><span class="sxs-lookup"><span data-stu-id="6ef21-108">Value</span></span> | <span data-ttu-id="6ef21-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ef21-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="6ef21-110">true</span><span class="sxs-lookup"><span data-stu-id="6ef21-110">true</span></span>  | <span data-ttu-id="6ef21-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6ef21-111">Default.</span></span> <span data-ttu-id="6ef21-112">L'immagine di primo piano scorre sull'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="6ef21-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="6ef21-113">false</span><span class="sxs-lookup"><span data-stu-id="6ef21-113">false</span></span> | <span data-ttu-id="6ef21-114">L'immagine in primo piano viene rivelata sul posto sull'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="6ef21-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6ef21-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ef21-115">Remarks</span></span>

<span data-ttu-id="6ef21-116">Quando il dispositivo di scorrimento **thumbImage** viene spostato con il mouse, se la **diapositiva** è impostata su true, l'immagine in primo piano scorre come se venisse premuto dal dispositivo di scorrimento per coprire l'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="6ef21-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="6ef21-117">Se la **diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento spostasse l'immagine di sfondo dall'immagine in primo piano.</span><span class="sxs-lookup"><span data-stu-id="6ef21-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef21-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ef21-118">Requirements</span></span>



| <span data-ttu-id="6ef21-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ef21-119">Requirement</span></span> | <span data-ttu-id="6ef21-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6ef21-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6ef21-121">Versione</span><span class="sxs-lookup"><span data-stu-id="6ef21-121">Version</span></span><br/> | <span data-ttu-id="6ef21-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="6ef21-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ef21-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ef21-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef21-124">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="6ef21-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="6ef21-125">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="6ef21-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="6ef21-126">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="6ef21-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





