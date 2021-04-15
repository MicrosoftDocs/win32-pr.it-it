---
description: 'Nella figura seguente sono illustrate due curve: una aperta e una chiusa.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curve aperte e chiuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569596"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="da1e1-103">Curve aperte e chiuse</span><span class="sxs-lookup"><span data-stu-id="da1e1-103">Open and Closed Curves</span></span>

<span data-ttu-id="da1e1-104">Nella figura seguente sono illustrate due curve: una aperta e una chiusa.</span><span class="sxs-lookup"><span data-stu-id="da1e1-104">The following illustration shows two curves: one open and one closed.</span></span>

![illustrazione di una curva aperta (linea curva) e una curva chiusa (il contorno di una forma)](images/aboutgdip02-art24.png)

<span data-ttu-id="da1e1-106">Le curve chiuse hanno una parte interna e pertanto possono essere riempite con un pennello.</span><span class="sxs-lookup"><span data-stu-id="da1e1-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="da1e1-107">La [**classe grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in Windows GDI+ fornisce i metodi seguenti per compilare le curve e le cifre chiuse: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)e [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span><span class="sxs-lookup"><span data-stu-id="da1e1-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="da1e1-108">Ogni volta che si chiama uno di questi metodi, è necessario passare l'indirizzo di uno dei tipi di pennello specifici ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)o [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) come argomento.</span><span class="sxs-lookup"><span data-stu-id="da1e1-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="da1e1-109">Il metodo [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) è un complemento al metodo [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) .</span><span class="sxs-lookup"><span data-stu-id="da1e1-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="da1e1-110">Proprio come il metodo DrawArc disegna una parte del contorno di un'ellisse, il metodo FillPie riempie una parte dell'area interna di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="da1e1-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="da1e1-111">Nell'esempio seguente viene disegnato un arco e viene riempita la parte corrispondente dell'interno dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="da1e1-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="da1e1-112">Nella figura seguente vengono illustrati l'arco e la torta piena.</span><span class="sxs-lookup"><span data-stu-id="da1e1-112">The following illustration shows the arc and the filled pie.</span></span>

![illustrazione che mostra un segmento di un'ellisse piena](images/aboutgdip02-art25.png)

<span data-ttu-id="da1e1-114">Il metodo [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) è un complemento al metodo [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="da1e1-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="da1e1-115">Entrambi i metodi chiudono automaticamente la curva connettendo il punto finale al punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="da1e1-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="da1e1-116">Nell'esempio seguente viene disegnata una curva che passa attraverso (0, 0), (60, 20) e (40, 50).</span><span class="sxs-lookup"><span data-stu-id="da1e1-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="da1e1-117">La curva viene quindi chiusa automaticamente connettendosi (40, 50) al punto iniziale (0, 0) e l'interno viene riempito con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="da1e1-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="da1e1-118">Un percorso può essere costituito da più figure (sottopercorsi).</span><span class="sxs-lookup"><span data-stu-id="da1e1-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="da1e1-119">Il metodo [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempie l'area interna di ogni figura.</span><span class="sxs-lookup"><span data-stu-id="da1e1-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="da1e1-120">Se una figura non è chiusa, il metodo **Graphics:: FillPath** riempie l'area che verrebbe racchiusa se la figura venisse chiusa.</span><span class="sxs-lookup"><span data-stu-id="da1e1-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="da1e1-121">Nell'esempio seguente viene disegnato e compilato un percorso costituito da un arco, una spline di cardinalità, una stringa e una torta.</span><span class="sxs-lookup"><span data-stu-id="da1e1-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="da1e1-122">Nella figura seguente viene mostrato il percorso prima e dopo che è stato riempito con un pennello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="da1e1-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="da1e1-123">Si noti che il testo nella stringa è delineato, ma non riempito, dal metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) .</span><span class="sxs-lookup"><span data-stu-id="da1e1-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="da1e1-124">Si tratta del metodo [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) che dipinge gli interni dei caratteri nella stringa.</span><span class="sxs-lookup"><span data-stu-id="da1e1-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![illustrazione che mostra due volte il testo e una curva aperta e chiusa; Questi sono vuoti la prima volta e riempiti la seconda volta](images/aboutgdip02-art26.png)

 

 



