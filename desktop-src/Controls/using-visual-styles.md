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
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>Uso di stili di visualizzazione con controlli personalizzati e Owner-Drawn

Questo argomento descrive come usare l'API degli stili di visualizzazione per applicare gli stili di visualizzazione ai controlli personalizzati o ai controlli creati dal proprietario.

-   [Disegno di controlli con stili di visualizzazione](#drawing-controls-with-visual-styles)
-   [Risposta alle modifiche del tema](#responding-to-theme-changes)
-   [Argomenti correlati](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>Disegno di controlli con stili di visualizzazione

Gli stili di visualizzazione sono supportati da ComCtrl32.dll versione 6 e successive. Se l'applicazione è configurata per l'uso ComCtrl32.dll versione 6 e successive e se tale versione è disponibile nel sistema, gli stili di visualizzazione correnti vengono applicati automaticamente a tutti i controlli comuni nell'applicazione. Gli stili di visualizzazione correnti, tuttavia, non vengono applicati automaticamente ai controlli personalizzati o ai controlli creati dal proprietario. L'applicazione deve includere codice che controlla se gli stili di visualizzazione sono disponibili e, in caso affermativo, usa l'API stili di visualizzazione per applicare gli stili di visualizzazione attualmente selezionati ai controlli personalizzati e creati dal proprietario.

Per controllare se sono disponibili gli stili di visualizzazione, chiamare la funzione [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) . Se gli stili di visualizzazione non sono disponibili, usare il codice di fallback per disegnare il controllo.

Se gli stili di visualizzazione sono disponibili, è possibile usare funzioni degli stili visivi, ad esempio [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , per eseguire il rendering del controllo. Si noti che [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) consente di personalizzare l'aspetto del testo, mantenendo alcune proprietà del tipo di carattere del tema durante la modifica di altre.

**Per creare un controllo nello stile di visualizzazione corrente**

1.  Chiamare [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passando l' *HWND* del controllo a cui si vogliono applicare gli stili di visualizzazione e un elenco di classi che descrive il tipo del controllo. Le classi sono definite in Vssym32. h. **OpenThemeData** restituisce un handle hTheme, ma se il gestore degli stili di visualizzazione è disabilitato o lo stile di visualizzazione corrente non fornisce informazioni specifiche per un determinato controllo, la funzione restituisce **null**. Se il valore restituito è **null**, usare le funzioni di disegno di stili non visivi.
2.  Per creare lo sfondo del controllo, chiamare [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) o [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).
3.  Per determinare la posizione del rettangolo di contenuto, chiamare [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).
4.  Per eseguire il rendering del testo, usare [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) o [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basandone le coordinate sul rettangolo restituito da [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect). Queste funzioni possono eseguire il rendering del testo nel tipo di carattere per una parte del controllo e uno stato specificati oppure nel tipo di carattere attualmente selezionato nel contesto di periferica (DC).
5.  Quando il controllo riceve un messaggio [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , chiamare [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) per rilasciare l'handle del tema restituito quando è stato chiamato [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).

Nell'esempio di codice riportato di seguito viene illustrato un modo per creare un controllo Button nello stile di visualizzazione corrente.


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





Il codice di esempio seguente si trova nel gestore di messaggi di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) per un controllo Button sottoclassato. Il testo per il controllo viene disegnato nel tipo di carattere degli stili di visualizzazione, ma il colore è definito dall'applicazione a seconda dello stato del controllo.


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



È possibile usare parti di altri controlli ed eseguire il rendering separatamente di ogni parte. Per un controllo calendario costituito da una griglia, ad esempio, è possibile considerare ogni quadrato formato dalla griglia come pulsante della barra degli strumenti, ottenendo l'handle del tema come indicato di seguito:


```C++
OpenThemeData(hwnd, L"Toolbar");
```



È possibile combinare e associare le parti di controllo chiamando [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) più volte per un determinato controllo e usando l'handle del tema appropriato per creare parti diverse. In alcuni stili visivi, tuttavia, alcune parti potrebbero non essere compatibili con altre parti.

Un altro approccio per il rendering dei controlli nello stile di visualizzazione attivo consiste nell'utilizzo dei colori di sistema. È ad esempio possibile utilizzare i colori di sistema per impostare il colore del testo quando si chiama la funzione [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) . La maggior parte dei colori di sistema viene impostata quando viene applicato un file di stile di visualizzazione.

## <a name="responding-to-theme-changes"></a>Risposta alle modifiche del tema

Quando il controllo riceve un messaggio [**WM \_ THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) e mantiene un handle globale per il tema, deve eseguire le operazioni seguenti:

-   Chiamare [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) per chiudere l'handle del tema esistente.
-   Chiamare [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) per ottenere l'handle del tema per lo stile di visualizzazione appena caricato.

Nell'esempio seguente vengono illustrate le due chiamate.


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione degli stili di visualizzazione](cookbook-overview.md)
</dt> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> </dl>

 

 