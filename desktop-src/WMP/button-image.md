---
title: BUTTON. image
description: L'attributo Image specifica o recupera l'immagine predefinita del pulsante.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON. Image Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331765"
---
# <a name="buttonimage"></a><span data-ttu-id="bf5e1-104">BUTTON. image</span><span class="sxs-lookup"><span data-stu-id="bf5e1-104">BUTTON.image</span></span>

<span data-ttu-id="bf5e1-105">L'attributo **Image** specifica o recupera l'immagine predefinita del **pulsante**.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="bf5e1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="bf5e1-106">Possible Values</span></span>

<span data-ttu-id="bf5e1-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf5e1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf5e1-108">Remarks</span></span>

<span data-ttu-id="bf5e1-109">I formati di immagine supportati sono BMP, JPG, PNG e GIF (incluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="bf5e1-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="bf5e1-110">Se l'immagine del **pulsante** è più grande dell'area definita dagli attributi **Width** e **Height** , l'immagine verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="bf5e1-111">Se l'immagine non è specificata, ma l' **altezza** e la **larghezza** sono, viene visualizzata l'immagine direttamente dietro il controllo.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="bf5e1-112">Ciò consente di semplificare il disegno dell'immagine nella **visualizzazione** stessa, riducendo il numero di file di immagine separati necessari.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="bf5e1-113">Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).</span><span class="sxs-lookup"><span data-stu-id="bf5e1-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf5e1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf5e1-114">Requirements</span></span>



| <span data-ttu-id="bf5e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf5e1-115">Requirement</span></span> | <span data-ttu-id="bf5e1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="bf5e1-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bf5e1-117">Versione</span><span class="sxs-lookup"><span data-stu-id="bf5e1-117">Version</span></span><br/> | <span data-ttu-id="bf5e1-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="bf5e1-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf5e1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf5e1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5e1-120">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="bf5e1-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





