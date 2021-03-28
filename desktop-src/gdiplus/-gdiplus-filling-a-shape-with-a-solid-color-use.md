---
description: Per riempire una forma con un colore a tinta unita, creare un oggetto SolidBrush e quindi passare l'indirizzo di tale oggetto SolidBrush come argomento a uno dei metodi Fill della classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Riempimento di una forma con un colore a tinta unita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994261"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="de8de-103">Riempimento di una forma con un colore a tinta unita</span><span class="sxs-lookup"><span data-stu-id="de8de-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="de8de-104">Per riempire una forma con un colore a tinta unita, creare un oggetto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) e quindi passare l'indirizzo di tale oggetto **SolidBrush** come argomento a uno dei metodi Fill della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="de8de-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="de8de-105">Nell'esempio seguente viene illustrato come riempire un'ellisse con il colore rosso:</span><span class="sxs-lookup"><span data-stu-id="de8de-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="de8de-106">Nell'esempio precedente, il costruttore [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) accetta un riferimento a un oggetto [**colore**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) come unico argomento.</span><span class="sxs-lookup"><span data-stu-id="de8de-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="de8de-107">I valori utilizzati dal costruttore di **colori** rappresentano i componenti alfa, rosso, verde e blu del colore.</span><span class="sxs-lookup"><span data-stu-id="de8de-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="de8de-108">Ognuno di questi valori deve essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="de8de-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="de8de-109">Il primo 255 indica che il colore è completamente opaco e il secondo 255 indica che il componente rosso è a intensità piena.</span><span class="sxs-lookup"><span data-stu-id="de8de-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="de8de-110">I due zeri indicano che i componenti verde e blu hanno un'intensità pari a 0.</span><span class="sxs-lookup"><span data-stu-id="de8de-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="de8de-111">I quattro numeri (0, 0, 100, 60) passati al metodo [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) specificano la posizione e le dimensioni del rettangolo di delimitazione per l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="de8de-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="de8de-112">Il rettangolo ha un angolo superiore sinistro di (0,0), una larghezza di 100 e un'altezza di 60.</span><span class="sxs-lookup"><span data-stu-id="de8de-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
