---
title: Uso di stili di visualizzazione con controlli personalizzati e Owner-Drawn
description: Questo argomento descrive come usare l'API degli stili di visualizzazione per applicare gli stili di visualizzazione ai controlli personalizzati o ai controlli creati dal proprietario.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118546"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="7c94e-103">Uso di stili di visualizzazione con controlli personalizzati e Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="7c94e-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="7c94e-104">Questo argomento descrive come usare l'API degli stili di visualizzazione per applicare gli stili di visualizzazione ai controlli personalizzati o ai controlli creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7c94e-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="7c94e-105">Disegno di controlli con stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="7c94e-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="7c94e-106">Risposta alle modifiche del tema</span><span class="sxs-lookup"><span data-stu-id="7c94e-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="7c94e-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c94e-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="7c94e-108">Disegno di controlli con stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="7c94e-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="7c94e-109">Gli stili di visualizzazione sono supportati da ComCtrl32.dll versione 6 e successive.</span><span class="sxs-lookup"><span data-stu-id="7c94e-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="7c94e-110">Se l'applicazione è configurata per l'uso ComCtrl32.dll versione 6 e successive e se tale versione è disponibile nel sistema, gli stili di visualizzazione correnti vengono applicati automaticamente a tutti i controlli comuni nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c94e-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="7c94e-111">Gli stili di visualizzazione correnti, tuttavia, non vengono applicati automaticamente ai controlli personalizzati o ai controlli creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7c94e-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="7c94e-112">L'applicazione deve includere codice che controlla se gli stili di visualizzazione sono disponibili e, in caso affermativo, usa l'API stili di visualizzazione per applicare gli stili di visualizzazione attualmente selezionati ai controlli personalizzati e creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7c94e-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="7c94e-113">Per controllare se sono disponibili gli stili di visualizzazione, chiamare la funzione [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) .</span><span class="sxs-lookup"><span data-stu-id="7c94e-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="7c94e-114">Se gli stili di visualizzazione non sono disponibili, usare il codice di fallback per disegnare il controllo.</span><span class="sxs-lookup"><span data-stu-id="7c94e-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="7c94e-115">Se gli stili di visualizzazione sono disponibili, è possibile usare funzioni degli stili visivi, ad esempio [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , per eseguire il rendering del controllo.</span><span class="sxs-lookup"><span data-stu-id="7c94e-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="7c94e-116">Si noti che [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) consente di personalizzare l'aspetto del testo, mantenendo alcune proprietà del tipo di carattere del tema durante la modifica di altre.</span><span class="sxs-lookup"><span data-stu-id="7c94e-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="7c94e-117">**Per creare un controllo nello stile di visualizzazione corrente**</span><span class="sxs-lookup"><span data-stu-id="7c94e-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="7c94e-118">Chiamare [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passando l' *HWND* del controllo a cui si vogliono applicare gli stili di visualizzazione e un elenco di classi che descrive il tipo del controllo.</span><span class="sxs-lookup"><span data-stu-id="7c94e-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="7c94e-119">Le classi sono definite in Vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="7c94e-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="7c94e-120">**OpenThemeData** restituisce un handle hTheme, ma se il gestore degli stili di visualizzazione è disabilitato o lo stile di visualizzazione corrente non fornisce informazioni specifiche per un determinato controllo, la funzione restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="7c94e-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="7c94e-121">Se il valore restituito è **null**, usare le funzioni di disegno di stili non visivi.</span><span class="sxs-lookup"><span data-stu-id="7c94e-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="7c94e-122">Per creare lo sfondo del controllo, chiamare [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) o [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span><span class="sxs-lookup"><span data-stu-id="7c94e-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="7c94e-123">Per determinare la posizione del rettangolo di contenuto, chiamare [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="7c94e-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="7c94e-124">Per eseguire il rendering del testo, usare [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) o [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basandone le coordinate sul rettangolo restituito da [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="7c94e-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="7c94e-125">Queste funzioni possono eseguire il rendering del testo nel tipo di carattere per una parte del controllo e uno stato specificati oppure nel tipo di carattere attualmente selezionato nel contesto di periferica (DC).</span><span class="sxs-lookup"><span data-stu-id="7c94e-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="7c94e-126">Quando il controllo riceve un messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , chiamare [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) per rilasciare l'handle del tema restituito quando è stato chiamato [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="7c94e-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="7c94e-127">Nell'esempio di codice riportato di seguito viene illustrato un modo per creare un controllo Button nello stile di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="7c94e-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





<span data-ttu-id="7c94e-128">Il codice di esempio seguente si trova nel gestore di messaggi di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) per un controllo Button sottoclassato.</span><span class="sxs-lookup"><span data-stu-id="7c94e-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="7c94e-129">Il testo per il controllo viene disegnato nel tipo di carattere degli stili di visualizzazione, ma il colore è definito dall'applicazione a seconda dello stato del controllo.</span><span class="sxs-lookup"><span data-stu-id="7c94e-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



<span data-ttu-id="7c94e-130">È possibile usare parti di altri controlli ed eseguire il rendering separatamente di ogni parte.</span><span class="sxs-lookup"><span data-stu-id="7c94e-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="7c94e-131">Per un controllo calendario costituito da una griglia, ad esempio, è possibile considerare ogni quadrato formato dalla griglia come pulsante della barra degli strumenti, ottenendo l'handle del tema come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="7c94e-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="7c94e-132">È possibile combinare e associare le parti di controllo chiamando [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) più volte per un determinato controllo e usando l'handle del tema appropriato per creare parti diverse.</span><span class="sxs-lookup"><span data-stu-id="7c94e-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="7c94e-133">In alcuni stili visivi, tuttavia, alcune parti potrebbero non essere compatibili con altre parti.</span><span class="sxs-lookup"><span data-stu-id="7c94e-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="7c94e-134">Un altro approccio per il rendering dei controlli nello stile di visualizzazione attivo consiste nell'utilizzo dei colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="7c94e-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="7c94e-135">È ad esempio possibile utilizzare i colori di sistema per impostare il colore del testo quando si chiama la funzione [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="7c94e-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="7c94e-136">La maggior parte dei colori di sistema viene impostata quando viene applicato un file di stile di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7c94e-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="7c94e-137">Risposta alle modifiche del tema</span><span class="sxs-lookup"><span data-stu-id="7c94e-137">Responding to Theme Changes</span></span>

<span data-ttu-id="7c94e-138">Quando il controllo riceve un messaggio [**WM \_ THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) e mantiene un handle globale per il tema, deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c94e-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="7c94e-139">Chiamare [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) per chiudere l'handle del tema esistente.</span><span class="sxs-lookup"><span data-stu-id="7c94e-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="7c94e-140">Chiamare [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) per ottenere l'handle del tema per lo stile di visualizzazione appena caricato.</span><span class="sxs-lookup"><span data-stu-id="7c94e-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="7c94e-141">Nell'esempio seguente vengono illustrate le due chiamate.</span><span class="sxs-lookup"><span data-stu-id="7c94e-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="7c94e-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c94e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c94e-143">Abilitazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="7c94e-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="7c94e-144">Stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="7c94e-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 