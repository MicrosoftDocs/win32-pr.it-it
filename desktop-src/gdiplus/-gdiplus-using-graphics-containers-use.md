---
description: Un oggetto Graphics fornisce metodi quali DrawLine, DrawImage e DrawString per la visualizzazione di immagini vettoriali, immagini raster e testo.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilizzo dei contenitori di grafica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978906"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="7032f-103">Utilizzo dei contenitori di grafica</span><span class="sxs-lookup"><span data-stu-id="7032f-103">Using Graphics Containers</span></span>

<span data-ttu-id="7032f-104">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce metodi quali [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))e [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) per la visualizzazione di immagini vettoriali, immagini raster e testo.</span><span class="sxs-lookup"><span data-stu-id="7032f-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="7032f-105">Un oggetto **Graphics** dispone inoltre di diverse proprietà che influenzano la qualità e l'orientamento degli elementi disegnati.</span><span class="sxs-lookup"><span data-stu-id="7032f-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="7032f-106">Ad esempio, la proprietà modalità di smussamento determina se l'anti-aliasing viene applicato a linee e curve e la proprietà trasformazione globale influisce sulla posizione e sulla rotazione degli elementi disegnati.</span><span class="sxs-lookup"><span data-stu-id="7032f-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="7032f-107">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è spesso associato a un particolare dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7032f-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="7032f-108">Quando si usa un oggetto **Graphics** per il progetto in una finestra, l'oggetto **Graphics** viene associato anche a tale finestra specifica.</span><span class="sxs-lookup"><span data-stu-id="7032f-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="7032f-109">Un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) può essere considerato come un contenitore perché include un set di proprietà che influenzano il disegno ed è collegato a informazioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7032f-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="7032f-110">È possibile creare un contenitore secondario in un oggetto **Graphics** esistente chiamando il metodo [BeginContainer](/previous-versions//ms535731(v=vs.85)) dell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="7032f-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="7032f-111">Gli argomenti seguenti riguardano gli oggetti [**grafici**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e i contenitori annidati in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="7032f-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="7032f-112">Stato di un oggetto Graphics</span><span class="sxs-lookup"><span data-stu-id="7032f-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="7032f-113">Contenitori di oggetti Graphics annidati</span><span class="sxs-lookup"><span data-stu-id="7032f-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
