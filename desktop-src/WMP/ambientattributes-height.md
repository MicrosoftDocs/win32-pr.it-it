---
title: AmbientAttributes. Height
description: L'attributo Height specifica o recupera l'altezza del controllo.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Media Player Windows AmbientAttributes. Height
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331405"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="0e765-104">AmbientAttributes. Height</span><span class="sxs-lookup"><span data-stu-id="0e765-104">AmbientAttributes.height</span></span>

<span data-ttu-id="0e765-105">L'attributo **Height** specifica o recupera l'altezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="0e765-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="0e765-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0e765-106">Possible Values</span></span>

<span data-ttu-id="0e765-107">Questo attributo è un **numero** di lettura/scrittura (**Long**) che rappresenta l'altezza del controllo in pixel.</span><span class="sxs-lookup"><span data-stu-id="0e765-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="0e765-108">Il valore predefinito è zero o l'altezza dell'immagine specificata nell'attributo **Image** del controllo.</span><span class="sxs-lookup"><span data-stu-id="0e765-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e765-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e765-109">Remarks</span></span>

<span data-ttu-id="0e765-110">Se l'altezza specificata è inferiore all'altezza dell'immagine specificata, l'immagine verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="0e765-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="0e765-111">Se l'altezza è maggiore dell'altezza dell'immagine, l'area di clic andrà oltre il limite dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0e765-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="0e765-112">Indipendentemente dal valore assegnato a questo attributo, l'immagine non può superare la **visualizzazione** padre o la relativa **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="0e765-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e765-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e765-113">Requirements</span></span>



| <span data-ttu-id="0e765-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e765-114">Requirement</span></span> | <span data-ttu-id="0e765-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e765-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0e765-116">Versione</span><span class="sxs-lookup"><span data-stu-id="0e765-116">Version</span></span><br/> | <span data-ttu-id="0e765-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="0e765-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e765-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e765-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e765-119">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="0e765-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





