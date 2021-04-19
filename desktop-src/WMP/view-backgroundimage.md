---
title: Visualizza. backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo della vista o della vista.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW. backgroundImage Media Player Windows
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325973"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="0f224-104">Visualizza. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="0f224-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="0f224-105">L'attributo **BackgroundImage** specifica o recupera l'immagine di sfondo della **vista** o **della vista.**</span><span class="sxs-lookup"><span data-stu-id="0f224-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="0f224-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0f224-106">Possible Values</span></span>

<span data-ttu-id="0f224-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0f224-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f224-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f224-108">Remarks</span></span>

<span data-ttu-id="0f224-109">I formati supportati sono BMP, JPG, GIF e PNG.</span><span class="sxs-lookup"><span data-stu-id="0f224-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="0f224-110">Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **backgroundImageHueShift** e **backgroundImageSaturation** .</span><span class="sxs-lookup"><span data-stu-id="0f224-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="0f224-111">In un pacchetto di download di Windows Media, se si specifica l'attributo **BackgroundImage** per un elemento di **visualizzazione** , è necessario specificare anche l'attributo **BackgroundColor** per quell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0f224-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f224-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f224-112">Requirements</span></span>



| <span data-ttu-id="0f224-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f224-113">Requirement</span></span> | <span data-ttu-id="0f224-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0f224-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0f224-115">Versione</span><span class="sxs-lookup"><span data-stu-id="0f224-115">Version</span></span><br/> | <span data-ttu-id="0f224-116">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="0f224-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f224-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f224-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f224-118">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="0f224-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="0f224-119">**Visualizza backgroundImageHueShift**</span><span class="sxs-lookup"><span data-stu-id="0f224-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="0f224-120">**Visualizza backgroundImageSaturation**</span><span class="sxs-lookup"><span data-stu-id="0f224-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





