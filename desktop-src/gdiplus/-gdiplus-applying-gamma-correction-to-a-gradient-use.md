---
description: 'È possibile abilitare la correzione gamma per un pennello sfumatura passando TRUE al Metodo PathGradientBrush:: SetGammaCorrection del pennello.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Applicazione della correzione gamma a una sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131387"
---
# <a name="applying-gamma-correction-to-a-gradient"></a><span data-ttu-id="38cf3-103">Applicazione della correzione gamma a una sfumatura</span><span class="sxs-lookup"><span data-stu-id="38cf3-103">Applying Gamma Correction to a Gradient</span></span>

<span data-ttu-id="38cf3-104">È possibile abilitare la correzione gamma per un pennello sfumatura passando **true** al metodo [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) del pennello.</span><span class="sxs-lookup"><span data-stu-id="38cf3-104">You can enable gamma correction for a gradient brush by passing **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method of that brush.</span></span> <span data-ttu-id="38cf3-105">È possibile disabilitare la correzione gamma passando **false** al metodo **PathGradientBrush:: SetGammaCorrection** .</span><span class="sxs-lookup"><span data-stu-id="38cf3-105">You can disable gamma correction by passing **FALSE** to the **PathGradientBrush::SetGammaCorrection** method.</span></span> <span data-ttu-id="38cf3-106">Per impostazione predefinita, la correzione gamma è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="38cf3-106">Gamma correction is disabled by default.</span></span>

<span data-ttu-id="38cf3-107">Nell'esempio seguente viene creato un pennello sfumato lineare e tale pennello viene utilizzato per riempire due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="38cf3-107">The following example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="38cf3-108">Il primo rettangolo viene riempito senza correzione gamma e il secondo rettangolo viene riempito con la correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="38cf3-108">The first rectangle is filled without gamma correction and the second rectangle is filled with gamma correction.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



<span data-ttu-id="38cf3-109">Nella figura seguente sono illustrati i due rettangoli riempiti.</span><span class="sxs-lookup"><span data-stu-id="38cf3-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="38cf3-110">Il rettangolo superiore, che non ha la correzione gamma, appare scuro al centro.</span><span class="sxs-lookup"><span data-stu-id="38cf3-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="38cf3-111">Il rettangolo inferiore, con correzione gamma, sembra avere un'intensità più uniforme.</span><span class="sxs-lookup"><span data-stu-id="38cf3-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>

![illustrazione che mostra due rettangoli: il riempimento colorato del primo varia in intensità, il riempimento del secondo varia in meno](images/gammagradient1.png)

<span data-ttu-id="38cf3-113">Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un percorso a forma di stella.</span><span class="sxs-lookup"><span data-stu-id="38cf3-113">The following example creates a path gradient brush based on a star-shaped path.</span></span> <span data-ttu-id="38cf3-114">Il codice usa il pennello sfumatura del percorso con la correzione gamma disabilitata (impostazione predefinita) per riempire il percorso.</span><span class="sxs-lookup"><span data-stu-id="38cf3-114">The code uses the path gradient brush with gamma correction disabled (the default) to fill the path.</span></span> <span data-ttu-id="38cf3-115">Quindi il codice passa **true** al metodo [**PathGradientBrush:: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) per abilitare la correzione gamma per il pennello sfumatura del percorso.</span><span class="sxs-lookup"><span data-stu-id="38cf3-115">Then the code passes **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method to enable gamma correction for the path gradient brush.</span></span> <span data-ttu-id="38cf3-116">La chiamata a [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) imposta la trasformazione globale di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in modo che la chiamata successiva a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempia una stella che si trova a destra della prima stella.</span><span class="sxs-lookup"><span data-stu-id="38cf3-116">The call to [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) sets the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills a star that sits to the right of the first star.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="38cf3-117">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="38cf3-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="38cf3-118">La stella a destra ha la correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="38cf3-118">The star on the right has gamma correction.</span></span> <span data-ttu-id="38cf3-119">Si noti che la stella a sinistra, che non ha la correzione gamma, presenta aree che appaiono scure.</span><span class="sxs-lookup"><span data-stu-id="38cf3-119">Note that the star on the left, which does not have gamma correction, has areas that appear dark.</span></span>

![illustrazione di 2 5-puntato inizia con riempimento sfumato colorato; il primo ha aree scure, il secondo non](images/gammagradient2.png)

 

 



