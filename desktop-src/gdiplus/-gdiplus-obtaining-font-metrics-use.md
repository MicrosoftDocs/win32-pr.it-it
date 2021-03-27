---
description: 'La classe FontFamily fornisce i metodi seguenti che recuperano varie metriche per una particolare combinazione famiglia/stile:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Recupero della metrica dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049469"
---
# <a name="obtaining-font-metrics"></a><span data-ttu-id="5d8c4-103">Recupero della metrica dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="5d8c4-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="5d8c4-104">La classe [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) fornisce i metodi seguenti che recuperano varie metriche per una particolare combinazione famiglia/stile:</span><span class="sxs-lookup"><span data-stu-id="5d8c4-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="5d8c4-105">[**FontFamily:: GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5d8c4-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="5d8c4-106">[**FontFamily:: GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5d8c4-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="5d8c4-107">[**FontFamily:: GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5d8c4-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="5d8c4-108">[**FontFamily:: GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="5d8c4-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="5d8c4-109">I numeri restituiti da questi metodi sono in unità di progettazione dei tipi di carattere, quindi sono indipendenti dalle dimensioni e dalle unità di un particolare oggetto [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="5d8c4-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="5d8c4-110">Nella figura seguente vengono mostrati i valori di ascesa, discesa e interlinea.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![diagramma di due caratteri nelle righe adiacenti, che mostra l'ascesa delle celle, la discesa della cella e l'interlinea](images/fontstext7a.png)

<span data-ttu-id="5d8c4-112">Nell'esempio seguente vengono visualizzate le metriche per lo stile regolare della famiglia di caratteri Arial.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="5d8c4-113">Il codice crea anche un oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (basato sulla famiglia Arial) con dimensioni pari a 16 pixel e visualizza le metriche (in pixel) per quel particolare oggetto **tipo di carattere** .</span><span class="sxs-lookup"><span data-stu-id="5d8c4-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



<span data-ttu-id="5d8c4-114">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-114">The following illustration shows the output of the preceding code.</span></span>

![Screenshot di una finestra con testo che indica le dimensioni e l'altezza del carattere e l'ascesa, la discesa e l'interlinea](images/fontstext8.png)

<span data-ttu-id="5d8c4-116">Prendere nota delle prime due righe di output nell'illustrazione precedente.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="5d8c4-117">L'oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) restituisce una dimensione di 16 e l'oggetto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) restituisce un'altezza em di 2.048.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="5d8c4-118">Questi due numeri (16 e 2.048) rappresentano la chiave per la conversione tra le unità di progettazione dei tipi di carattere e le unità (in questo caso pixel) dell'oggetto **tipo di carattere** .</span><span class="sxs-lookup"><span data-stu-id="5d8c4-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="5d8c4-119">Ad esempio, è possibile convertire l'ascesa da unità di progettazione a pixel come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5d8c4-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![equazione che moltiplica 1854 unità di progettazione per 16 pixel divise per 2048 unità di progettazione, equivalenti a 14,484375 pixel](images/fontstext9.png)

<span data-ttu-id="5d8c4-121">Il codice precedente posiziona il testo verticalmente impostando il membro dati *y* di un oggetto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) .</span><span class="sxs-lookup"><span data-stu-id="5d8c4-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="5d8c4-122">La coordinata y viene aumentata da `font.GetHeight(0.0f)` per ogni nuova riga di testo.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="5d8c4-123">Il metodo [**font:: GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) di un oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) restituisce l'interlinea (in pixel) per quel particolare oggetto **tipo di carattere** .</span><span class="sxs-lookup"><span data-stu-id="5d8c4-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="5d8c4-124">In questo esempio, il numero restituito da **font:: GetHeight** è 18,398438.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="5d8c4-125">Si noti che si tratta dello stesso numero ottenuto convertendo la metrica di interlinea in pixel.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 
