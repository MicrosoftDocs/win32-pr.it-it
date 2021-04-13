---
description: 'A volte può essere necessario creare una bitmap fuori schermo con le caratteristiche seguenti:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Uso della modalità di composizione per controllare la fusione alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978911"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="68a53-103">Uso della modalità di composizione per controllare la fusione alfa</span><span class="sxs-lookup"><span data-stu-id="68a53-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="68a53-104">A volte può essere necessario creare una bitmap fuori schermo con le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="68a53-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="68a53-105">I colori hanno valori alfa minori di 255.</span><span class="sxs-lookup"><span data-stu-id="68a53-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="68a53-106">Quando si crea la bitmap, i colori non vengono combinati con l'alfa.</span><span class="sxs-lookup"><span data-stu-id="68a53-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="68a53-107">Quando si visualizza la bitmap completata, i colori nella bitmap sono alpha blended con i colori di sfondo sul dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="68a53-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="68a53-108">Per creare una bitmap di questo tipo, costruire un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) vuoto e quindi costruire un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su tale bitmap.</span><span class="sxs-lookup"><span data-stu-id="68a53-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="68a53-109">Impostare la modalità di composizione dell'oggetto **Graphics** su CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="68a53-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="68a53-110">Nell'esempio seguente viene creato un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="68a53-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="68a53-111">Il codice usa l'oggetto **Graphics** insieme a due pennelli semitrasparenti (alpha = 160) per disegnare sulla bitmap.</span><span class="sxs-lookup"><span data-stu-id="68a53-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="68a53-112">Il codice riempie un'ellisse rossa e un'ellisse verde usando i pennelli semitrasparenti.</span><span class="sxs-lookup"><span data-stu-id="68a53-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="68a53-113">L'ellisse verde si sovrappone all'ellisse rossa, ma il verde non viene mescolato con il rosso perché la modalità di composizione dell'oggetto **Graphics** è impostata su CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="68a53-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="68a53-114">Successivamente, il codice viene preparato per l'estrazione sullo schermo chiamando [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) e creando un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68a53-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="68a53-115">Il codice disegna la bitmap sullo schermo due volte: una volta su uno sfondo bianco e una volta su uno sfondo a più colori.</span><span class="sxs-lookup"><span data-stu-id="68a53-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="68a53-116">I pixel nella bitmap che fanno parte dei due ellissi hanno un componente alfa di 160, quindi i puntini di sospensione vengono combinati con i colori di sfondo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="68a53-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



<span data-ttu-id="68a53-117">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="68a53-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="68a53-118">Si noti che i puntini di sospensione vengono combinati con lo sfondo, ma non sono combinati tra loro.</span><span class="sxs-lookup"><span data-stu-id="68a53-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![illustrazione che mostra due ellissi colorate in modo diverso, ciascuna delle quali si fonde con lo sfondo multicolore](images/sourcecopy.png)

<span data-ttu-id="68a53-120">Nell'esempio di codice precedente è presente l'istruzione seguente:</span><span class="sxs-lookup"><span data-stu-id="68a53-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="68a53-121">Se si desidera che i puntini di sospensione vengano combinati tra loro e con lo sfondo, modificare l'istruzione seguente:</span><span class="sxs-lookup"><span data-stu-id="68a53-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="68a53-122">Nella figura seguente viene illustrato l'output del codice modificato.</span><span class="sxs-lookup"><span data-stu-id="68a53-122">The following illustration shows the output of the revised code.</span></span>

![uso della modalità di composizione per controllare l'illustrazione della fusione alfa](images/sourceover.png)

 

 



