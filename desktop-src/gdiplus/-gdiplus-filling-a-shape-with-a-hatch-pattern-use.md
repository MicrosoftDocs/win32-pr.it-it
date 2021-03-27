---
description: 'Un modello di tratteggio è costituito da due colori: uno per lo sfondo e uno per le linee che formano il modello sullo sfondo.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Riempimento di una forma con un motivo di tratteggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987769"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="29d1b-103">Riempimento di una forma con un motivo di tratteggio</span><span class="sxs-lookup"><span data-stu-id="29d1b-103">Filling a Shape with a Hatch Pattern</span></span>

<span data-ttu-id="29d1b-104">Un modello di tratteggio è costituito da due colori: uno per lo sfondo e uno per le linee che formano il modello sullo sfondo.</span><span class="sxs-lookup"><span data-stu-id="29d1b-104">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="29d1b-105">Per riempire una forma chiusa con un motivo di tratteggio, usare un oggetto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .</span><span class="sxs-lookup"><span data-stu-id="29d1b-105">To fill a closed shape with a hatch pattern, use a [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) object.</span></span> <span data-ttu-id="29d1b-106">Nell'esempio seguente viene illustrato come riempire un'ellisse con un motivo di tratteggio:</span><span class="sxs-lookup"><span data-stu-id="29d1b-106">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



<span data-ttu-id="29d1b-107">Nell'illustrazione seguente viene mostrata l'ellisse piena.</span><span class="sxs-lookup"><span data-stu-id="29d1b-107">The following illustration shows the filled ellipse.</span></span>

![illustrazione di un'ellisse riempita con lo schema tratteggiato delle linee orizzontali su uno sfondo a tinta unita](images/hatch1.png)

<span data-ttu-id="29d1b-109">Il costruttore [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) accetta tre argomenti: lo stile di tratteggio, il colore della linea di tratteggio e il colore dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="29d1b-109">The [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="29d1b-110">L'argomento dello stile di tratteggio può essere qualsiasi elemento dell'enumerazione [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) .</span><span class="sxs-lookup"><span data-stu-id="29d1b-110">The hatch style argument can be any element of the [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) enumeration.</span></span> <span data-ttu-id="29d1b-111">Sono presenti più di 50 elementi nell'enumerazione **HatchStyle** . alcuni di questi elementi sono illustrati nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="29d1b-111">There are more than fifty elements in the **HatchStyle** enumeration; a few of those elements are shown in the following list:</span></span>

-   <span data-ttu-id="29d1b-112">**HatchStyleHorizontal**</span><span class="sxs-lookup"><span data-stu-id="29d1b-112">**HatchStyleHorizontal**</span></span>
-   <span data-ttu-id="29d1b-113">**HatchStyleVertical**</span><span class="sxs-lookup"><span data-stu-id="29d1b-113">**HatchStyleVertical**</span></span>
-   <span data-ttu-id="29d1b-114">**HatchStyleForwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="29d1b-114">**HatchStyleForwardDiagonal**</span></span>
-   <span data-ttu-id="29d1b-115">**HatchStyleBackwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="29d1b-115">**HatchStyleBackwardDiagonal**</span></span>
-   <span data-ttu-id="29d1b-116">**HatchStyleCross**</span><span class="sxs-lookup"><span data-stu-id="29d1b-116">**HatchStyleCross**</span></span>
-   <span data-ttu-id="29d1b-117">**HatchStyleDiagonalCross**</span><span class="sxs-lookup"><span data-stu-id="29d1b-117">**HatchStyleDiagonalCross**</span></span>

 

 



