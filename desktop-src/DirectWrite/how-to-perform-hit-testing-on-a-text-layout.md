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
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="89036-103">Come eseguire l'hit testing in un layout di testo</span><span class="sxs-lookup"><span data-stu-id="89036-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="89036-104">Viene fornita una breve esercitazione su come aggiungere l'hit test a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo tramite l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="89036-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="89036-105">Il risultato di questa esercitazione è un'applicazione che sottolinea il carattere su cui si fa clic con il pulsante sinistro del mouse, come illustrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="89036-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![Screenshot di "fare clic su questo testo"](images/hittest.png)

<span data-ttu-id="89036-107">Questa procedura include le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="89036-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="89036-108">Passaggio 1: creare un layout di testo.</span><span class="sxs-lookup"><span data-stu-id="89036-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="89036-109">Passaggio 2: aggiungere un metodo OnClick.</span><span class="sxs-lookup"><span data-stu-id="89036-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="89036-110">Passaggio 3: eseguire l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="89036-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="89036-111">Passaggio 4: sottolineare il testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="89036-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="89036-112">Passaggio 5: gestire il \_ messaggio WM LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="89036-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="89036-113">Passaggio 1: creare un layout di testo.</span><span class="sxs-lookup"><span data-stu-id="89036-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="89036-114">Per iniziare, sarà necessaria un'applicazione che usi un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="89036-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="89036-115">Se è già presente un'applicazione che visualizza testo con un layout di testo, andare al passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="89036-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="89036-116">Per aggiungere un layout di testo è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="89036-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="89036-117">Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe.</span><span class="sxs-lookup"><span data-stu-id="89036-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="89036-118">Alla fine del metodo **CreateDeviceIndependentResources** , creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="89036-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

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

3. <span data-ttu-id="89036-119">Quindi, è necessario modificare la chiamata al metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="89036-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="89036-120">Passaggio 2: aggiungere un metodo OnClick.</span><span class="sxs-lookup"><span data-stu-id="89036-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="89036-121">A questo punto, aggiungere un metodo alla classe che utilizzerà la funzionalità di hit testing del layout di testo.</span><span class="sxs-lookup"><span data-stu-id="89036-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="89036-122">Dichiarare un metodo **OnClick** nel file di intestazione della classe.</span><span class="sxs-lookup"><span data-stu-id="89036-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="89036-123">Definire un metodo **OnClick** nel file di implementazione della classe.</span><span class="sxs-lookup"><span data-stu-id="89036-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="89036-124">Passaggio 3: eseguire l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="89036-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="89036-125">Per determinare la posizione in cui l'utente ha fatto clic sul layout del testo, viene usato il metodo [**IDWriteTextLayout:: HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="89036-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="89036-126">Aggiungere quanto segue al metodo **OnClick** definito nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="89036-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="89036-127">Dichiarare le variabili che vengono passate come parametri al metodo.</span><span class="sxs-lookup"><span data-stu-id="89036-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="89036-128">Il metodo [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) restituisce i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="89036-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="89036-129">Variabile</span><span class="sxs-lookup"><span data-stu-id="89036-129">Variable</span></span>         | <span data-ttu-id="89036-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89036-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="89036-131">*hitTestMetrics*</span><span class="sxs-lookup"><span data-stu-id="89036-131">*hitTestMetrics*</span></span> | <span data-ttu-id="89036-132">Geometria che racchiude completamente il percorso di hit test.</span><span class="sxs-lookup"><span data-stu-id="89036-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="89036-133">*Interno*</span><span class="sxs-lookup"><span data-stu-id="89036-133">*isInside*</span></span>       | <span data-ttu-id="89036-134">Indica se il percorso di hit test si trova all'interno della stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="89036-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="89036-135">Se è FALSE, viene restituita la posizione più vicina al bordo del testo.</span><span class="sxs-lookup"><span data-stu-id="89036-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="89036-136">*isTrailingHit*</span><span class="sxs-lookup"><span data-stu-id="89036-136">*isTrailingHit*</span></span>  | <span data-ttu-id="89036-137">Indica se il percorso di hit test si trova al lato principale o finale del carattere.</span><span class="sxs-lookup"><span data-stu-id="89036-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="89036-138">Chiamare il metodo [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) dell'oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="89036-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="89036-139">Il codice in questo esempio passa le variabili *x* e *y* per la posizione senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="89036-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="89036-140">Questa operazione può essere eseguita in questo esempio perché il layout del testo ha le stesse dimensioni della finestra e ha origine nell'angolo superiore sinistro della finestra.</span><span class="sxs-lookup"><span data-stu-id="89036-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="89036-141">In caso contrario, è necessario determinare le coordinate in relazione all'origine del layout del testo.</span><span class="sxs-lookup"><span data-stu-id="89036-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="89036-142">Passaggio 4: sottolineare il testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="89036-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="89036-143">Aggiungere quanto segue all'oggetto **OnClick** definito nel passaggio 2, dopo la chiamata al metodo [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) .</span><span class="sxs-lookup"><span data-stu-id="89036-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="89036-144">Questo codice esegue le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="89036-144">This code does the following.</span></span>

1. <span data-ttu-id="89036-145">Controlla se il punto di hit test si trova all'interno del testo utilizzando la variabile *Inside* .</span><span class="sxs-lookup"><span data-stu-id="89036-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="89036-146">Il membro **TextPosition** della struttura *hitTestMetrics* contiene l'indice in base zero del carattere selezionato.</span><span class="sxs-lookup"><span data-stu-id="89036-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="89036-147">Ottiene la sottolineatura per questo carattere passando questo valore al metodo [**IDWriteTextLayout:: getunderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) .</span><span class="sxs-lookup"><span data-stu-id="89036-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="89036-148">Dichiara una variabile [**di \_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) con la posizione iniziale impostata su **hitTestMetrics. TextPosition** e una lunghezza pari a 1.</span><span class="sxs-lookup"><span data-stu-id="89036-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="89036-149">Consente di abilitare o disabilitare la sottolineatura utilizzando il metodo [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) SetValue.</span><span class="sxs-lookup"><span data-stu-id="89036-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="89036-150">Dopo aver impostato la sottolineatura, ricreare il testo chiamando il metodo **DrawD2DContent** della classe.</span><span class="sxs-lookup"><span data-stu-id="89036-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="89036-151">Passaggio 5: gestire il \_ messaggio WM LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="89036-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="89036-152">Infine, aggiungere il messaggio **WM \_ LBUTTONDOWN** al gestore di messaggi per l'applicazione e chiamare il metodo **OnClick** della classe.</span><span class="sxs-lookup"><span data-stu-id="89036-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="89036-153">**Ottenere \_ Le macro x \_ lParam** e **get \_ x \_ lParam** sono dichiarate nel file di intestazione windowsx. h.</span><span class="sxs-lookup"><span data-stu-id="89036-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="89036-154">Consentono di recuperare facilmente la posizione x e y del clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="89036-154">They easily retrieve the x and y position of the mouse click.</span></span>
