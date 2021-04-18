---
title: AmbientAttributes.clippingImage
description: L'attributo clippingImage specifica o recupera l'area in cui ritagliare il controllo.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Media Player Windows AmbientAttributes. clippingImage
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331407"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="c7763-104">AmbientAttributes.clippingImage</span><span class="sxs-lookup"><span data-stu-id="c7763-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="c7763-105">L'attributo **clippingImage** specifica o recupera l'area in cui ritagliare il controllo.</span><span class="sxs-lookup"><span data-stu-id="c7763-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="c7763-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c7763-106">Possible Values</span></span>

<span data-ttu-id="c7763-107">Questo attributo è una **stringa** di lettura/scrittura che indica il nome del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="c7763-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="c7763-108">e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c7763-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7763-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7763-109">Remarks</span></span>

<span data-ttu-id="c7763-110">L'attributo **clippingImage** supporta file PNG, jpg, BMP e gif (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="c7763-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="c7763-111">Poiché i jpg sono con perdita di perdite e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate per le immagini di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="c7763-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="c7763-112">Questo attributo è utile quando si desidera visualizzare solo una parte dell'immagine del controllo e non l'intera area rettangolare.</span><span class="sxs-lookup"><span data-stu-id="c7763-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="c7763-113">L'attributo **clippingColor** indica le aree dell'immagine di ritaglio che corrispondono a parti trasparenti e non selezionabili del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7763-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="c7763-114">Il controllo può quindi essere di qualsiasi forma.</span><span class="sxs-lookup"><span data-stu-id="c7763-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="c7763-115">Per ottenere risultati ottimali, l'immagine di ritaglio deve avere le stesse dimensioni dell'immagine del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7763-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="c7763-116">L'attributo **clippingImage** non è supportato dagli elementi **playlist**, **View** e **subview** .</span><span class="sxs-lookup"><span data-stu-id="c7763-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="c7763-117">Un'immagine di ritaglio non funzionerà con l'elemento **video** se *video*. senza **finestra** è impostato su false, né con l'elemento **Effects** se *Effects*. **windowed** è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="c7763-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="c7763-118">Poiché l'uso di immagini di ritaglio impone una riduzione delle prestazioni, non è consigliabile usarle quando l'efficienza è un problema.</span><span class="sxs-lookup"><span data-stu-id="c7763-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="c7763-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="c7763-119">Examples</span></span>

<span data-ttu-id="c7763-120">Per un esempio che illustra l'uso di questo attributo, vedere l'attributo [ButtonElement. mappingColor](buttonelement-mappingcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="c7763-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7763-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7763-121">Requirements</span></span>



| <span data-ttu-id="c7763-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7763-122">Requirement</span></span> | <span data-ttu-id="c7763-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c7763-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c7763-124">Versione</span><span class="sxs-lookup"><span data-stu-id="c7763-124">Version</span></span><br/> | <span data-ttu-id="c7763-125">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="c7763-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7763-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7763-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7763-127">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="c7763-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7763-128">**AmbientAttributes.clippingColor**</span><span class="sxs-lookup"><span data-stu-id="c7763-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





