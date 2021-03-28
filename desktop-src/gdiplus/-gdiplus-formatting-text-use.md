---
description: Per applicare una formattazione speciale al testo, inizializzare un oggetto StringFormat e passare l'indirizzo dell'oggetto al metodo DrawString della classe Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formattazione del testo (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563403"
---
# <a name="formatting-text-gdi"></a><span data-ttu-id="aa0a6-103">Formattazione del testo (GDI+)</span><span class="sxs-lookup"><span data-stu-id="aa0a6-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="aa0a6-104">Per applicare una formattazione speciale al testo, inizializzare un oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e passare l'indirizzo dell'oggetto al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="aa0a6-105">Per creare testo formattato in un rettangolo, sono necessari oggetti [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)e [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="aa0a6-106">Allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="aa0a6-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="aa0a6-107">Impostazione tabulazioni</span><span class="sxs-lookup"><span data-stu-id="aa0a6-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="aa0a6-108">Disegno di testo verticale</span><span class="sxs-lookup"><span data-stu-id="aa0a6-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="aa0a6-109">Allineamento del testo</span><span class="sxs-lookup"><span data-stu-id="aa0a6-109">Aligning Text</span></span>

<span data-ttu-id="aa0a6-110">Nell'esempio seguente viene disegnato un testo in un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="aa0a6-111">Ogni riga di testo viene centrata (affiancata) e l'intero blocco di testo viene centrato (dall'alto verso il basso) nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="aa0a6-112">Nella figura seguente vengono illustrati il rettangolo e il testo centrato.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-112">The following illustration shows the rectangle and the centered text.</span></span>

![Screenshot di una finestra contenente un rettangolo, che contiene sei righe di testo, centrate orizzontalmente](images/fontstext3.png)

<span data-ttu-id="aa0a6-114">Il codice precedente chiama due metodi dell'oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: sealignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) e [**StringFormat:: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span><span class="sxs-lookup"><span data-stu-id="aa0a6-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="aa0a6-115">La chiamata a **StringFormat:: Sealignment** specifica che ogni riga di testo viene centrata nel rettangolo specificato dal terzo argomento passato al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="aa0a6-116">La chiamata a **StringFormat:: SetLineAlignment** specifica che il blocco di testo viene centrato (dall'alto verso il basso) nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="aa0a6-117">Il valore [\* \* \* \* StringAlignmentCenter \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) \* \* è un elemento dell'enumerazione **StringAlignment** , dichiarata in Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="aa0a6-118">Impostazione tabulazioni</span><span class="sxs-lookup"><span data-stu-id="aa0a6-118">Setting Tab Stops</span></span>

<span data-ttu-id="aa0a6-119">È possibile impostare le tabulazioni per il testo chiamando il metodo [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) di un oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , quindi passando l'indirizzo di tale oggetto **StringFormat** al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="aa0a6-120">Nell'esempio seguente vengono impostate le tabulazioni a 150, 250 e 350.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="aa0a6-121">Il codice Visualizza quindi un elenco a schede di nomi e punteggi dei test.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-121">Then the code displays a tabbed list of names and test scores.</span></span>


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="aa0a6-122">Nella figura seguente viene illustrato il testo a schede.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-122">The following illustration shows the tabbed text.</span></span>

![illustrazione di un rettangolo contenente quattro colonne di testo; ogni colonna è Left-allineati](images/fontstext4.png)

<span data-ttu-id="aa0a6-124">Il codice precedente passa tre argomenti al metodo [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="aa0a6-125">Il terzo argomento è l'indirizzo di una matrice contenente gli offset di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="aa0a6-126">Il secondo argomento indica che nella matrice sono presenti tre offset.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="aa0a6-127">Il primo argomento passato a **StringFormat:: SetTabStops** è 0, che indica che il primo offset nella matrice viene misurato dalla posizione 0, dal bordo sinistro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="aa0a6-128">Disegno di testo verticale</span><span class="sxs-lookup"><span data-stu-id="aa0a6-128">Drawing Vertical Text</span></span>

<span data-ttu-id="aa0a6-129">È possibile utilizzare un oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) per specificare che il testo deve essere disegnato verticalmente anziché orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="aa0a6-130">Nell'esempio seguente il valore [\* \* \* \* StringFormatFlagsDirectionVertical \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) viene passato al metodo [**StringFormat:: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) di un oggetto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="aa0a6-131">L'indirizzo dell'oggetto **StringFormat** viene passato al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="aa0a6-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="aa0a6-132">Il valore [\* \* \* \* StringFormatFlagsDirectionVertical \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* è un elemento dell'enumerazione **StringFormatFlags** , dichiarata in Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



<span data-ttu-id="aa0a6-133">Nella figura seguente viene illustrato il testo verticale.</span><span class="sxs-lookup"><span data-stu-id="aa0a6-133">The following illustration shows the vertical text.</span></span>

![illustrazione che mostra una finestra contenente testo ruotato di 90 gradi in senso orario](images/fontstext5.png)

 

 



