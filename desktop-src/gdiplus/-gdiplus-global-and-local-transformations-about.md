---
description: Una trasformazione globale è una trasformazione che viene applicata a ogni elemento disegnato da un determinato oggetto Graphics.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Trasformazioni globali e locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557708"
---
# <a name="global-and-local-transformations"></a><span data-ttu-id="c4240-103">Trasformazioni globali e locali</span><span class="sxs-lookup"><span data-stu-id="c4240-103">Global and Local Transformations</span></span>

<span data-ttu-id="c4240-104">Una trasformazione globale è una trasformazione che viene applicata a ogni elemento disegnato da un determinato oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c4240-104">A global transformation is a transformation that applies to every item drawn by a given [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c4240-105">Per creare una trasformazione globale, costruire un oggetto **Graphics** , quindi chiamare il metodo [**Graphics:: setransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) .</span><span class="sxs-lookup"><span data-stu-id="c4240-105">To create a global transformation, construct a **Graphics** object, and then call its [**Graphics::SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) method.</span></span> <span data-ttu-id="c4240-106">Il metodo **Graphics:: setransform** modifica un oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) associato all'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c4240-106">The **Graphics::SetTransform** method manipulates a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object that is associated with the **Graphics** object.</span></span> <span data-ttu-id="c4240-107">La trasformazione archiviata nell'oggetto **matrice** viene chiamata *trasformazione globale*.</span><span class="sxs-lookup"><span data-stu-id="c4240-107">The transformation stored in that **Matrix** object is called the *world transformation*.</span></span> <span data-ttu-id="c4240-108">La trasformazione mondiale può essere una semplice trasformazione affine o una complessa sequenza di trasformazioni affini, ma indipendentemente dalla complessità, la trasformazione globale è archiviata in un singolo oggetto **Matrix** .</span><span class="sxs-lookup"><span data-stu-id="c4240-108">The world transformation can be a simple affine transformation or a complex sequence of affine transformations, but regardless of its complexity, the world transformation is stored in a single **Matrix** object.</span></span>

<span data-ttu-id="c4240-109">La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce diversi metodi per la creazione di una trasformazione globale composita: [**Graphics:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)e [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span><span class="sxs-lookup"><span data-stu-id="c4240-109">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several methods for building up a composite world transformation: [**Graphics::MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics::ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform), and [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span></span> <span data-ttu-id="c4240-110">Nell'esempio seguente viene disegnata un'ellisse due volte: una volta prima di creare una trasformazione globale e una volta dopo.</span><span class="sxs-lookup"><span data-stu-id="c4240-110">The following example draws an ellipse twice: once before creating a world transformation and once after.</span></span> <span data-ttu-id="c4240-111">La trasformazione viene innanzitutto ridimensionata in base a un fattore di 0,5 nella direzione y, quindi converte 50 unità nella direzione x e quindi ruota di 30 gradi.</span><span class="sxs-lookup"><span data-stu-id="c4240-111">The transformation first scales by a factor of 0.5 in the y direction, then translates 50 units in the x direction, and then rotates 30 degrees.</span></span>


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



<span data-ttu-id="c4240-112">Nella figura seguente vengono illustrati l'ellisse originale e l'ellisse trasformata.</span><span class="sxs-lookup"><span data-stu-id="c4240-112">The following illustration shows the original ellipse and the transformed ellipse.</span></span>

![Screenshot di una finestra che contiene due ellissi sovrapposti; uno è più piccolo e ruotato](images/aboutgdip05-art14.png)

> [!Note]  
> <span data-ttu-id="c4240-114">Nell'esempio precedente, l'ellisse viene ruotata sull'origine del sistema di coordinate, che si trova nell'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="c4240-114">In the previous example, the ellipse is rotated about the origin of the coordinate system, which is at the upper–left corner of the client area.</span></span> <span data-ttu-id="c4240-115">Questo produce un risultato diverso rispetto alla rotazione dell'ellisse sul proprio centro.</span><span class="sxs-lookup"><span data-stu-id="c4240-115">This produces a different result than rotating the ellipse about its own center.</span></span>

 

<span data-ttu-id="c4240-116">Una trasformazione locale è una trasformazione che si applica a un elemento specifico da disegnare.</span><span class="sxs-lookup"><span data-stu-id="c4240-116">A local transformation is a transformation that applies to a specific item to be drawn.</span></span> <span data-ttu-id="c4240-117">Un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , ad esempio, dispone di un metodo [**GraphicsPath:: Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) che consente di trasformare i punti dati di tale percorso.</span><span class="sxs-lookup"><span data-stu-id="c4240-117">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that allows you to transform the data points of that path.</span></span> <span data-ttu-id="c4240-118">Nell'esempio seguente viene disegnato un rettangolo senza trasformazione e un percorso con una trasformazione di rotazione.</span><span class="sxs-lookup"><span data-stu-id="c4240-118">The following example draws a rectangle with no transformation and a path with a rotation transformation.</span></span> <span data-ttu-id="c4240-119">(Si supponga che non esista alcuna trasformazione globale).</span><span class="sxs-lookup"><span data-stu-id="c4240-119">(Assume that there is no world transformation.)</span></span>


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="c4240-120">È possibile combinare la trasformazione globale con le trasformazioni locali per ottenere una serie di risultati.</span><span class="sxs-lookup"><span data-stu-id="c4240-120">You can combine the world transformation with local transformations to achieve a variety of results.</span></span> <span data-ttu-id="c4240-121">È ad esempio possibile utilizzare la trasformazione mondo per modificare il sistema di coordinate e utilizzare le trasformazioni locali per ruotare e ridimensionare gli oggetti disegnati nel nuovo sistema di coordinate.</span><span class="sxs-lookup"><span data-stu-id="c4240-121">For example, you can use the world transformation to revise the coordinate system and use local transformations to rotate and scale objects drawn on the new coordinate system.</span></span>

<span data-ttu-id="c4240-122">Si supponga di volere un sistema di coordinate con origine 200 pixel dal bordo sinistro dell'area client e 150 pixel dalla parte superiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="c4240-122">Suppose you want a coordinate system that has its origin 200 pixels from the left edge of the client area and 150 pixels from the top of the client area.</span></span> <span data-ttu-id="c4240-123">Si supponga inoltre che l'unità di misura sia il pixel, con l'asse x che punta verso destra e l'asse y che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="c4240-123">Furthermore, assume that you want the unit of measure to be the pixel, with the x-axis pointing to the right and the y-axis pointing up.</span></span> <span data-ttu-id="c4240-124">Il sistema di coordinate predefinito ha l'asse y che punta verso il basso ed è quindi necessario eseguire una reflection sull'asse orizzontale.</span><span class="sxs-lookup"><span data-stu-id="c4240-124">The default coordinate system has the y-axis pointing down, so you need to perform a reflection across the horizontal axis.</span></span> <span data-ttu-id="c4240-125">Nella figura seguente viene illustrata la matrice di tale Reflection.</span><span class="sxs-lookup"><span data-stu-id="c4240-125">The following illustration shows the matrix of such a reflection.</span></span>

![illustrazione che mostra una matrice tre per tre](images/aboutgdip05-art15.png)

<span data-ttu-id="c4240-127">Si supponga quindi che sia necessario eseguire una traduzione 200 unità a destra e 150 unità in basso.</span><span class="sxs-lookup"><span data-stu-id="c4240-127">Next, assume you need to perform a translation 200 units to the right and 150 units down.</span></span>

<span data-ttu-id="c4240-128">Nell'esempio seguente viene stabilito il sistema di coordinate appena descritto impostando la trasformazione globale di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c4240-128">The following example establishes the coordinate system just described by setting the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



<span data-ttu-id="c4240-129">Il codice seguente (inserito dopo il codice nell'esempio precedente) crea un percorso costituito da un singolo rettangolo con l'angolo inferiore sinistro all'origine del nuovo sistema di coordinate.</span><span class="sxs-lookup"><span data-stu-id="c4240-129">The following code (placed after the code in the preceding example) creates a path that consists of a single rectangle with its lower-left corner at the origin of the new coordinate system.</span></span> <span data-ttu-id="c4240-130">Il rettangolo viene compilato una volta senza alcuna trasformazione locale e una volta con una trasformazione locale.</span><span class="sxs-lookup"><span data-stu-id="c4240-130">The rectangle is filled once with no local transformation and once with a local transformation.</span></span> <span data-ttu-id="c4240-131">La trasformazione locale è costituita da un ridimensionamento orizzontale di un fattore 2 seguito da una rotazione di 30 gradi.</span><span class="sxs-lookup"><span data-stu-id="c4240-131">The local transformation consists of a horizontal scaling by a factor of 2 followed by a 30-degree rotation.</span></span>


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



<span data-ttu-id="c4240-132">Nella figura seguente vengono illustrati il nuovo sistema di coordinate e i due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="c4240-132">The following illustration shows the new coordinate system and the two rectangles.</span></span>

![Screenshot di un asse x e y e un quadrato blu sovrapposto a una semitrasparente rectagle ruotata intorno all'angolo inferiore sinistro](images/aboutgdip05-art16.png)

 

 



