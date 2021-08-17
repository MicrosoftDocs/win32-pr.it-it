---
title: Come ritagliare con un oggetto clip rettangolo
description: Questo argomento illustra come usare un oggetto clip rettangolo per ritagliare un oggetto visivo o una struttura ad albero visuale.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10386f3e99dead7fff04a57463c2ee753bd1d712e9a59e6b928136c32f25ae75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119100"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Come ritagliare con un oggetto clip rettangolo

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedere [Modernizzare l'app desktop usando il livello Visivo.](/windows/uwp/composition/visual-layer-in-desktop-apps)

Questo argomento illustra come usare un oggetto clip rettangolo per ritagliare un oggetto visivo o una struttura ad albero visuale.

L'esempio in questo argomento definisce un clip rettangolare centrato nella posizione del mouse e applica il clip a un oggetto visivo centrato nell'area client della finestra di destinazione della composizione. Questa schermata mostra il risultato dell'applicazione dell'oggetto clip rettangolo all'oggetto visivo.

![risultato dell'applicazione di un oggetto clip rettangolo a un oggetto visivo](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [DirectComposition](directcomposition-portal.md)
-   [Grafica Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX Graphic Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Microsoft Win32
-   Component Object Model (COM)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-initialize-directcomposition-objects"></a>Passaggio 1: Inizializzare oggetti DirectComposition

1.  Creare l'oggetto dispositivo e l'oggetto di destinazione della composizione.
2.  Creare un oggetto visivo, impostarne il contenuto e aggiungerlo alla struttura ad albero visuale.

Per altre informazioni, vedere [Come inizializzare DirectComposition.](initialize-directcomposition.md)

### <a name="step-2-create-the-rectangle-clip-object"></a>Passaggio 2: Creare l'oggetto clip rettangolo

Usare il [**metodo IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) per creare un'istanza dell'oggetto clip rettangolo.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Passaggio 3: Impostare le proprietà dell'oggetto clip rettangolo

Chiamare i metodi dell'interfaccia [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) dell'oggetto clip rettangolo per impostare le proprietà del rettangolo di ritaglio.

Nell'esempio seguente viene definito un rettangolo di ritaglio centrato intorno alla posizione corrente del mouse. Le `m_offsetX` variabili membro e contengono i valori delle proprietà `m_offsetY` OffsetX e OffsetY dell'oggetto visivo.


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



Si noti che [**l'interfaccia IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) include i metodi seguenti per definire un rettangolo di ritaglio con angoli arrotondati:

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Passaggio 4: Impostare la proprietà Clip dell'oggetto visivo

Usare il [**metodo IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) per associare la proprietà Clip dell'oggetto visivo all'oggetto clip rettangolo.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Passaggio 5: Eseguire il commit della composizione

Chiamare il [**metodo IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit del batch di comandi a Microsoft DirectComposition per l'elaborazione. Il risultato dell'applicazione del rettangolo di ritaglio viene visualizzato nella finestra di destinazione.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Passaggio 6: Liberare gli oggetti DirectComposition

Assicurarsi di liberare l'oggetto clip rettangolo quando non è più necessario, nonché l'oggetto dispositivo, l'oggetto di destinazione della composizione e tutti gli oggetti visivi. Nell'esempio seguente viene chiamata la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti DirectComposition.


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ritaglio](clipping.md)
</dt> </dl>

 

 