---
description: Una figura chiusa, ad esempio un rettangolo o un'ellisse, è costituita da una struttura e da una parte interna.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pennelli e forme piene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570850"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="6a515-103">Pennelli e forme piene</span><span class="sxs-lookup"><span data-stu-id="6a515-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="6a515-104">Una figura chiusa, ad esempio un rettangolo o un'ellisse, è costituita da una struttura e da una parte interna.</span><span class="sxs-lookup"><span data-stu-id="6a515-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="6a515-105">Il contorno viene disegnato con un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e l'interno viene riempito con un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="6a515-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="6a515-106">In Windows GDI+ sono disponibili diverse classi di pennelli per riempire le parti interne delle figure chiuse, ovvero [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)e [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="6a515-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="6a515-107">Tutte queste classi ereditano dalla classe **Brush** .</span><span class="sxs-lookup"><span data-stu-id="6a515-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="6a515-108">Nella figura seguente viene illustrato un rettangolo riempito con un pennello a tinta unita e un'ellisse riempita con un pennello di tratteggio.</span><span class="sxs-lookup"><span data-stu-id="6a515-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![illustrazione che mostra un rettangolo blu e un'ellisse magenta riempita con un modello di tratteggio blu](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="6a515-110">Pennelli a tinta unita</span><span class="sxs-lookup"><span data-stu-id="6a515-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="6a515-111">Pennelli tratteggiati</span><span class="sxs-lookup"><span data-stu-id="6a515-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="6a515-112">Pennelli trama</span><span class="sxs-lookup"><span data-stu-id="6a515-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="6a515-113">Pennelli sfumatura</span><span class="sxs-lookup"><span data-stu-id="6a515-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="6a515-114">Pennelli a tinta unita</span><span class="sxs-lookup"><span data-stu-id="6a515-114">Solid Brushes</span></span>

<span data-ttu-id="6a515-115">Per riempire una forma chiusa sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="6a515-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="6a515-116">L'oggetto **Graphics** fornisce metodi, ad esempio [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) e [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), e l'oggetto **Brush** archivia gli attributi del riempimento, ad esempio il colore e il motivo.</span><span class="sxs-lookup"><span data-stu-id="6a515-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="6a515-117">L'indirizzo dell'oggetto **pennello** viene passato come uno degli argomenti del metodo Fill.</span><span class="sxs-lookup"><span data-stu-id="6a515-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="6a515-118">Nell'esempio seguente viene riempita un'ellisse con un colore rosso a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="6a515-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="6a515-119">Si noti che nell'esempio precedente il pennello è di tipo [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), che eredita da [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span><span class="sxs-lookup"><span data-stu-id="6a515-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="6a515-120">Pennelli tratteggiati</span><span class="sxs-lookup"><span data-stu-id="6a515-120">Hatch Brushes</span></span>

<span data-ttu-id="6a515-121">Quando si riempie una forma con un pennello tratteggiato, è necessario specificare un colore di primo piano, un colore di sfondo e uno stile di tratteggio.</span><span class="sxs-lookup"><span data-stu-id="6a515-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="6a515-122">Il colore di primo piano è il colore del tratteggio.</span><span class="sxs-lookup"><span data-stu-id="6a515-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="6a515-123">GDI+ fornisce più di 50 stili di tratteggio, specificati in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span><span class="sxs-lookup"><span data-stu-id="6a515-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="6a515-124">I tre stili illustrati nella figura seguente sono Horizontal, ForwardDiagonal e Cross.</span><span class="sxs-lookup"><span data-stu-id="6a515-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![illustrazione che mostra tre ellissi colorate, ognuna con uno stile di tratteggio diverso](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="6a515-126">Pennelli trama</span><span class="sxs-lookup"><span data-stu-id="6a515-126">Texture Brushes</span></span>

<span data-ttu-id="6a515-127">Con un pennello trama è possibile riempire una forma con un modello archiviato in una bitmap.</span><span class="sxs-lookup"><span data-stu-id="6a515-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="6a515-128">Si supponga, ad esempio, che l'immagine seguente venga archiviata in un file su disco denominato MyTexture.bmp.</span><span class="sxs-lookup"><span data-stu-id="6a515-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![Screenshot di un piccolo quadrato riempito con vari colori](images/aboutgdip02-art19.png)

<span data-ttu-id="6a515-130&quot;>Nell'esempio seguente viene riempita un'ellisse ripetendo l'immagine archiviata in MyTexture.bmp.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6a515-130&quot;>The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L&quot;MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="6a515-131">Nell'illustrazione seguente viene mostrata l'ellisse piena.</span><span class="sxs-lookup"><span data-stu-id="6a515-131">The following illustration shows the filled ellipse.</span></span>

![illustrazione che mostra un'ellisse riempita con il modello definito in precedenza](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="6a515-133">Pennelli sfumatura</span><span class="sxs-lookup"><span data-stu-id="6a515-133">Gradient Brushes</span></span>

<span data-ttu-id="6a515-134">È possibile utilizzare un pennello sfumatura per riempire una forma con un colore che cambia gradualmente da una parte della forma a un'altra.</span><span class="sxs-lookup"><span data-stu-id="6a515-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="6a515-135">Un pennello sfumato orizzontale, ad esempio, cambierà colore mentre si sposta dal lato sinistro di una figura a destra.</span><span class="sxs-lookup"><span data-stu-id="6a515-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="6a515-136">Nell'esempio seguente viene riempita un'ellisse con un pennello sfumato orizzontale che passa da blu a verde mentre si sposta dal lato sinistro dell'ellisse al lato destro.</span><span class="sxs-lookup"><span data-stu-id="6a515-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="6a515-137">Nell'illustrazione seguente viene mostrata l'ellisse piena.</span><span class="sxs-lookup"><span data-stu-id="6a515-137">The following illustration shows the filled ellipse.</span></span>

![illustrazione che mostra un'ellisse con un riempimento sfumato: blu a destra verso il verde a sinistra](images/aboutgdip02-art21.png)

<span data-ttu-id="6a515-139">Un pennello sfumatura percorso può essere configurato per modificare il colore mentre si sposta dal centro di una figura verso il limite.</span><span class="sxs-lookup"><span data-stu-id="6a515-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![illustrazione di un'ellisse con blu scuro al centro, ombreggiatura a blu chiaro sul bordo](images/aboutgdip02-art22.png)

<span data-ttu-id="6a515-141">I pennelli sfumatura del percorso sono piuttosto flessibili.</span><span class="sxs-lookup"><span data-stu-id="6a515-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="6a515-142">Il pennello sfumatura utilizzato per riempire il triangolo nell'illustrazione seguente passa gradualmente da rosso al centro a ognuno dei tre colori diversi nei vertici.</span><span class="sxs-lookup"><span data-stu-id="6a515-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![illustrazione di un triangolo rosso al centro, ombreggiatura a un colore diverso in ogni vertice](images/aboutgdip02-art23.png)

 

 



