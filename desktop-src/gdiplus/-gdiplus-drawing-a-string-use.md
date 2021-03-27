---
description: Nell'argomento disegno di una linea viene illustrato come scrivere un'applicazione Windows che utilizza Windows GDI+ per disegnare una linea.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Disegno di una stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227083"
---
# <a name="drawing-a-string"></a><span data-ttu-id="32501-103">Disegno di una stringa</span><span class="sxs-lookup"><span data-stu-id="32501-103">Drawing a String</span></span>

<span data-ttu-id="32501-104">Nell'argomento [disegno di una linea](-gdiplus-drawing-a-line-use.md) viene illustrato come scrivere un'applicazione Windows che utilizza Windows GDI+ per disegnare una linea.</span><span class="sxs-lookup"><span data-stu-id="32501-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="32501-105">Per disegnare una stringa, sostituire la funzione **OnPaint** mostrata in tale argomento con la funzione **OnPaint** seguente:</span><span class="sxs-lookup"><span data-stu-id="32501-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



<span data-ttu-id="32501-106">Il codice precedente crea diversi oggetti GDI+.</span><span class="sxs-lookup"><span data-stu-id="32501-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="32501-107">L'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornisce il metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , che esegue il disegno effettivo.</span><span class="sxs-lookup"><span data-stu-id="32501-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="32501-108">L'oggetto [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) specifica il colore della stringa.</span><span class="sxs-lookup"><span data-stu-id="32501-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="32501-109">Il costruttore [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) riceve un singolo argomento stringa che identifica la famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="32501-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="32501-110">L'indirizzo dell'oggetto **FontFamily** è il primo argomento passato al costruttore del [**tipo di carattere**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="32501-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="32501-111">Il secondo argomento passato al costruttore del [tipo di carattere](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) specifica le dimensioni del carattere e il terzo argomento specifica lo stile.</span><span class="sxs-lookup"><span data-stu-id="32501-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="32501-112">Il valore **FontStyleRegular** è un membro dell'enumerazione [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , dichiarata in Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="32501-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="32501-113">L'ultimo argomento del costruttore del **tipo di carattere** indica che la dimensione del tipo di carattere (24 in questo caso) viene misurata in pixel.</span><span class="sxs-lookup"><span data-stu-id="32501-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="32501-114">Il valore **UnitPixel** è un membro dell'enumerazione di [**unità**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .</span><span class="sxs-lookup"><span data-stu-id="32501-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="32501-115">Il primo argomento passato al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) è l'indirizzo di una stringa di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="32501-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="32501-116">Il secondo argomento,-1, specifica che la stringa è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="32501-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="32501-117">Se la stringa non termina con null, il secondo argomento deve specificare il numero di caratteri wide nella stringa. Il terzo argomento è l'indirizzo dell'oggetto del [**tipo di carattere**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="32501-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="32501-118">Il quarto argomento è un riferimento a un oggetto [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) che specifica la posizione in cui verrà disegnata la stringa.</span><span class="sxs-lookup"><span data-stu-id="32501-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="32501-119">L'ultimo argomento è l'indirizzo dell'oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , che specifica il colore della stringa.</span><span class="sxs-lookup"><span data-stu-id="32501-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
