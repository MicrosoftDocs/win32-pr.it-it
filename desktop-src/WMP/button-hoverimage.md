---
title: BUTTON. hoverImage
description: L'attributo hoverImage specifica o recupera l'immagine visualizzata quando il pulsante si trova nello stato up e l'utente posiziona il puntatore del mouse su di esso con il puntatore del mouse.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325449"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="39e14-104">BUTTON. hoverImage</span><span class="sxs-lookup"><span data-stu-id="39e14-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="39e14-105">L'attributo **hoverImage** specifica o recupera l'immagine visualizzata quando il **pulsante** si trova nello stato up e l'utente posiziona il puntatore del mouse su di esso con il puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="39e14-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="39e14-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="39e14-106">Possible Values</span></span>

<span data-ttu-id="39e14-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="39e14-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e14-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="39e14-108">Remarks</span></span>

<span data-ttu-id="39e14-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="39e14-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="39e14-110">L'immagine predefinita è quella specificata nell'attributo **Image** oppure il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="39e14-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="39e14-111">Se l'immagine del passaggio del mouse è maggiore dell'area definita nell'attributo di ambiente, l'immagine del passaggio del mouse verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="39e14-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="39e14-112">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="39e14-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e14-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39e14-113">Requirements</span></span>



| <span data-ttu-id="39e14-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e14-114">Requirement</span></span> | <span data-ttu-id="39e14-115">Valore</span><span class="sxs-lookup"><span data-stu-id="39e14-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="39e14-116">Versione</span><span class="sxs-lookup"><span data-stu-id="39e14-116">Version</span></span><br/> | <span data-ttu-id="39e14-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="39e14-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39e14-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39e14-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e14-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="39e14-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="39e14-120">**BUTTON. image**</span><span class="sxs-lookup"><span data-stu-id="39e14-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





