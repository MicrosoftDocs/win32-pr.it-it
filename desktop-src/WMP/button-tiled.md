---
title: PULSANTE affiancato
description: L'attributo affiancato specifica o recupera un valore che indica se l'immagine del pulsante verrà affiancata.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- PULSANTE. finestre affiancate Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333425"
---
# <a name="buttontiled"></a><span data-ttu-id="3283b-104">PULSANTE affiancato</span><span class="sxs-lookup"><span data-stu-id="3283b-104">BUTTON.tiled</span></span>

<span data-ttu-id="3283b-105">L'attributo **affiancato** specifica o recupera un valore che indica se l'immagine del **pulsante** verrà affiancata.</span><span class="sxs-lookup"><span data-stu-id="3283b-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="3283b-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3283b-106">Possible Values</span></span>

<span data-ttu-id="3283b-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3283b-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="3283b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3283b-108">Value</span></span> | <span data-ttu-id="3283b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3283b-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="3283b-110">true</span><span class="sxs-lookup"><span data-stu-id="3283b-110">true</span></span>  | <span data-ttu-id="3283b-111">L'immagine verrà affiancata.</span><span class="sxs-lookup"><span data-stu-id="3283b-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="3283b-112">false</span><span class="sxs-lookup"><span data-stu-id="3283b-112">false</span></span> | <span data-ttu-id="3283b-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3283b-113">Default.</span></span> <span data-ttu-id="3283b-114">L'immagine non verrà affiancata.</span><span class="sxs-lookup"><span data-stu-id="3283b-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3283b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3283b-115">Remarks</span></span>

<span data-ttu-id="3283b-116">Se l'immagine è più piccola dell'area effettiva del controllo, il affiancamento dell'immagine lo ripeterà fino a riempire l'intera area.</span><span class="sxs-lookup"><span data-stu-id="3283b-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="3283b-117">Se un'immagine non è specificata o non può essere recuperata, l'oggetto **affiancato** verrà impostato su false.</span><span class="sxs-lookup"><span data-stu-id="3283b-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="3283b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3283b-118">Requirements</span></span>



| <span data-ttu-id="3283b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3283b-119">Requirement</span></span> | <span data-ttu-id="3283b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3283b-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3283b-121">Versione</span><span class="sxs-lookup"><span data-stu-id="3283b-121">Version</span></span><br/> | <span data-ttu-id="3283b-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="3283b-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3283b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3283b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3283b-124">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="3283b-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="3283b-125">**BUTTON. image**</span><span class="sxs-lookup"><span data-stu-id="3283b-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





