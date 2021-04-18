---
description: Un percorso è una sequenza di primitive grafiche (linee, rettangoli, curve, testo e simili) che possono essere modificate e disegnate come una singola unità. Un percorso può essere suddiviso in figure aperte o chiuse. Una figura può contenere diverse primitive.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Costruzione e creazione di percorsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994304"
---
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="1cf06-105">Costruzione e creazione di percorsi</span><span class="sxs-lookup"><span data-stu-id="1cf06-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="1cf06-106">Un percorso è una sequenza di primitive grafiche (linee, rettangoli, curve, testo e simili) che possono essere modificate e disegnate come una singola unità.</span><span class="sxs-lookup"><span data-stu-id="1cf06-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="1cf06-107">Un percorso può essere suddiviso in *figure* aperte o chiuse.</span><span class="sxs-lookup"><span data-stu-id="1cf06-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="1cf06-108">Una figura può contenere diverse primitive.</span><span class="sxs-lookup"><span data-stu-id="1cf06-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="1cf06-109">È possibile creare un tracciato chiamando il metodo [**Graphics::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ed è possibile riempire un percorso chiamando il metodo [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) della classe **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="1cf06-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="1cf06-110">Gli argomenti seguenti riguardano i percorsi in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="1cf06-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="1cf06-111">Creazione di figure da linee, curve e forme</span><span class="sxs-lookup"><span data-stu-id="1cf06-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="1cf06-112">Riempimento di figure aperte</span><span class="sxs-lookup"><span data-stu-id="1cf06-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 



