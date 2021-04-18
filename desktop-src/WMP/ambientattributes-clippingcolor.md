---
title: AmbientAttributes.clippingColor
description: L'attributo clippingColor specifica o Recupera il colore da ritagliare dalla bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- Media Player Windows AmbientAttributes. clippingColor
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331408"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="54002-104">AmbientAttributes.clippingColor</span><span class="sxs-lookup"><span data-stu-id="54002-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="54002-105">L'attributo **clippingColor** specifica o Recupera il colore da ritagliare dalla bitmap **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="54002-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="54002-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="54002-106">Possible Values</span></span>

<span data-ttu-id="54002-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="54002-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="54002-108">Valore</span><span class="sxs-lookup"><span data-stu-id="54002-108">Value</span></span>                                       | <span data-ttu-id="54002-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54002-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="54002-110">Auto</span><span class="sxs-lookup"><span data-stu-id="54002-110">Auto</span></span>                                        | <span data-ttu-id="54002-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="54002-111">Default.</span></span> <span data-ttu-id="54002-112">Viene utilizzato il colore nella posizione del pixel 0, 0.</span><span class="sxs-lookup"><span data-stu-id="54002-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="54002-113">qualsiasi valore di colore di Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="54002-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="54002-114">Viene utilizzato il colore di Internet Explorer specificato.</span><span class="sxs-lookup"><span data-stu-id="54002-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="54002-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="54002-115">Remarks</span></span>

<span data-ttu-id="54002-116">Il colore di ritaglio indica le aree di **clippingImage** (o **BackgroundImage** per la **visualizzazione** o la **visualizzazione**) che corrispondono a parti trasparenti e non selezionabili del controllo.</span><span class="sxs-lookup"><span data-stu-id="54002-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="54002-117">Il colore di ritaglio può indicare più aree da ritagliare. Viene emesso un avviso se **clippingImage** è un jpg per avvertire la perdita di colore in jpg.</span><span class="sxs-lookup"><span data-stu-id="54002-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="54002-118">L'attributo **clippingColor** non è supportato dall'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="54002-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="54002-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54002-119">Requirements</span></span>



| <span data-ttu-id="54002-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54002-120">Requirement</span></span> | <span data-ttu-id="54002-121">Valore</span><span class="sxs-lookup"><span data-stu-id="54002-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="54002-122">Versione</span><span class="sxs-lookup"><span data-stu-id="54002-122">Version</span></span><br/> | <span data-ttu-id="54002-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="54002-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54002-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54002-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54002-125">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="54002-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="54002-126">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="54002-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="54002-127">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="54002-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





