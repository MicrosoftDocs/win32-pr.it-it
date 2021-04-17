---
title: Panoramica dell'API di ingrandimento
description: Questo argomento descrive l'API di ingrandimento e spiega come usarlo in un'applicazione.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Ingrandimento
- applicazioni di ingrandimento schermo
- Ingrandimento
- elaborazione di immagini personalizzate
- Magnification.dll
- creazione di controlli Magnifier
- ingrandimento selettivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300038"
---
# <a name="magnification-api-overview"></a>Panoramica dell'API di ingrandimento

L'API di ingrandimento consente ai fornitori di Assistive Technology di sviluppare applicazioni di ingrandimento dello schermo eseguite in Microsoft Windows. Questo argomento descrive l'API di ingrandimento e spiega come usarlo in un'applicazione. Contiene le sezioni seguenti:

- [Per iniziare](#getting-started)
- [Concetti di base](#basic-concepts)
  - [Tipi di lente di ingrandimento](#types-of-magnifiers)
  - [Fattore di ingrandimento](#magnification-factor)
  - [Effetti colore](#color-effects)
  - [Rettangolo di origine](#source-rectangle)
  - [Elenco filtri](#filter-list)
  - [Trasformazione input](#input-transform)
  - [Cursore di sistema](#system-cursor)
- [Inizializzazione della libreria di runtime della lente di ingrandimento](#initializing-the-magnifier-run-time-library)
- [Uso di Full-Screen Magnifier](#using-the-full-screen-magnifier)
- [Uso del controllo Magnifier](#using-the-magnifier-control)
  - [Creazione del controllo Magnifier](#creating-the-magnifier-control)
  - [Inizializzazione del controllo](#initializing-the-control)
  - [Impostazione del rettangolo di origine](#setting-the-source-rectangle)
  - [Applicazione degli effetti colore](#applying-color-effects)
  - [Ingrandimento selettivo](#selective-magnification)
- [Argomenti correlati](#related-topics)

## <a name="getting-started"></a>Introduzione

La versione originale dell'API di ingrandimento è supportata in Windows Vista e nei sistemi operativi successivi. In Windows 8 e versioni successive, l'API supporta funzionalità aggiuntive, tra cui l'ingrandimento a schermo intero e l'impostazione della visibilità del cursore di sistema ingrandito.

Il supporto per l'API di ingrandimento è fornito da Magnification.dll. Per compilare l'applicazione, includere ingrandimento. h e collegamento a ingrandimento. lib.

> [!Note]  
> L'API di ingrandimento non è supportata in WOW64; ovvero, un'applicazione di Magnifier a 32 bit non verrà eseguita correttamente in Windows a 64 bit.

## <a name="basic-concepts"></a>Concetti di base

Questa sezione descrive i concetti fondamentali su cui si basa l'API di ingrandimento. Contiene le parti seguenti:

- [Tipi di lente di ingrandimento](#types-of-magnifiers)
- [Fattore di ingrandimento](#magnification-factor)
- [Effetti colore](#color-effects)
- [Rettangolo di origine](#source-rectangle)
- [Elenco filtri](#filter-list)
- [Trasformazione input](#input-transform)
- [Cursore di sistema](#system-cursor)

### <a name="types-of-magnifiers"></a>Tipi di lente di ingrandimento

L'API supporta due tipi di lente di ingrandimento, il *Magnifier a schermo intero* e il *controllo lente di ingrandimento*. La lente di ingrandimento a schermo intero consente di ingrandire il contenuto dell'intero schermo, mentre il controllo Magnifier ingrandisce il contenuto di una particolare area dello schermo e visualizza il contenuto in una finestra. Per entrambe le lenti, le immagini e il testo sono ingranditi ed entrambi consentono di controllare la quantità di ingrandimento. È anche possibile applicare effetti cromatici al contenuto della schermata ingrandita, semplificando la visualizzazione per gli utenti che hanno difetti di colore o che necessitano di colori con un contrasto maggiore o minore.

> [!Important]  
> L'API di controllo Magnifier è disponibile in Windows Vista e nei sistemi operativi successivi, mentre l'API di ingrandimento a schermo intero è disponibile solo nei sistemi operativi Windows 8 e versioni successive.

### <a name="magnification-factor"></a>Fattore di ingrandimento

Sia il controllo Magnifier a schermo intero che il controllo Magnifier applicano una trasformazione di ridimensionamento per ingrandire il contenuto dello schermo. La quantità di ingrandimento applicata dalla trasformazione scala è detta *fattore di ingrandimento*. Viene espresso come valore a virgola mobile dove 1,0 corrisponde a nessun ingrandimento e i valori più grandi comportano una quantità di ingrandimento corrispondente. Ad esempio, il valore 1,5 rende il contenuto della schermata 50% più grande. Un fattore di ingrandimento inferiore a 1,0 non è valido.

### <a name="color-effects"></a>Effetti colore

Gli effetti cromatici si ottengono applicando una matrice di trasformazione dei colori 5 per 5 ai colori del contenuto della schermata ingrandita. La matrice determina le intensità dei componenti rosso, blu, verde e alfa del contenuto. Per ulteriori informazioni, vedere [utilizzo di una matrice di colori per trasformare un singolo colore](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) nella documentazione di Windows GDI+.

### <a name="source-rectangle"></a>Rettangolo di origine

La lente di ingrandimento a schermo intero applica la trasformazione scala e la trasformazione colore a tutto lo schermo. Il controllo Magnifier, invece, copia un'area dello schermo, denominata *rettangolo di origine*, in una bitmap fuori schermo. Successivamente, il controllo applica la trasformazione di ridimensionamento e la trasformazione del colore, se presente, alla bitmap fuori schermo. Infine, il controllo Visualizza la bitmap ridimensionata e con colore trasformato nella finestra di controllo lente di ingrandimento.

### <a name="filter-list"></a>Elenco filtri

Per impostazione predefinita, il controllo Magnifier ingrandisce tutte le finestre nel rettangolo di origine specificato. Tuttavia, fornendo un *elenco di filtri* per gli handle di finestra, è possibile controllare quali finestre sono incluse nel contenuto ingrandito e quali non lo sono. Per altre informazioni, vedere [ingrandimento selettivo](#selective-magnification).

La lente di ingrandimento a schermo intero non supporta un elenco di filtri; che ingrandisce sempre tutte le finestre sullo schermo.

### <a name="input-transform"></a>Trasformazione input

In genere, il contenuto della schermata ingrandita è "invisibile" all'input penna o tocco utente. Se, ad esempio, l'utente tocca l'immagine ingrandita di un controllo, il sistema non passa necessariamente l'input al controllo. Il sistema passa invece l'input a qualsiasi elemento, se presente, che si trova in corrispondenza delle coordinate dello schermo toccato sul desktop non ingrandito. La funzione [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) consente di specificare una *trasformazione di input* che esegue il mapping dello spazio delle coordinate del contenuto della schermata ingrandita allo spazio delle coordinate dello schermo effettivo (non ingrandito). In questo modo, il sistema può passare l'input penna o tocco immesso nel contenuto della schermata ingrandita all'elemento dell'interfaccia utente corretto sullo schermo.

> [!Note]  
> Il processo chiamante deve disporre dei privilegi UIAccess per impostare la trasformazione di input. Per ulteriori informazioni, vedere l'articolo relativo alle [considerazioni sulla sicurezza di automazione interfaccia utente](../uiauto-securityoverview.md) e [/MANIFESTUAC (incorporare informazioni sul controllo dell'account utente nel manifesto)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest)

### <a name="system-cursor"></a>Cursore di sistema

La funzione [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) consente di visualizzare o nascondere il cursore di sistema. Se si Visualizza il cursore di sistema quando la lente di ingrandimento a schermo intero è attiva, il cursore di sistema viene sempre ingrandito insieme al resto del contenuto dello schermo. Se si nasconde il cursore di sistema quando la lente di ingrandimento a schermo intero è attiva, il cursore di sistema non è visibile.

Con il controllo Magnifier, la funzione [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) Mostra o nasconde il cursore di sistema non ingrandito, ma non ha alcun effetto sul cursore di sistema ingrandito. La visibilità del cursore di sistema ingrandito varia a seconda che il controllo Magnifier abbia lo stile [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) . Se ha questo stile, il controllo Magnifier Visualizza il cursore di sistema ingrandito, insieme al contenuto della schermata ingrandita, ogni volta che il cursore di sistema immette il rettangolo di origine.

## <a name="initializing-the-magnifier-run-time-library"></a>Inizializzazione della libreria di runtime della lente di ingrandimento

Prima di poter chiamare qualsiasi altra funzione API Magnifier, è necessario creare e inizializzare gli oggetti di runtime della lente di ingrandimento chiamando la funzione [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) . Analogamente, dopo aver completato l'utilizzo dell'API Magnifier, chiamare la funzione [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) per eliminare gli oggetti di runtime della lente di ingrandimento e liberare le risorse di sistema associate.

## <a name="using-the-full-screen-magnifier"></a>Uso di Full-Screen Magnifier

Per usare la funzione di ingrandimento a schermo intero, chiamare la funzione [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) . Il parametro *magLevel* specifica il fattore di ingrandimento. I parametri *xoffset* e *yoffset* specificano in che modo il contenuto della schermata ingrandita è posizionato rispetto allo schermo.

Quando il contenuto della schermata viene ingrandito, diventa più grande della schermata stessa. Una parte del contenuto si estende oltre i bordi dello schermo e diventa invisibile per l'utente. I parametri *xoffset* e *YOffset* della funzione [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) determinano quale parte del contenuto della schermata ingrandita viene visualizzata sullo schermo. Insieme, i parametri specificano le coordinate di un punto nel contenuto della schermata non ingrandita. Quando il contenuto viene ingrandito, viene posizionato con il punto specificato nell'angolo superiore sinistro dello schermo.

Nell'esempio seguente viene impostato il fattore di ingrandimento per il magnifier a schermo intero e il centro del contenuto della schermata ingrandita al centro dello schermo.

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

Usare la funzione [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) per applicare gli effetti dei colori al contenuto a schermo intero impostando una matrice di trasformazione dei colori definita dall'applicazione. Nell'esempio seguente viene impostata una matrice di trasformazione dei colori che converte i colori in scala di grigi.

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

È possibile recuperare il fattore di ingrandimento e i valori di offset correnti chiamando la funzione [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) . È possibile recuperare la matrice di trasformazione del colore corrente chiamando la funzione [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .

## <a name="using-the-magnifier-control"></a>Uso del controllo Magnifier

Il controllo Magnifier ingrandisce il contenuto di una particolare area dello schermo e visualizza il contenuto in una finestra. Questa sezione descrive come usare il controllo Magnifier. Contiene le parti seguenti:

- [Creazione del controllo Magnifier](#creating-the-magnifier-control)
- [Inizializzazione del controllo](#initializing-the-control)
- [Impostazione del rettangolo di origine](#setting-the-source-rectangle)
- [Applicazione degli effetti colore](#applying-color-effects)
- [Ingrandimento selettivo](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Creazione del controllo Magnifier

Il controllo Magnifier deve essere ospitato in una finestra creata con lo stile esteso [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) . Dopo aver creato la finestra host, chiamare [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) per impostare l'opacità della finestra host. La finestra host viene in genere impostata sull'opacità completa per impedire la visualizzazione del contenuto della schermata sottostante. Nell'esempio seguente viene illustrato come impostare la finestra host sull'opacità completa:

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Se si applica lo stile [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) alla finestra host, i clic del mouse vengono passati all'oggetto che si trova dietro la finestra host nella posizione del cursore del mouse. Tenere presente che, poiché la finestra host non elabora i clic del mouse, l'utente non sarà in grado di spostare o ridimensionare la finestra di ingrandimento tramite il mouse.

La classe Window della finestra di controllo Magnifier deve essere **WC_MAGNIFIER**. Se si applica lo stile [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , il controllo Magnifier include il cursore di sistema nel contenuto della schermata ingrandita e il cursore viene ingrandito insieme al contenuto dello schermo.

Dopo aver creato il controllo Magnifier, mantenerlo in modo che sia possibile passarlo ad altre funzioni.

Nell'esempio seguente viene illustrato come creare il controllo Magnifier.

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>Inizializzazione del controllo

Dopo aver creato il controllo Magnifier, è necessario chiamare la funzione [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) per specificare il fattore di ingrandimento. Si tratta semplicemente di specificare una matrice di

(*n*, 0,0, 0,0)

(0,0, *n*, 0,0)

(0,0, 0,0, 1,0)

dove *n* è il fattore di ingrandimento.

Nell'esempio seguente viene illustrato come impostare il fattore di ingrandimento per il controllo Magnifier.

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>Impostazione del rettangolo di origine

Quando l'utente sposta il cursore del mouse intorno allo schermo, l'applicazione chiama la funzione [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) per specificare la parte della schermata sottostante da ingrandire.

La funzione di esempio seguente calcola la posizione e le dimensioni del rettangolo di origine (in base alla posizione del mouse e alle dimensioni della finestra di ingrandimento divisa per il fattore di ingrandimento) e imposta di conseguenza il rettangolo di origine. La funzione centra anche l'area client della finestra host nella posizione del mouse. Questa funzione verrebbe chiamata a intervalli per aggiornare la finestra di ingrandimento.

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>Applicazione degli effetti colore

Un controllo Magnifier con lo stile [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) applica una matrice di trasformazione dei colori incorporata che inverte i colori del contenuto della schermata ingrandita. Nella figura seguente viene illustrato il contenuto della schermata in un controllo Magnifier con lo stile **MS_INVERTCOLORS** .

![screenshot del contenuto ingrandito con colori invertiti](images/color-inversion.png)

La funzione [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) consente di applicare altri effetti sui colori impostando una matrice di trasformazione dei colori definita dall'applicazione. La funzione seguente, ad esempio, imposta una matrice di trasformazione dei colori che converte i colori in scala di grigi.


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

Per ulteriori informazioni sul funzionamento delle trasformazioni dei colori, vedere [utilizzo di una matrice di colori per trasformare un singolo colore](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) nella documentazione di GDI+.

### <a name="selective-magnification"></a>Ingrandimento selettivo

Per impostazione predefinita, l'ingrandimento viene applicato a tutte le finestre diverse dalla finestra di ingrandimento. Per specificare le finestre da ingrandire, chiamare la funzione [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) . Questo metodo accetta un elenco di finestre da ingrandire o un elenco di finestre da escludere dall'ingrandimento.

## <a name="related-topics"></a>Argomenti correlati

[API Magnification](entry-magapi-sdk.md)