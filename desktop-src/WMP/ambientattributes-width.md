---
title: AmbientAttributes. Width
description: L'attributo Width specifica o recupera la larghezza del controllo.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Media Player Windows AmbientAttributes. Width
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325591"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="41f93-104">AmbientAttributes. Width</span><span class="sxs-lookup"><span data-stu-id="41f93-104">AmbientAttributes.width</span></span>

<span data-ttu-id="41f93-105">L'attributo **Width** specifica o recupera la larghezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="41f93-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="41f93-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="41f93-106">Possible Values</span></span>

<span data-ttu-id="41f93-107">Questo attributo è un **Integer** a 16 bit in lettura/scrittura (da 0 a 32.767) che rappresenta la larghezza del controllo in pixel.</span><span class="sxs-lookup"><span data-stu-id="41f93-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="41f93-108">Il valore predefinito è zero o la larghezza dell'immagine specificata nell'attributo **Image** del controllo.</span><span class="sxs-lookup"><span data-stu-id="41f93-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f93-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="41f93-109">Remarks</span></span>

<span data-ttu-id="41f93-110">Se la larghezza specificata è più stretta rispetto alla larghezza dell'immagine fornita, l'immagine verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="41f93-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="41f93-111">Se la larghezza è maggiore della larghezza dell'immagine, l'area di clic andrà oltre il limite dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="41f93-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="41f93-112">Indipendentemente dal valore assegnato a questo attributo, l'immagine non può superare la **visualizzazione** padre o la relativa **visualizzazione**.</span><span class="sxs-lookup"><span data-stu-id="41f93-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f93-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41f93-113">Requirements</span></span>



| <span data-ttu-id="41f93-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f93-114">Requirement</span></span> | <span data-ttu-id="41f93-115">Valore</span><span class="sxs-lookup"><span data-stu-id="41f93-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="41f93-116">Versione</span><span class="sxs-lookup"><span data-stu-id="41f93-116">Version</span></span><br/> | <span data-ttu-id="41f93-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="41f93-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41f93-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41f93-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f93-119">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="41f93-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





