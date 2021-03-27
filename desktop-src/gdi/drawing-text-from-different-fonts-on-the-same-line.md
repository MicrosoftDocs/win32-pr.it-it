---
description: Stili di tipi diversi all'interno di una famiglia di caratteri possono avere larghezze diverse.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Disegno di testo da diversi tipi di carattere nella stessa riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226699"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="256c7-103">Disegno di testo da diversi tipi di carattere nella stessa riga</span><span class="sxs-lookup"><span data-stu-id="256c7-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="256c7-104">Stili di tipi diversi all'interno di una famiglia di caratteri possono avere larghezze diverse.</span><span class="sxs-lookup"><span data-stu-id="256c7-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="256c7-105">Gli stili grassetto e corsivo di una famiglia, ad esempio, sono sempre più ampi dello stile Roman per le dimensioni del punto specificato.</span><span class="sxs-lookup"><span data-stu-id="256c7-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="256c7-106">Quando si visualizzano o stampano diversi stili di tipo su una sola riga, è necessario tenere traccia della larghezza della riga per evitare che i caratteri vengano visualizzati o stampati uno sopra l'altro.</span><span class="sxs-lookup"><span data-stu-id="256c7-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="256c7-107">È possibile usare due funzioni per recuperare la larghezza (o l'extent) del testo nel tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="256c7-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="256c7-108">La funzione [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcola la larghezza e l'altezza di una stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="256c7-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="256c7-109">Se la stringa contiene uno o più caratteri di tabulazione, la larghezza della stringa si basa su una matrice specificata di posizioni di interruzione di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="256c7-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="256c7-110">La funzione [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcola la larghezza e l'altezza di una riga di testo.</span><span class="sxs-lookup"><span data-stu-id="256c7-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="256c7-111">Quando necessario, il sistema sintetizza un tipo di carattere cambiando le bitmap dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="256c7-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="256c7-112">Per sintetizzare un carattere in un tipo di carattere in grassetto, il sistema disegna il carattere due volte: in corrispondenza del punto iniziale e di nuovo un pixel a destra del punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="256c7-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="256c7-113">Per sintetizzare un carattere in un tipo di carattere corsivo, il sistema disegna due righe di pixel nella parte inferiore della cella di caratteri, sposta il punto iniziale di un pixel a destra, disegna le due righe successive e continua fino a quando non viene disegnato il carattere.</span><span class="sxs-lookup"><span data-stu-id="256c7-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="256c7-114">Spostando i pixel, ogni carattere viene tagliato a destra.</span><span class="sxs-lookup"><span data-stu-id="256c7-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="256c7-115">La quantità di cesoia è una funzione dell'altezza del carattere.</span><span class="sxs-lookup"><span data-stu-id="256c7-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="256c7-116">Un modo per scrivere una riga di testo contenente più tipi di carattere consiste nell'usare la funzione [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) dopo ogni chiamata a [Text](/windows/desktop/api/Wingdi/nf-wingdi-textouta) out e aggiungere la lunghezza a una posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="256c7-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="256c7-117">Nell'esempio seguente viene scritta la riga "Questa è una stringa di esempio".</span><span class="sxs-lookup"><span data-stu-id="256c7-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="256c7-118">utilizzando caratteri in grassetto per "This is a", passa a caratteri italici per "Sample", quindi torna ai caratteri in grassetto per "String".</span><span class="sxs-lookup"><span data-stu-id="256c7-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="256c7-119">Una volta stampate tutte le stringhe, vengono ripristinati i caratteri predefiniti del sistema.</span><span class="sxs-lookup"><span data-stu-id="256c7-119">After printing all the strings, it restores the system default characters.</span></span>


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



<span data-ttu-id="256c7-120">In questo esempio, la funzione [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) Inizializza i membri di una struttura di [dimensioni](/previous-versions//dd145106(v=vs.85)) con la lunghezza e l'altezza della stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="256c7-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="256c7-121">La funzione [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera la sporgenza per il tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="256c7-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="256c7-122">Poiché la sporgenza è zero se il tipo di carattere è un tipo di carattere TrueType, il valore di sporgenza non modifica la posizione della stringa.</span><span class="sxs-lookup"><span data-stu-id="256c7-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="256c7-123">Per i tipi di carattere raster, tuttavia, è importante usare il valore di sporgenza.</span><span class="sxs-lookup"><span data-stu-id="256c7-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="256c7-124">La sporgenza viene sottratta dalla stringa in grassetto una volta, per portare i caratteri successivi alla fine della stringa se il tipo di carattere è un tipo di carattere raster.</span><span class="sxs-lookup"><span data-stu-id="256c7-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="256c7-125">Poiché la sporgenza interessa sia l'inizio che la fine della stringa in corsivo in un tipo di carattere raster, i glifi iniziano a destra della posizione specificata e terminano a sinistra dell'endpoint della cella dell'ultimo carattere.</span><span class="sxs-lookup"><span data-stu-id="256c7-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="256c7-126">La funzione [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera l'ambito delle celle di tipo carattere, non l'extent dei glifi. Per tenere conto della sporgenza nella stringa in corsivo raster, l'esempio sottrae la sporgenza prima di inserire la stringa e la sottrae prima di inserire i caratteri successivi.</span><span class="sxs-lookup"><span data-stu-id="256c7-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="256c7-127">La funzione [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) aggiunge ulteriore spazio ai caratteri break in una riga di testo.</span><span class="sxs-lookup"><span data-stu-id="256c7-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="256c7-128">È possibile utilizzare la funzione [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) per determinare l'estensione di una stringa, quindi sottrarla dalla quantità totale di spazio che la riga deve occupare e utilizzare la funzione [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) per distribuire lo spazio aggiuntivo tra i caratteri di interruzioni della stringa.</span><span class="sxs-lookup"><span data-stu-id="256c7-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="256c7-129">La funzione [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) aggiunge ulteriore spazio a ogni cella di caratteri nel tipo di carattere selezionato, incluso il carattere di rottura.</span><span class="sxs-lookup"><span data-stu-id="256c7-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="256c7-130">È possibile utilizzare la funzione [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) per determinare la quantità corrente di spazio aggiuntivo aggiunto alle celle di caratteri. l'impostazione predefinita è zero.</span><span class="sxs-lookup"><span data-stu-id="256c7-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="256c7-131">È possibile inserire caratteri con una maggiore precisione utilizzando la funzione [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) o [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) per recuperare le larghezze dei singoli caratteri in un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="256c7-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="256c7-132">La funzione [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) è più precisa della funzione [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , ma può essere utilizzata solo con i tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="256c7-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="256c7-133">La spaziatura ABC consente anche a un'applicazione di eseguire un allineamento del testo molto accurato.</span><span class="sxs-lookup"><span data-stu-id="256c7-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="256c7-134">Ad esempio, quando l'applicazione Allinea a destra un tipo di carattere raster Roman senza usare la spaziatura ABC, la larghezza di avanzamento viene calcolata come larghezza del carattere.</span><span class="sxs-lookup"><span data-stu-id="256c7-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="256c7-135">Ciò significa che gli spazi vuoti a destra del glifo nella bitmap sono allineati, non il glifo stesso.</span><span class="sxs-lookup"><span data-stu-id="256c7-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="256c7-136">Con le larghezze ABC, le applicazioni hanno maggiore flessibilità nel posizionamento e nella rimozione di spazi vuoti durante l'allineamento del testo, perché contengono informazioni che consentono loro di controllare con precisione la spaziatura tra i caratteri.</span><span class="sxs-lookup"><span data-stu-id="256c7-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
