---
title: Destinazioni di rendering, dispositivi e risorse
description: Destinazioni di rendering, dispositivi e risorse
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337199"
---
# <a name="render-targets-devices-and-resources"></a>Destinazioni di rendering, dispositivi e risorse

Una *destinazione di rendering* è semplicemente la posizione in cui verrà disegnato il programma. In genere, la destinazione di rendering è una finestra (in particolare, l'area client della finestra). Potrebbe anche essere una bitmap in memoria che non viene visualizzata. Una destinazione di rendering è rappresentata dall'interfaccia [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .

Un *dispositivo* è un'astrazione che rappresenta qualsiasi cosa disegna effettivamente i pixel. Un dispositivo hardware usa la GPU per ottenere prestazioni più veloci, mentre un dispositivo software usa la CPU. L'applicazione non crea il dispositivo. Al contrario, il dispositivo viene creato in modo implicito quando l'applicazione crea la destinazione di rendering. Ogni destinazione di rendering è associata a un particolare dispositivo, hardware o software.

![diagramma che mostra la relazione tra una destinazione di rendering e un dispositivo.](images/graphics09.png)

Una *risorsa* è un oggetto utilizzato dal programma per il disegno. Di seguito sono riportati alcuni esempi di risorse definite in Direct2D:

-   **Pennello**. Controlla il modo in cui vengono disegnate le linee e le aree. I tipi di pennelli includono pennelli a tinta unita e pennelli sfumatura.
-   **Stile tratto**. Controlla l'aspetto di una riga, ad esempio tratteggiata o a tinta unita.
-   **Geometria**. Rappresenta una raccolta di linee e curve.
-   **Mesh**. Forma composta da triangoli. I dati mesh possono essere utilizzati direttamente dalla GPU, a differenza dei dati geometry, che devono essere convertiti prima del rendering.

Anche le destinazioni di rendering sono considerate un tipo di risorsa.

Alcune risorse traggono vantaggio dall'accelerazione hardware. Una risorsa di questo tipo è sempre associata a un particolare dispositivo, ovvero hardware (GPU) o software (CPU). Questo tipo di risorsa viene definito *dipendente dal dispositivo*. I pennelli e le mesh sono esempi di risorse dipendenti dal dispositivo. Se il dispositivo diventa non disponibile, è necessario ricreare la risorsa per un nuovo dispositivo.

Le altre risorse vengono mantenute nella memoria della CPU, indipendentemente dal dispositivo usato. Queste risorse sono *indipendenti dal dispositivo*, perché non sono associate a un dispositivo specifico. Non è necessario ricreare risorse indipendenti dal dispositivo quando il dispositivo viene modificato. Gli stili e le geometrie del tratto sono risorse indipendenti dal dispositivo.

La documentazione MSDN relativa a ogni risorsa indica se la risorsa è dipendente dal dispositivo o indipendente dal dispositivo. Ogni tipo di risorsa è rappresentato da un'interfaccia che deriva da [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource). I pennelli, ad esempio, sono rappresentati dall'interfaccia [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .

## <a name="the-direct2d-factory-object"></a>Oggetto factory Direct2D

Il primo passaggio quando si utilizza Direct2D consiste nel creare un'istanza dell'oggetto factory Direct2D. Nella programmazione di computer, una *Factory* è un oggetto che crea altri oggetti. La factory Direct2D crea i tipi di oggetti seguenti:

-   Destinazioni di rendering.
-   Risorse indipendenti dal dispositivo, ad esempio stili di tratto e geometrie.

Le risorse dipendenti dal dispositivo, ad esempio pennelli e bitmap, vengono create dall'oggetto di destinazione di rendering.

![diagramma che mostra la factory Direct2D.](images/graphics10.png)

Per creare l'oggetto factory Direct2D, chiamare la funzione [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



Il primo parametro è un flag che specifica le opzioni di creazione. Il flag a **\_ \_ \_ \_ thread singolo di tipo Factory d2d1** significa che non si chiamerà Direct2D da più thread. Per supportare le chiamate da più thread, specificare **d2d1 \_ Factory di \_ tipo \_ multithread \_**. Se il programma usa un solo thread per chiamare Direct2D, l'opzione a thread singolo è più efficiente.

Il secondo parametro della funzione [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) riceve un puntatore all'interfaccia [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .

È necessario creare l'oggetto factory Direct2D prima del primo messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) . Il gestore di messaggi [**WM \_ create**](/windows/desktop/winmsg/wm-create) è una posizione ideale per creare la Factory:


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>Creazione di risorse Direct2D

Il programma Circle usa le risorse dipendenti dal dispositivo seguenti:

-   Destinazione di rendering associata alla finestra dell'applicazione.
-   Pennello a tinta unita per disegnare il cerchio.

Ognuna di queste risorse è rappresentata da un'interfaccia COM:

-   L'interfaccia [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) rappresenta la destinazione di rendering.
-   L'interfaccia [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) rappresenta il pennello.

Il programma Circle archivia i puntatori a queste interfacce come variabili membro della `MainWindow` classe:


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



Il codice seguente crea queste due risorse.


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



Per creare una destinazione di rendering per una finestra, chiamare il metodo [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) nella factory Direct2D.

-   Il primo parametro specifica le opzioni comuni a qualsiasi tipo di destinazione di rendering. In questo caso, vengono passate le opzioni predefinite chiamando la funzione helper [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).
-   Il secondo parametro specifica l'handle per la finestra più le dimensioni della destinazione di rendering, in pixel.
-   Il terzo parametro riceve un puntatore [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .

Per creare il pennello a tinta unita, chiamare il metodo [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) sulla destinazione di rendering. Il colore viene specificato come valore [**\_ \_ F del colore d2d1**](/windows/desktop/Direct2D/d2d1-color-f) . Per ulteriori informazioni sui colori in Direct2D, vedere [utilizzo del colore in Direct2D](using-color-in-direct2d.md).

Si noti inoltre che se la destinazione di rendering esiste già, il `CreateGraphicsResources` metodo **restituisce \_ OK** senza eseguire alcuna operazione. Il motivo di questa progettazione diventerà chiaro nell'argomento successivo.

## <a name="next"></a>Prossima

[Disegno con Direct2D](drawing-with-direct2d.md)

 

 