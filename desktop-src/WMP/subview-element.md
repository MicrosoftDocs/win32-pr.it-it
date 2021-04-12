---
title: Elemento subview
description: Elemento subview
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player Skin, elemento subview
- Skin, elemento subview
- Elemento subview
- riferimento per Skin, elemento subview
- elementi, visualizzazione subview
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331860"
---
# <a name="subview-element"></a><span data-ttu-id="76f26-108">Elemento subview</span><span class="sxs-lookup"><span data-stu-id="76f26-108">SUBVIEW Element</span></span>

<span data-ttu-id="76f26-109">L'elemento **subview** fornisce un modo per modificare una parte di un'interfaccia, ad esempio per fornire un pannello di controllo che può essere nascosto quando non è in uso.</span><span class="sxs-lookup"><span data-stu-id="76f26-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="76f26-110">Gli elementi della **visualizzazione subview** sono sempre elementi figlio degli elementi di **visualizzazione** padre e possono contenere altro elemento Skin ad eccezione di **visualizzazione**, **tema** e altri elementi di **Sottovisualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="76f26-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="76f26-111">L'elemento **subview** supporta gli attributi seguenti, definiti nell'elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="76f26-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="76f26-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="76f26-112">Attribute</span></span>                                                       | <span data-ttu-id="76f26-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76f26-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76f26-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="76f26-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="76f26-115">Specifica o Recupera il colore di sfondo del controllo di **Sottovisualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="76f26-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="76f26-116">Il valore predefinito è "None".</span><span class="sxs-lookup"><span data-stu-id="76f26-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="76f26-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="76f26-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="76f26-118">Specifica o recupera l'immagine di sfondo del controllo **Sottovisualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="76f26-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="76f26-119">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="76f26-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="76f26-120">Specifica o recupera la quantità in base alla quale viene spostata la tonalità dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="76f26-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="76f26-121">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="76f26-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="76f26-122">Specifica o Recupera il valore di saturazione dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="76f26-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="76f26-123">backgroundTiled</span><span class="sxs-lookup"><span data-stu-id="76f26-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="76f26-124">Specifica o recupera un valore che indica se l'immagine di sfondo del controllo **Sottovisualizzazione** è affiancata.</span><span class="sxs-lookup"><span data-stu-id="76f26-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="76f26-125">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="76f26-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="76f26-126">Specifica o recupera un valore che indica se è possibile ridimensionare l'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="76f26-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="76f26-127">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="76f26-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="76f26-128">Specifica o Recupera il colore di trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="76f26-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="76f26-129">L'elemento **subview** supporta gli attributi di ambiente, eccetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="76f26-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="76f26-130">Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="76f26-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="76f26-131">L'elemento **subview** può implementare i gestori eventi di ambiente seguenti: [onendmove](onendmove.md) e [OnResize](onresize.md).</span><span class="sxs-lookup"><span data-stu-id="76f26-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76f26-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76f26-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f26-133">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="76f26-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="76f26-134">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="76f26-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 




