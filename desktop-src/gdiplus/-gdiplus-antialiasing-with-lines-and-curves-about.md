---
description: Quando si utilizza Windows GDI+ per creare una linea, si specifica il punto iniziale e il punto finale della linea, ma non è necessario fornire informazioni sui singoli pixel della riga.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Anti-aliasing con linee e curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755775"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="c9233-103">Anti-aliasing con linee e curve</span><span class="sxs-lookup"><span data-stu-id="c9233-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="c9233-104">Quando si utilizza Windows GDI+ per creare una linea, si specifica il punto iniziale e il punto finale della linea, ma non è necessario fornire informazioni sui singoli pixel della riga.</span><span class="sxs-lookup"><span data-stu-id="c9233-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="c9233-105">GDI+ funziona insieme al software per i driver di visualizzazione per determinare quali pixel verranno accesi per visualizzare la riga in un particolare dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c9233-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="c9233-106">Prendere in considerazione una linea rossa diritta che va dal punto (4, 2) al punto (16, 10).</span><span class="sxs-lookup"><span data-stu-id="c9233-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="c9233-107">Si supponga che il sistema di coordinate abbia l'origine nell'angolo superiore sinistro e che l'unità di misura sia il pixel.</span><span class="sxs-lookup"><span data-stu-id="c9233-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="c9233-108">Si supponga inoltre che l'asse x punti a destra e che l'asse y punti verso il basso.</span><span class="sxs-lookup"><span data-stu-id="c9233-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="c9233-109">Nella figura seguente viene illustrata una vista ingrandita della linea rossa disegnata su uno sfondo a più colori.</span><span class="sxs-lookup"><span data-stu-id="c9233-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![illustrazione che mostra i pixel rossi a tinta unita su uno sfondo multicolore](images/aboutgdip02-art33.png)

<span data-ttu-id="c9233-111">Si noti che i pixel rossi utilizzati per il rendering della linea sono opachi.</span><span class="sxs-lookup"><span data-stu-id="c9233-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="c9233-112">Non sono presenti pixel parzialmente trasparenti per la visualizzazione della riga.</span><span class="sxs-lookup"><span data-stu-id="c9233-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="c9233-113">Questo tipo di rendering della linea fornisce un aspetto irregolare alla riga e la linea appare come una scalinata.</span><span class="sxs-lookup"><span data-stu-id="c9233-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="c9233-114">Questa tecnica di rappresentazione di una linea con una scala è detta aliasing; la scala è un alias per la linea teorica.</span><span class="sxs-lookup"><span data-stu-id="c9233-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="c9233-115">Una tecnica più sofisticata per il rendering di una linea prevede l'uso di pixel parzialmente trasparenti insieme ai pixel rossi puri.</span><span class="sxs-lookup"><span data-stu-id="c9233-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="c9233-116">I pixel sono impostati su rosso puro o su una combinazione di rosso e il colore di sfondo, a seconda della distanza con cui si trovano nella riga.</span><span class="sxs-lookup"><span data-stu-id="c9233-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="c9233-117">Questo tipo di rendering è denominato anti-aliasing e produce una linea che l'occhio umano percepisce come più uniforme.</span><span class="sxs-lookup"><span data-stu-id="c9233-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="c9233-118">Nella figura seguente viene illustrato il modo in cui alcuni pixel vengono combinati con lo sfondo per produrre una riga con antialiasing.</span><span class="sxs-lookup"><span data-stu-id="c9233-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![illustrazione che mostra i pixel con sfumature di rosso sullo stesso sfondo](images/aboutgdip02-art34.png)

<span data-ttu-id="c9233-120">L'anti-aliasing (smussamento) può essere applicato anche alle curve.</span><span class="sxs-lookup"><span data-stu-id="c9233-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="c9233-121">La figura seguente mostra una visualizzazione ingrandita di un'ellisse smussata.</span><span class="sxs-lookup"><span data-stu-id="c9233-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![illustrazione di un'ellisse composta da diverse sfumature di pixel blu su uno sfondo bianco](images/aboutgdip02-art35.png)

<span data-ttu-id="c9233-123">La figura seguente mostra la stessa ellisse nelle dimensioni effettive, una volta senza anti-aliasing e una volta con l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="c9233-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![Screenshot di due puntini di sospensione: quello con anti-aliasing appare più semplice](images/aboutgdip02-art36.png)

<span data-ttu-id="c9233-125">Per creare linee e curve che usano l'anti-aliasing, creare un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passare *SmoothingModeAntiAlias* al relativo metodo [**Graphics:: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="c9233-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="c9233-126">Quindi, chiamare uno dei metodi di disegno dello stesso oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c9233-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="c9233-127">**SmoothingModeAntiAlias** è un elemento dell'enumerazione [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="c9233-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



