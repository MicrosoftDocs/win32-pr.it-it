---
title: Come eseguire l'hit testing su un layout di testo
description: Fornisce una breve esercitazione su come aggiungere hit testing a un'applicazione DirectWrite che visualizza testo usando l'interfaccia IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d42967b069a7a5008de75c1cecb453a6158857eb2b05d2dd0298584a67cef69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816571"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Come eseguire l'hit testing su un layout di testo

Viene fornita una breve esercitazione su come aggiungere hit testing a [un'DirectWrite](direct-write-portal.md) che visualizza testo usando l'interfaccia [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Il risultato di questa esercitazione è un'applicazione che sottolinea il carattere su cui viene fatto clic con il pulsante sinistro del mouse, come illustrato nello screenshot seguente.

![Screenshot di "fare clic su questo testo"](images/hittest.png)

Questa procedura contiene le parti seguenti:

- [Passaggio 1: Creare un layout di testo.](#step-1-create-a-text-layout)
- [Passaggio 2: Aggiungere un metodo OnClick.](#step-2-add-an-onclick-method)
- [Passaggio 3: Eseguire l'hit testing.](#step-3-perform-hit-testing)
- [Passaggio 4: Sottolineare il testo selezionato.](#step-4-underline-the-clicked-text)
- [Passaggio 5: Gestire il messaggio \_ WM LBUTTONDOWN.](/windows)

## <a name="step-1-create-a-text-layout"></a>Passaggio 1: Creare un layout di testo.

Per iniziare, è necessaria un'applicazione che usa un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Se si ha già un'applicazione che visualizza testo con un layout di testo, andare al passaggio 2.

Per aggiungere un layout di testo, è necessario eseguire le operazioni seguenti:

1. Dichiarare un puntatore a [**un'interfaccia IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe .

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. Alla fine del metodo **CreateDeviceIndependentResources** creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il [**metodo CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)

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

3. È quindi necessario modificare la chiamata al metodo [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) in [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) come illustrato nel codice seguente.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Passaggio 2: Aggiungere un metodo OnClick.

Aggiungere ora un metodo alla classe che userà la funzionalità di hit testing del layout di testo.

1. Dichiarare un **metodo OnClick** nel file di intestazione della classe.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Definire un **metodo OnClick** nel file di implementazione della classe.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Passaggio 3: Eseguire l'hit testing.

Per determinare dove l'utente ha fatto clic sul layout di testo, si userà il [**metodo IDWriteTextLayout::HitTestPoint.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

Aggiungere quanto segue al **metodo OnClick** definito nel passaggio 2.

1. Dichiarare le variabili che verranno passate come parametri al metodo .

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    Il [**metodo HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) restituisce i parametri seguenti.

    | Variabile         | Descrizione                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | Geometria che racchiude completamente la posizione dell'hit test.                                                                                     |
    | *isInside*       | Indica se la posizione dell'hit test si trova o meno all'interno della stringa di testo. Se FALSE, viene restituita la posizione più vicina al bordo del testo. |
    | *isTrailingHit*  | Indica se la posizione dell'hit test si trova all'inizio o al lato finale del carattere.                                        |

2. Chiamare il [**metodo HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) dell'oggetto [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    Il codice in questo esempio passa le *variabili x* *e y* per la posizione senza alcuna modifica. Questa operazione può essere eseguita in questo esempio perché il layout del testo ha le stesse dimensioni della finestra e ha origine nell'angolo superiore sinistro della finestra. In caso contrario, è necessario determinare le coordinate in relazione all'origine del layout di testo.

## <a name="step-4-underline-the-clicked-text"></a>Passaggio 4: Sottolineare il testo selezionato.

Aggiungere quanto segue **all'oggetto OnClick** definito nel passaggio 2, dopo la chiamata al [**metodo HitTestPoint.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

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

1. Controlla se il punto di hit test si trova all'interno del testo usando la *variabile isInside.*
2. Il **membro textPosition** della struttura *hitTestMetrics* contiene l'indice in base zero del carattere selezionato.

    Ottiene la sottolineatura per questo carattere passando questo valore al [**metodo IDWriteTextLayout::GetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline)

3. Dichiara una [**variabile DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) con la posizione iniziale impostata su **hitTestMetrics.textPosition** e una lunghezza pari a 1.
4. Attiva o disattiva la sottolineatura usando il [**metodo IDWriteTextLayout::SetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline)

Dopo aver impostato la sottolineatura, ridisegnare il testo chiamando il **metodo DrawD2DContent** della classe .

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Passaggio 5: Gestire il messaggio \_ WM LBUTTONDOWN.

Infine, aggiungere il **messaggio \_ WM LBUTTONDOWN** al gestore di messaggi per l'applicazione e chiamare il **metodo OnClick** della classe .

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**GET \_ Le macro \_ X LPARAM** **e GET X \_ \_ LPARAM** vengono dichiarate nel file di intestazione windowsx.h. Recuperano facilmente la posizione x e y del clic del mouse.
