---
description: "È possibile riempire un percorso passando l'indirizzo di un oggetto GraphicsPath al metodo Graphics:: FillPath."
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Riempimento di figure aperte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551869"
---
# <a name="filling-open-figures"></a><span data-ttu-id="31648-103">Riempimento di figure aperte</span><span class="sxs-lookup"><span data-stu-id="31648-103">Filling Open Figures</span></span>

<span data-ttu-id="31648-104">È possibile riempire un percorso passando l'indirizzo di un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) al metodo [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) .</span><span class="sxs-lookup"><span data-stu-id="31648-104">You can fill a path by passing the address of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object to the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method.</span></span> <span data-ttu-id="31648-105">Il metodo **Graphics:: FillPath** riempie il percorso in base alla modalità di riempimento (alternativa o di avvolgimento) attualmente impostata per il percorso.</span><span class="sxs-lookup"><span data-stu-id="31648-105">The **Graphics::FillPath** method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="31648-106">Se il percorso contiene figure aperte, il percorso viene riempito come se tali figure fossero chiuse.</span><span class="sxs-lookup"><span data-stu-id="31648-106">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="31648-107">GDI+ chiude una figura disegnando una linea retta dal punto finale al punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="31648-107">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>

<span data-ttu-id="31648-108">Nell'esempio seguente viene creato un percorso con una figura aperta (un arco) e una figura chiusa (un'ellisse).</span><span class="sxs-lookup"><span data-stu-id="31648-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="31648-109">Il metodo [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempie il percorso in base alla modalità di riempimento predefinita, ovvero FillModeAlternate.</span><span class="sxs-lookup"><span data-stu-id="31648-109">The [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the path according to the default fill mode, which is FillModeAlternate.</span></span>


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="31648-110">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="31648-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="31648-111">Si noti che il percorso è riempito (in base a FillModeAlternate) come se la figura aperta fosse chiusa da una linea retta dal punto finale al punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="31648-111">Note that path is filled (according to FillModeAlternate) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>

![illustrazione che mostra un'ellisse alta che si sovrappone alla metà inferiore di un'ellisse ampia. l'Unione è compilata, ma l'intersezione è vuota](images/fillopenpath.png)

 

 



