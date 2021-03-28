---
description: In alcuni casi, un'applicazione deve essere in grado di enumerare i tipi di carattere disponibili e selezionare quella più appropriata per una determinata operazione.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Enumerazione dei tipi di carattere installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226697"
---
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="26a81-103">Enumerazione dei tipi di carattere installati</span><span class="sxs-lookup"><span data-stu-id="26a81-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="26a81-104">In alcuni casi, un'applicazione deve essere in grado di enumerare i tipi di carattere disponibili e selezionare quella più appropriata per una determinata operazione.</span><span class="sxs-lookup"><span data-stu-id="26a81-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="26a81-105">Un'applicazione può enumerare i tipi di carattere disponibili chiamando la funzione [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) o [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) .</span><span class="sxs-lookup"><span data-stu-id="26a81-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="26a81-106">Queste funzioni inviano informazioni sui tipi di carattere disponibili a una funzione di callback fornita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26a81-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="26a81-107">La funzione di callback riceve informazioni nelle strutture [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) e [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="26a81-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="26a81-108">La struttura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contiene informazioni su un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="26a81-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="26a81-109">Quando la funzione di callback riceve informazioni su un tipo di carattere non TrueType, le informazioni sono contenute in una struttura [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Utilizzando queste informazioni, un'applicazione può limitare le scelte dell'utente solo ai tipi di carattere disponibili.</span><span class="sxs-lookup"><span data-stu-id="26a81-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="26a81-110">La funzione [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) è simile alla funzione [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) ma include alcune funzionalità aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="26a81-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="26a81-111">**EnumFontFamilies** consente a un'applicazione di sfruttare gli stili disponibili con i tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="26a81-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="26a81-112">Le applicazioni nuove e aggiornate devono usare **EnumFontFamilies** anziché **EnumFonts**.</span><span class="sxs-lookup"><span data-stu-id="26a81-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="26a81-113">I tipi di carattere TrueType sono organizzati intorno a un nome di carattere tipografico (ad esempio, Courier New) e nomi di stile, ad esempio corsivo, grassetto e in grassetto.</span><span class="sxs-lookup"><span data-stu-id="26a81-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="26a81-114">La funzione [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) enumera tutti gli stili associati a un nome di famiglia specificato, non semplicemente gli attributi grassetto e corsivo.</span><span class="sxs-lookup"><span data-stu-id="26a81-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="26a81-115">Ad esempio, quando il sistema include un tipo di carattere TrueType denominato Courier New Extra Bold, **EnumFontFamilies** lo elenca con gli altri tipi di carattere Courier New.</span><span class="sxs-lookup"><span data-stu-id="26a81-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="26a81-116">Le funzionalità di **EnumFontFamilies** sono utili per i tipi di carattere con stili diversi o insoliti e per i tipi di carattere che superano i confini internazionali.</span><span class="sxs-lookup"><span data-stu-id="26a81-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="26a81-117">Se un'applicazione non fornisce un nome di carattere tipografico, le funzioni [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) forniscono informazioni su un tipo di carattere in ogni famiglia disponibile.</span><span class="sxs-lookup"><span data-stu-id="26a81-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="26a81-118">Per enumerare tutti i tipi di carattere in un contesto di dispositivo, l'applicazione può specificare **null** per il nome del carattere tipografico, compilare un elenco dei caratteri tipografici disponibili e quindi enumerare ogni carattere in ogni carattere tipografico.</span><span class="sxs-lookup"><span data-stu-id="26a81-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="26a81-119">Nell'esempio seguente viene usata la funzione [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) per recuperare il numero di famiglie di tipi di carattere raster, Vector e TrueType disponibili.</span><span class="sxs-lookup"><span data-stu-id="26a81-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



<span data-ttu-id="26a81-120">Questo esempio usa due maschere, \_ FONTTYPE raster e \_ FONTTYPE TrueType, per determinare il tipo di carattere enumerato.</span><span class="sxs-lookup"><span data-stu-id="26a81-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="26a81-121">Se \_ è impostato il bit FONTTYPE raster, il tipo di carattere è un tipo di carattere raster.</span><span class="sxs-lookup"><span data-stu-id="26a81-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="26a81-122">Se \_ è impostato il bit FONTTYPE di TrueType, il tipo di carattere è un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="26a81-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="26a81-123">Se non è impostato alcun bit, il tipo di carattere è un tipo di carattere vettoriale.</span><span class="sxs-lookup"><span data-stu-id="26a81-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="26a81-124">Una terza maschera, DEVICE \_ FONTTYPE, viene impostata quando un dispositivo (ad esempio, una stampante laser) supporta il download di tipi di carattere TrueType; è zero se il dispositivo è una scheda video, una stampante a matrice punto o un altro dispositivo raster.</span><span class="sxs-lookup"><span data-stu-id="26a81-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="26a81-125">Un'applicazione può anche usare il dispositivo \_ FONTTYPE mask per distinguere i tipi di carattere raster forniti da GDI dai tipi di carattere specificati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26a81-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="26a81-126">Il sistema è in grado di simulare gli attributi Bold, Italic, Underline e Strike per i tipi di carattere raster forniti da GDI, ma non per i tipi di carattere forniti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26a81-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="26a81-127">Un'applicazione può anche controllare BITS 1 e 2 nel membro **tmPitchAndFamily** della struttura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) per identificare un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="26a81-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="26a81-128">Se bit 1 è 0 e bit 2 è 1, il tipo di carattere è un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="26a81-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="26a81-129">I tipi di carattere vettoriali vengono categorizzati come \_ set di caratteri OEM anziché come set di caratteri ANSI \_ .</span><span class="sxs-lookup"><span data-stu-id="26a81-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="26a81-130">Alcune applicazioni identificano i tipi di carattere vettoriali usando queste informazioni, controllando il membro **tmCharSet** della struttura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="26a81-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="26a81-131">Questa categorizzazione in genere impedisce al mapper dei tipi di carattere di scegliere tipi di carattere vettoriali, a meno che non vengano richiesti specificamente.</span><span class="sxs-lookup"><span data-stu-id="26a81-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="26a81-132">(La maggior parte delle applicazioni non usa più tipi di carattere vettoriali perché i tratti sono singole righe e richiedono più tempo per disegnarli rispetto ai tipi di carattere TrueType, che offrono molte delle stesse funzionalità di ridimensionamento e rotazione necessarie per i tipi di carattere vettoriali).</span><span class="sxs-lookup"><span data-stu-id="26a81-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 
