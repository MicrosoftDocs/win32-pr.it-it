---
title: TESTO. foregroundColor
description: L'attributo foregroundColor specifica o Recupera il colore del testo per il controllo di testo.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Media Player di Windows TEXT. foregroundColor
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325826"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="839df-104">TESTO. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="839df-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="839df-105">L'attributo **ForegroundColor** specifica o Recupera il colore del testo per il controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="839df-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="839df-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="839df-106">Possible Values</span></span>

<span data-ttu-id="839df-107">Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="839df-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="839df-108">Il valore predefinito è "Black".</span><span class="sxs-lookup"><span data-stu-id="839df-108">The default value is "black".</span></span>

<span data-ttu-id="839df-109">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="839df-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="839df-110">Quando si usa **alphaBlend** o **alphaBlendTo** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero.</span><span class="sxs-lookup"><span data-stu-id="839df-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="839df-111">Se anche il colore di primo piano è nero (ovvero il valore predefinito per l'attributo **ForegroundColor** ), il testo potrebbe diventare illeggibile.</span><span class="sxs-lookup"><span data-stu-id="839df-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="839df-112">Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.</span><span class="sxs-lookup"><span data-stu-id="839df-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="839df-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="839df-113">Requirements</span></span>



| <span data-ttu-id="839df-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="839df-114">Requirement</span></span> | <span data-ttu-id="839df-115">Valore</span><span class="sxs-lookup"><span data-stu-id="839df-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="839df-116">Versione</span><span class="sxs-lookup"><span data-stu-id="839df-116">Version</span></span><br/> | <span data-ttu-id="839df-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="839df-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="839df-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="839df-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839df-119">**AmbientAttributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="839df-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="839df-120">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="839df-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="839df-121">**Riferimento ai colori**</span><span class="sxs-lookup"><span data-stu-id="839df-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="839df-122">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="839df-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="839df-123">**TESTO. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="839df-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 





