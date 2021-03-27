---
description: Windows GDI+ offre diversi livelli di qualità per il disegno di testo. In genere, il rendering di qualità superiore impiega più tempo di elaborazione rispetto al rendering di qualità inferiore.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Anti-aliasing con testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994461"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="ba3ff-104">Anti-aliasing con testo</span><span class="sxs-lookup"><span data-stu-id="ba3ff-104">Antialiasing with Text</span></span>

<span data-ttu-id="ba3ff-105">Windows GDI+ offre diversi livelli di qualità per il disegno di testo.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="ba3ff-106">In genere, il rendering di qualità superiore impiega più tempo di elaborazione rispetto al rendering di qualità inferiore.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="ba3ff-107">Il livello di qualità è una proprietà della classe [**grafica**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ba3ff-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="ba3ff-108">Per impostare il livello di qualità, chiamare il metodo [**Graphics:: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) di un oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="ba3ff-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="ba3ff-109">Il metodo **Graphics:: SetTextRenderingHint** riceve uno degli elementi dell'enumerazione [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , dichiarata in Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="ba3ff-110">GDI+ fornisce l'anti-aliasing tradizionale e un nuovo tipo di anti-aliasing basato sulla tecnologia di visualizzazione di Microsoft ClearType disponibile solo in Windows XP e Windows Server 2003 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="ba3ff-111">ClearType smoothing migliora la leggibilità dei monitor LCD a colori che dispongono di un'interfaccia digitale, ad esempio i monitoraggi in computer portatili e schermi desktop flat di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="ba3ff-112">Anche la leggibilità sulle schermate CRT è stata migliorata.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="ba3ff-113">ClearType dipende dall'orientamento e dall'ordinamento dei nastri LCD.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="ba3ff-114">Attualmente ClearType viene implementato solo per le strisce verticali ordinate RGB.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="ba3ff-115">Questo potrebbe costituire un problema se si utilizza un Tablet PC, in cui la visualizzazione può essere orientata in qualsiasi direzione o se si utilizza una schermata che può essere trasformata dall'orizzontale al verticale.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="ba3ff-116">Nell'esempio seguente viene disegnato un testo con due impostazioni di qualità diverse:</span><span class="sxs-lookup"><span data-stu-id="ba3ff-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="ba3ff-117">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-117">The following illustration shows the output of the preceding code.</span></span>

![Screenshot di una stringa i cui caratteri hanno bordi frastagliati contrapposti a uno con bordi smussati](images/fontstext10.png)

 

 



