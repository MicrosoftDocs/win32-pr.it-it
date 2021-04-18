---
title: BUTTONGROUP. mappingImage
description: L'attributo mappingImage specifica o Recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- Media Player Windows BUTTONGROUP. mappingImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330257"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="5470a-104">BUTTONGROUP. mappingImage</span><span class="sxs-lookup"><span data-stu-id="5470a-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="5470a-105">L'attributo **mappingImage** specifica o Recupera il nome dell'immagine che rappresenta la mappa dei pulsanti di **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="5470a-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="5470a-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5470a-106">Possible Values</span></span>

<span data-ttu-id="5470a-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5470a-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5470a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="5470a-108">Remarks</span></span>

<span data-ttu-id="5470a-109">Si tratta di un attributo obbligatorio che è necessario specificare.</span><span class="sxs-lookup"><span data-stu-id="5470a-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="5470a-110">L'immagine di mapping deve avere le stesse dimensioni dell' **immagine** principale.</span><span class="sxs-lookup"><span data-stu-id="5470a-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="5470a-111">Si tratta di una mappa delle aree selezionabili dell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="5470a-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="5470a-112">Costruire la mappa riempiendo ogni area selezionabile con un colore diverso.</span><span class="sxs-lookup"><span data-stu-id="5470a-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="5470a-113">Quando si definiscono i **pulsantielement**, designare il colore dalla mappa utilizzando l'attributo **mappingColor** .</span><span class="sxs-lookup"><span data-stu-id="5470a-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="5470a-114">Se, ad esempio, nell'immagine principale è presente una rappresentazione grafica di un pulsante con segno di arresto, è possibile creare una mappa con l'area del segno rosso colorato.</span><span class="sxs-lookup"><span data-stu-id="5470a-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="5470a-115">L'attributo **ButtonElement** deve quindi essere specificato come rosso per fare clic sull'immagine di stop-sign.</span><span class="sxs-lookup"><span data-stu-id="5470a-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="5470a-116">I formati di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="5470a-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="5470a-117">Poiché i jpg sono con perdita di perdite e pertanto sono soggetti a variazioni di colore impreviste, non sono consigliate per il mapping delle immagini.</span><span class="sxs-lookup"><span data-stu-id="5470a-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="5470a-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="5470a-118">Examples</span></span>

<span data-ttu-id="5470a-119">L'illustrazione seguente è un esempio di **mappingImage** e dell'immagine visibile a cui corrisponde.</span><span class="sxs-lookup"><span data-stu-id="5470a-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="5470a-120">Queste immagini fanno parte dell'interfaccia della piccola cartella inclusa nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="5470a-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![immagine di mapping di esempio](images/absam01m.png)![immagine di sfondo di esempio](images/absam01f.png)

<span data-ttu-id="5470a-123">Vedere *ButtonElement*. attributo [mappingColor](buttonelement-mappingcolor.md) per un esempio di codice che illustra l'uso di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="5470a-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="5470a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5470a-124">Requirements</span></span>



| <span data-ttu-id="5470a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5470a-125">Requirement</span></span> | <span data-ttu-id="5470a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5470a-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5470a-127">Versione</span><span class="sxs-lookup"><span data-stu-id="5470a-127">Version</span></span><br/> | <span data-ttu-id="5470a-128">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="5470a-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5470a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5470a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5470a-130">**BUTTONelement. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="5470a-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="5470a-131">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="5470a-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="5470a-132">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="5470a-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="5470a-133">**BUTTONGROUP. transparencyColor**</span><span class="sxs-lookup"><span data-stu-id="5470a-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





