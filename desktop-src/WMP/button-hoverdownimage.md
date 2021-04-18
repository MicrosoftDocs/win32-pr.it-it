---
title: BUTTON. hoverDownImage
description: L'attributo hoverDownImage specifica o recupera l'immagine visualizzata quando il pulsante è nello stato di inattività e l'utente passa il puntatore del mouse su di esso.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325453"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="1a78f-104">BUTTON. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="1a78f-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="1a78f-105">L'attributo **hoverDownImage** specifica o recupera l'immagine visualizzata quando il **pulsante** è nello stato di inattività e l'utente passa il puntatore del mouse su di esso.</span><span class="sxs-lookup"><span data-stu-id="1a78f-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="1a78f-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1a78f-106">Possible Values</span></span>

<span data-ttu-id="1a78f-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="1a78f-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a78f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a78f-108">Remarks</span></span>

<span data-ttu-id="1a78f-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="1a78f-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="1a78f-110">L'immagine predefinita è quella specificata nell'attributo **downImage** o il relativo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1a78f-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="1a78f-111">Se l'immagine al passaggio del mouse è più grande dell'area definita nell'attributo di ambiente, l'immagine al passaggio del mouse verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="1a78f-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="1a78f-112">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="1a78f-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a78f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a78f-113">Requirements</span></span>



| <span data-ttu-id="1a78f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a78f-114">Requirement</span></span> | <span data-ttu-id="1a78f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1a78f-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1a78f-116">Versione</span><span class="sxs-lookup"><span data-stu-id="1a78f-116">Version</span></span><br/> | <span data-ttu-id="1a78f-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="1a78f-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a78f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a78f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a78f-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="1a78f-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="1a78f-120">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="1a78f-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





