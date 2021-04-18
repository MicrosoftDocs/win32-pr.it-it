---
title: CUSTOMSLIDER.downImage
description: L'attributo downImage specifica o recupera l'immagine di stato inattivo del dispositivo di scorrimento personalizzato.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- Media Player Windows CUSTOMSLIDER. downImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331755"
---
# <a name="customsliderdownimage"></a><span data-ttu-id="d5917-104">CUSTOMSLIDER.downImage</span><span class="sxs-lookup"><span data-stu-id="d5917-104">CUSTOMSLIDER.downImage</span></span>

<span data-ttu-id="d5917-105">L'attributo **downImage** specifica o recupera l'immagine di stato inattivo del dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d5917-105">The **downImage** attribute specifies or retrieves the down state image of the custom slider.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="d5917-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d5917-106">Possible Values</span></span>

<span data-ttu-id="d5917-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="d5917-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5917-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5917-108">Remarks</span></span>

<span data-ttu-id="d5917-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d5917-109">This attribute is optional.</span></span> <span data-ttu-id="d5917-110">Se non è specificato, verrà usato il file specificato nell'attributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="d5917-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="d5917-111">**DownImage** rappresenta lo stato di inattività del controllo **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="d5917-111">The **downImage** represents the down state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="d5917-112">Può trattarsi di una singola immagine o di una serie di immagini che rappresentano i vari Stati del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d5917-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="d5917-113">Se vengono usate più immagini, vengono disposte nello stesso modo del file di **immagine** .</span><span class="sxs-lookup"><span data-stu-id="d5917-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="d5917-114">I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="d5917-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5917-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5917-115">Requirements</span></span>



| <span data-ttu-id="d5917-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5917-116">Requirement</span></span> | <span data-ttu-id="d5917-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d5917-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d5917-118">Versione</span><span class="sxs-lookup"><span data-stu-id="d5917-118">Version</span></span><br/> | <span data-ttu-id="d5917-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d5917-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5917-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5917-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5917-121">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="d5917-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="d5917-122">**CUSTOMSLIDER. image**</span><span class="sxs-lookup"><span data-stu-id="d5917-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





