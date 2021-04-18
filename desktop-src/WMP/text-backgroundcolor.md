---
title: TESTO. backgroundColor
description: L'attributo backgroundColor specifica o Recupera il colore di sfondo per il controllo di testo.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- Media Player di Windows TEXT. backgroundColor
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325572"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="306cc-104">TESTO. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="306cc-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="306cc-105">L'attributo **BackgroundColor** specifica o Recupera il colore di sfondo per il controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="306cc-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="306cc-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="306cc-106">Possible Values</span></span>

<span data-ttu-id="306cc-107">Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer oppure il valore "None".</span><span class="sxs-lookup"><span data-stu-id="306cc-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="306cc-108">Il valore predefinito è "None", che indica che lo sfondo è trasparente.</span><span class="sxs-lookup"><span data-stu-id="306cc-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="306cc-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="306cc-109">Remarks</span></span>

<span data-ttu-id="306cc-110">Il colore di sfondo è impostato per l'altezza e la larghezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="306cc-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="306cc-111">Se l'altezza e la larghezza non sono impostate, il colore di sfondo viene impostato sull'altezza e sulla larghezza del testo.</span><span class="sxs-lookup"><span data-stu-id="306cc-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="306cc-112">Quando si usa **alphaBlend** o **alphaBlendTo** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero.</span><span class="sxs-lookup"><span data-stu-id="306cc-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="306cc-113">Se anche il colore di primo piano è nero (ovvero il valore predefinito per l'attributo **ForegroundColor** ), il testo potrebbe diventare illeggibile.</span><span class="sxs-lookup"><span data-stu-id="306cc-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="306cc-114">Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.</span><span class="sxs-lookup"><span data-stu-id="306cc-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="306cc-115">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="306cc-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="306cc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="306cc-116">Requirements</span></span>



| <span data-ttu-id="306cc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="306cc-117">Requirement</span></span> | <span data-ttu-id="306cc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="306cc-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="306cc-119">Versione</span><span class="sxs-lookup"><span data-stu-id="306cc-119">Version</span></span><br/> | <span data-ttu-id="306cc-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="306cc-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="306cc-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="306cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306cc-122">**AmbientAttributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="306cc-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="306cc-123">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="306cc-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="306cc-124">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="306cc-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="306cc-125">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="306cc-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="306cc-126">**TESTO. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="306cc-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





