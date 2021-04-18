---
title: Colore RGB raggiunto
description: Colore RGB raggiunto
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Windows Media Player Mobile Skins, colori pulsante
- interfacce, colori pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, colori
- riferimento ai colori per le interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298653"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="a0908-108">Colore RGB raggiunto</span><span class="sxs-lookup"><span data-stu-id="a0908-108">Hit RGB Color</span></span>

<span data-ttu-id="a0908-109">Se si usano i pulsanti Region (PushHit, ToggleHit e 2PushHit), è necessario definire il colore che verrà usato da Windows Media Player per determinare l'area di hit del pulsante.</span><span class="sxs-lookup"><span data-stu-id="a0908-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="a0908-110">Questo valore deve essere specificato utilizzando tre numeri interi positivi separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="a0908-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="a0908-111">Questi numeri interi rappresentano la quantità di rosso, verde e blu per un colore bitmap e variano da 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="a0908-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="a0908-112">I tipi di pulsanti sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a0908-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="a0908-113">È possibile usare qualsiasi colore per i valori, ma assicurarsi che ogni pulsante dell'area definito abbia un colore univoco nel file di immagine dell'area e che il valore del colore definito qui come numero corrisponda al colore effettivo usato nell'immagine dell'area.</span><span class="sxs-lookup"><span data-stu-id="a0908-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="a0908-114">La tabella seguente illustra alcuni colori tipici che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="a0908-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="a0908-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a0908-115">Value</span></span>       | <span data-ttu-id="a0908-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0908-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="a0908-117">0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="a0908-117">0,0,0</span></span>       | <span data-ttu-id="a0908-118">Nero</span><span class="sxs-lookup"><span data-stu-id="a0908-118">Black</span></span>       |
| <span data-ttu-id="a0908-119">255.255.255</span><span class="sxs-lookup"><span data-stu-id="a0908-119">255,255,255</span></span> | <span data-ttu-id="a0908-120">White</span><span class="sxs-lookup"><span data-stu-id="a0908-120">White</span></span>       |
| <span data-ttu-id="a0908-121">255, 0, 0</span><span class="sxs-lookup"><span data-stu-id="a0908-121">255,0,0</span></span>     | <span data-ttu-id="a0908-122">Red</span><span class="sxs-lookup"><span data-stu-id="a0908-122">Red</span></span>         |
| <span data-ttu-id="a0908-123">0255, 0</span><span class="sxs-lookup"><span data-stu-id="a0908-123">0,255,0</span></span>     | <span data-ttu-id="a0908-124">Green</span><span class="sxs-lookup"><span data-stu-id="a0908-124">Green</span></span>       |
| <span data-ttu-id="a0908-125">0, 0255</span><span class="sxs-lookup"><span data-stu-id="a0908-125">0,0,255</span></span>     | <span data-ttu-id="a0908-126">Blu</span><span class="sxs-lookup"><span data-stu-id="a0908-126">Blue</span></span>        |



 

<span data-ttu-id="a0908-127">Se non si usano i pulsanti Region, è necessario immettere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a0908-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="a0908-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0908-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0908-129">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="a0908-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




