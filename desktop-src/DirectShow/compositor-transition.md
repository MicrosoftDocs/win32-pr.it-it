---
description: Transizione del Compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transizione del Compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551979"
---
# <a name="compositor-transition"></a><span data-ttu-id="404ed-103">Transizione del Compositor</span><span class="sxs-lookup"><span data-stu-id="404ed-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="404ed-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="404ed-104">\[Deprecated.</span></span> <span data-ttu-id="404ed-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="404ed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="404ed-106">La transizione del Compositor compone un sottorettangolo dal primo piano in un rettangolo designato in background, senza alterare il resto dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="404ed-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="404ed-107">Usare questa transizione per creare effetti a schermata doppia o immagine in immagine.</span><span class="sxs-lookup"><span data-stu-id="404ed-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="404ed-108">Nell'immagine seguente viene illustrata la transizione del Compositor:</span><span class="sxs-lookup"><span data-stu-id="404ed-108">The following image shows the compositor transition:</span></span>

![transizione del Compositor](images/trans-compositor.png)

<span data-ttu-id="404ed-110">ID classe (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="404ed-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="404ed-111">Nome variabile CLSID: CLSID \_ DxtCompositor</span><span class="sxs-lookup"><span data-stu-id="404ed-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="404ed-112">Nome descrittivo: "DxtCompositor"</span><span class="sxs-lookup"><span data-stu-id="404ed-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="404ed-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="404ed-113">Properties</span></span>



| <span data-ttu-id="404ed-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="404ed-114">Property</span></span>   | <span data-ttu-id="404ed-115">Type</span><span class="sxs-lookup"><span data-stu-id="404ed-115">Type</span></span> | <span data-ttu-id="404ed-116">Predefinito</span><span class="sxs-lookup"><span data-stu-id="404ed-116">Default</span></span> | <span data-ttu-id="404ed-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="404ed-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="404ed-118">Altezza</span><span class="sxs-lookup"><span data-stu-id="404ed-118">Height</span></span>     | <span data-ttu-id="404ed-119">long</span><span class="sxs-lookup"><span data-stu-id="404ed-119">long</span></span> | <span data-ttu-id="404ed-120">0</span><span class="sxs-lookup"><span data-stu-id="404ed-120">0</span></span>       | <span data-ttu-id="404ed-121">Altezza, in pixel, del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="404ed-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="404ed-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="404ed-122">OffsetX</span></span>    | <span data-ttu-id="404ed-123">long</span><span class="sxs-lookup"><span data-stu-id="404ed-123">long</span></span> | <span data-ttu-id="404ed-124">0</span><span class="sxs-lookup"><span data-stu-id="404ed-124">0</span></span>       | <span data-ttu-id="404ed-125">Offset orizzontale del rettangolo di destinazione, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="404ed-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="404ed-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="404ed-126">OffsetY</span></span>    | <span data-ttu-id="404ed-127">long</span><span class="sxs-lookup"><span data-stu-id="404ed-127">long</span></span> | <span data-ttu-id="404ed-128">0</span><span class="sxs-lookup"><span data-stu-id="404ed-128">0</span></span>       | <span data-ttu-id="404ed-129">Offset verticale del rettangolo di destinazione, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="404ed-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="404ed-130">SrcHeight</span><span class="sxs-lookup"><span data-stu-id="404ed-130">SrcHeight</span></span>  | <span data-ttu-id="404ed-131">long</span><span class="sxs-lookup"><span data-stu-id="404ed-131">long</span></span> | <span data-ttu-id="404ed-132">0</span><span class="sxs-lookup"><span data-stu-id="404ed-132">0</span></span>       | <span data-ttu-id="404ed-133">Altezza del sottorettangolo sull'origine, in pixel.</span><span class="sxs-lookup"><span data-stu-id="404ed-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="404ed-134">SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="404ed-134">SrcOffsetX</span></span> | <span data-ttu-id="404ed-135">long</span><span class="sxs-lookup"><span data-stu-id="404ed-135">long</span></span> | <span data-ttu-id="404ed-136">0</span><span class="sxs-lookup"><span data-stu-id="404ed-136">0</span></span>       | <span data-ttu-id="404ed-137">Coordinata x del sottorettangolo sull'origine, espressa in pixel.</span><span class="sxs-lookup"><span data-stu-id="404ed-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="404ed-138">SrcOffsetY</span><span class="sxs-lookup"><span data-stu-id="404ed-138">SrcOffsetY</span></span> | <span data-ttu-id="404ed-139">long</span><span class="sxs-lookup"><span data-stu-id="404ed-139">long</span></span> | <span data-ttu-id="404ed-140">0</span><span class="sxs-lookup"><span data-stu-id="404ed-140">0</span></span>       | <span data-ttu-id="404ed-141">Coordinata y del sottorettangolo sull'origine, espressa in pixel.</span><span class="sxs-lookup"><span data-stu-id="404ed-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="404ed-142">SrcWidth</span><span class="sxs-lookup"><span data-stu-id="404ed-142">SrcWidth</span></span>   | <span data-ttu-id="404ed-143">long</span><span class="sxs-lookup"><span data-stu-id="404ed-143">long</span></span> | <span data-ttu-id="404ed-144">0</span><span class="sxs-lookup"><span data-stu-id="404ed-144">0</span></span>       | <span data-ttu-id="404ed-145">Larghezza del sottorettangolo sull'origine, in pixel.</span><span class="sxs-lookup"><span data-stu-id="404ed-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="404ed-146">Larghezza</span><span class="sxs-lookup"><span data-stu-id="404ed-146">Width</span></span>      | <span data-ttu-id="404ed-147">long</span><span class="sxs-lookup"><span data-stu-id="404ed-147">long</span></span> | <span data-ttu-id="404ed-148">0</span><span class="sxs-lookup"><span data-stu-id="404ed-148">0</span></span>       | <span data-ttu-id="404ed-149">Larghezza, in pixel, del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="404ed-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="404ed-150">Nel diagramma seguente vengono illustrate queste proprietà:</span><span class="sxs-lookup"><span data-stu-id="404ed-150">The following diagram illustrates these properties:</span></span>

![Proprietà compositor](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="404ed-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="404ed-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="404ed-153">Transizioni ed effetti</span><span class="sxs-lookup"><span data-stu-id="404ed-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 



