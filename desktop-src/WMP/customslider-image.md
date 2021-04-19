---
title: CUSTOMSLIDER. image
description: L'attributo Image specifica o Recupera il nome del file contenente le immagini corrispondenti ai vari Stati del dispositivo di scorrimento personalizzato.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Media Player Windows CUSTOMSLIDER. image
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323910"
---
# <a name="customsliderimage"></a><span data-ttu-id="9ae32-104">CUSTOMSLIDER. image</span><span class="sxs-lookup"><span data-stu-id="9ae32-104">CUSTOMSLIDER.image</span></span>

<span data-ttu-id="9ae32-105">L'attributo **Image** specifica o Recupera il nome del file contenente le immagini corrispondenti ai vari Stati del dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9ae32-105">The **image** attribute specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="9ae32-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9ae32-106">Possible Values</span></span>

<span data-ttu-id="9ae32-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="9ae32-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ae32-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ae32-108">Remarks</span></span>

<span data-ttu-id="9ae32-109">L'attributo **Image** è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ae32-109">The **image** attribute is required.</span></span> <span data-ttu-id="9ae32-110">Specifica un file di immagine costituito da una o più immagini secondarie, disposte orizzontalmente o verticalmente, che rappresentano i vari Stati del dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9ae32-110">It specifies an image file that consists of one or more sub-images, arranged either horizontally or vertically, representing the various states of the custom slider.</span></span> <span data-ttu-id="9ae32-111">Ogni immagine secondaria deve avere le stesse dimensioni di **dimensione positionImage** o il dispositivo di scorrimento personalizzato non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="9ae32-111">Each sub-image must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span> <span data-ttu-id="9ae32-112">L'altezza o la larghezza dell'immagine complessiva deve quindi essere un multiplo pari dell'altezza o della larghezza del **dimensione positionImage**.</span><span class="sxs-lookup"><span data-stu-id="9ae32-112">The height or width of the overall image must therefore be an even multiple of the height or width of the **positionImage**.</span></span>

<span data-ttu-id="9ae32-113">I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).</span><span class="sxs-lookup"><span data-stu-id="9ae32-113">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="9ae32-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="9ae32-114">Examples</span></span>

<span data-ttu-id="9ae32-115">Di seguito è riportato un esempio di un'immagine del dispositivo di scorrimento personalizzata.</span><span class="sxs-lookup"><span data-stu-id="9ae32-115">The following is an example of a custom slider image.</span></span> <span data-ttu-id="9ae32-116">Il **dimensione positionImage** corrispondente viene visualizzato nella sezione esempio della proprietà **dimensione positionImage** .</span><span class="sxs-lookup"><span data-stu-id="9ae32-116">The corresponding **positionImage** is shown in the example section of the **positionImage** property.</span></span>

![immagine customslider di esempio](images/dial.png)

<span data-ttu-id="9ae32-118">L'attributo **dimensione positionImage** contiene anche un esempio di codice che illustra come vengono usati gli attributi dell'elemento **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="9ae32-118">The **positionImage** attribute also contains a code sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae32-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ae32-119">Requirements</span></span>



| <span data-ttu-id="9ae32-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae32-120">Requirement</span></span> | <span data-ttu-id="9ae32-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9ae32-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9ae32-122">Versione</span><span class="sxs-lookup"><span data-stu-id="9ae32-122">Version</span></span><br/> | <span data-ttu-id="9ae32-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="9ae32-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ae32-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ae32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae32-125">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="9ae32-125">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="9ae32-126">**CUSTOMSLIDER. dimensione positionImage**</span><span class="sxs-lookup"><span data-stu-id="9ae32-126">**CUSTOMSLIDER.positionImage**</span></span>](customslider-positionimage.md)
</dt> </dl>

 

 





