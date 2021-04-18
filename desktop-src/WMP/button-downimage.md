---
title: BUTTON. downImage
description: L'attributo downImage specifica o recupera l'immagine che rappresenta lo stato di inattività del pulsante.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324583"
---
# <a name="buttondownimage"></a><span data-ttu-id="49e1d-104">BUTTON. downImage</span><span class="sxs-lookup"><span data-stu-id="49e1d-104">BUTTON.downImage</span></span>

<span data-ttu-id="49e1d-105">L'attributo **downImage** specifica o recupera l'immagine che rappresenta lo stato di inattività del **pulsante**.</span><span class="sxs-lookup"><span data-stu-id="49e1d-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="49e1d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="49e1d-106">Possible Values</span></span>

<span data-ttu-id="49e1d-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="49e1d-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e1d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="49e1d-108">Remarks</span></span>

<span data-ttu-id="49e1d-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="49e1d-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="49e1d-110">L'immagine predefinita è quella specificata nell'attributo **Image** oppure il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="49e1d-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="49e1d-111">Se l'immagine inattiva è più grande dell'area definita nell'attributo di ambiente, l'immagine in giù verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="49e1d-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="49e1d-112">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="49e1d-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e1d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49e1d-113">Requirements</span></span>



| <span data-ttu-id="49e1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e1d-114">Requirement</span></span> | <span data-ttu-id="49e1d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49e1d-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="49e1d-116">Versione</span><span class="sxs-lookup"><span data-stu-id="49e1d-116">Version</span></span><br/> | <span data-ttu-id="49e1d-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="49e1d-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49e1d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49e1d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e1d-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="49e1d-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="49e1d-120">**PULSANTE in basso**</span><span class="sxs-lookup"><span data-stu-id="49e1d-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="49e1d-121">**BUTTON. image**</span><span class="sxs-lookup"><span data-stu-id="49e1d-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





