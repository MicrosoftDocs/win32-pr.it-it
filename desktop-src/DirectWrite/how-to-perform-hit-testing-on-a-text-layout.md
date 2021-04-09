---
title: Come eseguire l'hit testing in un layout di testo
description: Viene fornita una breve esercitazione su come aggiungere l'hit test a un'applicazione DirectWrite che Visualizza il testo tramite l'interfaccia IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103968986"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Come eseguire l'hit testing in un layout di testo

Viene fornita una breve esercitazione su come aggiungere l'hit test a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo tramite l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Il risultato di questa esercitazione è un'applicazione che sottolinea il carattere su cui si fa clic con il pulsante sinistro del mouse, come illustrato nello screenshot seguente.

![Screenshot di "fare clic su questo testo"](images/hittest.png)

Questa procedura include le parti seguenti:

- [Passaggio 1: creare un layout di testo.](#step-1-create-a-text-layout)
- [Passaggio 2: aggiungere un metodo OnClick.](#step-2-add-an-onclick-method)
- [Passaggio 3: eseguire l'hit testing.](#step-3-perform-hit-testing)
- [Passaggio 4: sottolineare il testo selezionato.](#step-4-underline-the-clicked-text)
- [Passaggio 5: gestire il \_ messaggio WM LBUTTONDOWN.](/windows)

## <a name="step-1-create-a-text-layout"></a>Passaggio 1: creare un layout di testo.

Per iniziare, sarà necessaria un'applicazione che usi un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Se è già presente un'applicazione che visualizza testo con un layout di testo, andare al passaggio 2.

Per aggiungere un layout di testo è necessario eseguire le operazioni seguenti:

1. Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe.

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. Alla fine del metodo **CreateDeviceIndependentResources** , creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .

    ```cpp
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    ```

3. Quindi, è necessario modificare la chiamata al metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) come illustrato nel codice seguente.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Passaggio 2: aggiungere un metodo OnClick.

A questo punto, aggiungere un metodo alla classe che utilizzerà la funzionalità di hit testing del layout di testo.

1. Dichiarare un metodo **OnClick** nel file di intestazione della classe.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Definire un metodo **OnClick** nel file di implementazione della classe.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Passaggio 3: eseguire l'hit testing.

Per determinare la posizione in cui l'utente ha fatto clic sul layout del testo, viene usato il metodo [**IDWriteTextLayout:: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

Aggiungere quanto segue al metodo **OnClick** definito nel passaggio 2.

1. Dichiarare le variabili che vengono passate come parametri al metodo.

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    Il metodo [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) restituisce i parametri seguenti.

    | Variabile         | Descrizione                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | Geometria che racchiude completamente il percorso di hit test.                                                                                     |
    | *Interno*       | Indica se il percorso di hit test si trova all'interno della stringa di testo. Se è FALSE, viene restituita la posizione più vicina al bordo del testo. |
    | *isTrailingHit*  | Indica se il percorso di hit test si trova al lato principale o finale del carattere.                                        |

2. Chiamare il metodo [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) dell'oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    Il codice in questo esempio passa le variabili *x* e *y* per la posizione senza alcuna modifica. Questa operazione può essere eseguita in questo esempio perché il layout del testo ha le stesse dimensioni della finestra e ha origine nell'angolo superiore sinistro della finestra. In caso contrario, è necessario determinare le coordinate in relazione all'origine del layout del testo.

## <a name="step-4-underline-the-clicked-text"></a>Passaggio 4: sottolineare il testo selezionato.

Aggiungere quanto segue all'oggetto **OnClick** definito nel passaggio 2, dopo la chiamata al metodo [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Questo codice esegue le operazioni seguenti.

1. Controlla se il punto di hit test si trova all'interno del testo utilizzando la variabile *Inside* .
2. Il membro **TextPosition** della struttura *hitTestMetrics* contiene l'indice in base zero del carattere selezionato.

    Ottiene la sottolineatura per questo carattere passando questo valore al metodo [**IDWriteTextLayout:: getunderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .

3. Dichiara una variabile [**di \_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) con la posizione iniziale impostata su **hitTestMetrics. TextPosition** e una lunghezza pari a 1.
4. Consente di abilitare o disabilitare la sottolineatura utilizzando il metodo [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) SetValue.

Dopo aver impostato la sottolineatura, ricreare il testo chiamando il metodo **DrawD2DContent** della classe.

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Passaggio 5: gestire il \_ messaggio WM LBUTTONDOWN.

Infine, aggiungere il messaggio **WM \_ LBUTTONDOWN** al gestore di messaggi per l'applicazione e chiamare il metodo **OnClick** della classe.

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**Ottenere \_ Le macro x \_ lParam** e **get \_ x \_ lParam** sono dichiarate nel file di intestazione windowsx. h. Consentono di recuperare facilmente la posizione x e y del clic del mouse.
