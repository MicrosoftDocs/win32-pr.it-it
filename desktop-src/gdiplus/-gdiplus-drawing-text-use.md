---
description: È possibile usare il metodo DrawString della classe Graphics per creare testo in una posizione specificata o all'interno di un rettangolo specificato.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Creazione di testo (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131347"
---
# <a name="drawing-text-gdi"></a><span data-ttu-id="9fb2e-103">Creazione di testo (GDI+)</span><span class="sxs-lookup"><span data-stu-id="9fb2e-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="9fb2e-104">È possibile usare il metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per creare testo in una posizione specificata o all'interno di un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="9fb2e-105">Disegno di testo in una posizione specificata</span><span class="sxs-lookup"><span data-stu-id="9fb2e-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="9fb2e-106">Disegno di testo in un rettangolo</span><span class="sxs-lookup"><span data-stu-id="9fb2e-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="9fb2e-107">Disegno di testo in una posizione specificata</span><span class="sxs-lookup"><span data-stu-id="9fb2e-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="9fb2e-108">Per creare testo in una posizione specifica, sono necessari oggetti [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="9fb2e-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="9fb2e-109">Nell'esempio seguente viene disegnata la stringa "Hello" nella posizione (30, 10).</span><span class="sxs-lookup"><span data-stu-id="9fb2e-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="9fb2e-110">La famiglia di caratteri è Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-110">The font family is Times New Roman.</span></span> <span data-ttu-id="9fb2e-111">Il tipo di carattere, che è un singolo membro della famiglia di caratteri, è Times New Roman, Size 24 pixels, regular Style.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="9fb2e-112">Si supponga che **Graphics** sia un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) esistente.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="9fb2e-113">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-113">The following illustration shows the output of the preceding code.</span></span>

![Screenshot di una piccola finestra contenente il testo "Hello"](images/fontstext1.png)

<span data-ttu-id="9fb2e-115">Nell'esempio precedente, il costruttore [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) riceve una stringa che identifica la famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="9fb2e-116">L'indirizzo dell'oggetto **FontFamily** viene passato come primo argomento al costruttore del [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="9fb2e-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="9fb2e-117">Il secondo argomento passato al costruttore del **tipo di carattere** specifica la dimensione del tipo di carattere misurato in unità fornite dal quarto argomento.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="9fb2e-118">Il terzo argomento specifica lo stile (normale, grassetto, corsivo e così via) del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="9fb2e-119">Il metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) riceve cinque argomenti.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="9fb2e-120">Il primo argomento è la stringa da disegnare e il secondo argomento è la lunghezza (in caratteri, non byte) di tale stringa.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="9fb2e-121">Se la stringa è con terminazione null, è possibile passare-1 per la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="9fb2e-122">Il terzo argomento è l'indirizzo dell'oggetto del [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="9fb2e-123">Il quarto argomento è un oggetto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) che contiene le coordinate dell'angolo superiore sinistro della stringa.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="9fb2e-124">Il quinto argomento è l'indirizzo di un oggetto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) che verrà utilizzato per inserire i caratteri della stringa.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="9fb2e-125">Disegno di testo in un rettangolo</span><span class="sxs-lookup"><span data-stu-id="9fb2e-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="9fb2e-126">Uno dei metodi [**DrawString**](https://www.bing.com/search?q=**DrawString**) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ha un parametro *RectF* .</span><span class="sxs-lookup"><span data-stu-id="9fb2e-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="9fb2e-127">Chiamando il metodo **DrawString** , è possibile creare un testo che esegue il wrapping in un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="9fb2e-128">Per creare testo in un rettangolo, sono necessari oggetti **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="9fb2e-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="9fb2e-129">Nell'esempio seguente viene creato un rettangolo con angolo superiore sinistro (30, 10), larghezza 100 e altezza 122.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="9fb2e-130">Il codice disegna quindi una stringa all'interno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="9fb2e-131">La stringa è limitata al rettangolo e viene eseguito il wrapping in modo tale che le singole parole non vengano interrotte.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

<span data-ttu-id="9fb2e-132">Nella figura seguente viene illustrato il testo disegnato nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-132">The following illustration shows the text drawn in the rectangle.</span></span>

![Screenshot di una piccola finestra contenente un recangle, all'interno della quale viene visualizzata la prima parte di una frase](images/fontstext2.png)

<span data-ttu-id="9fb2e-134">Nell'esempio precedente, il quarto argomento passato al metodo [**DrawString**](https://www.bing.com/search?q=**DrawString**) è un oggetto [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) che specifica il rettangolo di delimitazione per il testo.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="9fb2e-135">Il quinto parametro è di tipo [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), l'argomento è **null** perché non è richiesta alcuna formattazione speciale della stringa.</span><span class="sxs-lookup"><span data-stu-id="9fb2e-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
