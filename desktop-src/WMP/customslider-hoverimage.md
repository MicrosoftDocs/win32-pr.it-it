---
title: CUSTOMSLIDER.hoverImage
description: L'attributo hoverImage specifica o recupera l'immagine visualizzata quando il mouse è posizionato sul dispositivo di scorrimento personalizzato.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- Media Player Windows CUSTOMSLIDER. hoverImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331487"
---
# <a name="customsliderhoverimage"></a><span data-ttu-id="cf615-104">CUSTOMSLIDER.hoverImage</span><span class="sxs-lookup"><span data-stu-id="cf615-104">CUSTOMSLIDER.hoverImage</span></span>

<span data-ttu-id="cf615-105">L'attributo **hoverImage** specifica o recupera l'immagine visualizzata quando il mouse è posizionato sul dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cf615-105">The **hoverImage** attribute specifies or retrieves the image that appears when the mouse is over the custom slider.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="cf615-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="cf615-106">Possible Values</span></span>

<span data-ttu-id="cf615-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="cf615-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf615-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf615-108">Remarks</span></span>

<span data-ttu-id="cf615-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="cf615-109">This attribute is optional.</span></span> <span data-ttu-id="cf615-110">Se non è specificato, verrà usato il file specificato nell'attributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="cf615-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="cf615-111">**HoverImage** rappresenta lo stato del passaggio del mouse sul controllo CUSTOMSLIDER; ovvero lo stato visualizzato quando il cursore del mouse viene posizionato su di esso.</span><span class="sxs-lookup"><span data-stu-id="cf615-111">The **hoverImage** represents the hover state of the CUSTOMSLIDER control; that is, the state that is shown when the mouse cursor hovers over it.</span></span> <span data-ttu-id="cf615-112">Può trattarsi di una singola immagine o di una serie di immagini che rappresentano i vari Stati del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cf615-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="cf615-113">Se vengono usate più immagini, vengono disposte nello stesso modo del file di **immagine**</span><span class="sxs-lookup"><span data-stu-id="cf615-113">If multiple images are used, they are arranged in the same way as the **image** file</span></span>

<span data-ttu-id="cf615-114">I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="cf615-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf615-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf615-115">Requirements</span></span>



| <span data-ttu-id="cf615-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf615-116">Requirement</span></span> | <span data-ttu-id="cf615-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cf615-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cf615-118">Versione</span><span class="sxs-lookup"><span data-stu-id="cf615-118">Version</span></span><br/> | <span data-ttu-id="cf615-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="cf615-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf615-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf615-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf615-121">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="cf615-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="cf615-122">**CUSTOMSLIDER. image**</span><span class="sxs-lookup"><span data-stu-id="cf615-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





