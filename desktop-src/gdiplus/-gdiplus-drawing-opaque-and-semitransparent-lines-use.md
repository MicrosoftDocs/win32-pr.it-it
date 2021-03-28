---
description: Quando si crea una linea, è necessario passare l'indirizzo di un oggetto Pen al metodo DrawLine della classe Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Disegno di linee opache e semitrasparenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558318"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="9bca2-103">Disegno di linee opache e semitrasparenti</span><span class="sxs-lookup"><span data-stu-id="9bca2-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="9bca2-104">Quando si crea una linea, è necessario passare l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) al metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="9bca2-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="9bca2-105">Uno dei parametri del costruttore **Pen** è un oggetto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="9bca2-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="9bca2-106">Per disegnare una linea opaca, impostare il componente alfa del colore su 255.</span><span class="sxs-lookup"><span data-stu-id="9bca2-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="9bca2-107">Per disegnare una linea semitrasparente, impostare il componente alfa su un valore qualsiasi compreso tra 1 e 254.</span><span class="sxs-lookup"><span data-stu-id="9bca2-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="9bca2-108">Quando si disegna una linea semitrasparente su uno sfondo, il colore della linea viene sfumato con i colori dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="9bca2-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="9bca2-109">Il componente alfa specifica il modo in cui vengono combinati i colori della linea e dello sfondo; i valori alfa vicini a 0 hanno un peso maggiore sui colori di sfondo e i valori alfa vicini a 255 prevalgono più sul colore della linea.</span><span class="sxs-lookup"><span data-stu-id="9bca2-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="9bca2-110">Nell'esempio seguente viene disegnata un'immagine, quindi vengono disegnate tre linee che usano l'immagine come sfondo.</span><span class="sxs-lookup"><span data-stu-id="9bca2-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="9bca2-111">Per la prima linea si usa un componente alfa con un valore pari a 255, quindi la linea risulta opaca.</span><span class="sxs-lookup"><span data-stu-id="9bca2-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="9bca2-112">Per la seconda e la terza linea si usa un componente alfa con un valore pari a 128, quindi le linee risultano semitrasparenti. L'immagine di sfondo è visibile attraverso le linee.</span><span class="sxs-lookup"><span data-stu-id="9bca2-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="9bca2-113">La chiamata a [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fa sì che la fusione per la terza riga venga eseguita insieme alla correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="9bca2-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



<span data-ttu-id="9bca2-114">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="9bca2-114">The following illustration shows the output of the preceding code.</span></span>

![illustrazione che mostra un'immagine sovrapposta da tre linee larghe: una opaca, una leggermente trasparente e una molto trasparente](images/compqualline.png)

 

 



