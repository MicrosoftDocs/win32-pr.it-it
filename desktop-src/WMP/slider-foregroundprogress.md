---
title: SLIDER. foregroundProgress
description: L'attributo foregroundProgress specifica o recupera la posizione corrente dell'indicatore di stato in primo piano come percentuale dell'area del dispositivo di scorrimento.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Media Player Windows SLIDER. foregroundProgress
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330722"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="348de-104">SLIDER. foregroundProgress</span><span class="sxs-lookup"><span data-stu-id="348de-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="348de-105">L'attributo **foregroundProgress** specifica o recupera la posizione corrente dell'indicatore di stato in primo piano come percentuale dell'area del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="348de-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="348de-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="348de-106">Possible Values</span></span>

<span data-ttu-id="348de-107">Questo attributo è un **numero** di lettura/scrittura (**float**) compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="348de-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="348de-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="348de-108">Remarks</span></span>

<span data-ttu-id="348de-109">Questo attributo viene usato principalmente per tenere traccia dello stato di avanzamento del download di un file multimediale, monitorando contemporaneamente la posizione di riproduzione corrente del file usando l'attributo **value** .</span><span class="sxs-lookup"><span data-stu-id="348de-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="348de-110">La posizione del cursore del dispositivo di scorrimento è vincolata all'area dello stato di avanzamento in primo piano.</span><span class="sxs-lookup"><span data-stu-id="348de-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="348de-111">Ciò consente di eseguire la ricerca interattiva solo all'interno della parte disponibile di un file di download.</span><span class="sxs-lookup"><span data-stu-id="348de-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="348de-112">Per usare questa funzionalità, l'attributo **useForegroundProgress** deve essere impostato su true.</span><span class="sxs-lookup"><span data-stu-id="348de-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="348de-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="348de-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="348de-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="348de-114">Requirements</span></span>



| <span data-ttu-id="348de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="348de-115">Requirement</span></span> | <span data-ttu-id="348de-116">Valore</span><span class="sxs-lookup"><span data-stu-id="348de-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="348de-117">Versione</span><span class="sxs-lookup"><span data-stu-id="348de-117">Version</span></span><br/> | <span data-ttu-id="348de-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="348de-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="348de-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="348de-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348de-120">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="348de-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="348de-121">**SLIDER. min**</span><span class="sxs-lookup"><span data-stu-id="348de-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="348de-122">**SLIDER. max**</span><span class="sxs-lookup"><span data-stu-id="348de-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="348de-123">**SLIDER. useForegroundProgress**</span><span class="sxs-lookup"><span data-stu-id="348de-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="348de-124">**SLIDER. Value**</span><span class="sxs-lookup"><span data-stu-id="348de-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





