---
title: Come eseguire il clip con un oggetto rettangolo clip
description: In questo argomento viene illustrato come utilizzare un oggetto clip rettangolare per ritagliare una struttura ad albero visuale o visuale.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047574"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Come eseguire il clip con un oggetto rettangolo clip

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

In questo argomento viene illustrato come utilizzare un oggetto clip rettangolare per ritagliare una struttura ad albero visuale o visuale.

Nell'esempio riportato in questo argomento viene definita una clip rettangolare centrata sulla posizione del mouse e viene applicata la clip a un oggetto visivo centrato nell'area client della finestra di destinazione della composizione. Questa schermata mostra il risultato dell'applicazione dell'oggetto di ritaglio rettangolo all'oggetto visivo.

![risultato dell'applicazione di un oggetto di ritaglio rettangolo a un oggetto visivo](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [DirectComposition](directcomposition-portal.md)
-   [Grafica Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [Infrastruttura grafica DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Microsoft Win32
-   Component Object Model (COM)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-initialize-directcomposition-objects"></a>Passaggio 1: inizializzare gli oggetti DirectComposition

1.  Creare l'oggetto dispositivo e l'oggetto di destinazione della composizione.
2.  Creare un oggetto visivo, impostarne il contenuto e aggiungerlo alla struttura ad albero visuale.

Per ulteriori informazioni, vedere [come inizializzare DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-rectangle-clip-object"></a>Passaggio 2: creare l'oggetto rettangolo clip

Usare il metodo [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) per creare un'istanza dell'oggetto rettangolo di ritaglio.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Passaggio 3: impostare le proprietà dell'oggetto rettangolo clip

Chiamare i metodi dell'interfaccia [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) dell'oggetto clip Rectangle per impostare le proprietà del rettangolo di ritaglio.

Nell'esempio seguente viene definito un rettangolo di ritaglio centrato attorno alla posizione corrente del mouse. Le `m_offsetX` `m_offsetY` variabili membro e contengono i valori delle proprietà OffsetX e OffsetY dell'oggetto visivo.


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



Si noti che l'interfaccia [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) include i metodi seguenti per la definizione di un rettangolo di ritaglio con angoli arrotondati:

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Passaggio 4: impostare la proprietà clip dell'oggetto visivo

Usare il metodo [**IDCompositionVisual:: seclip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) per associare la proprietà clip dell'oggetto visivo all'oggetto rettangolo di ritaglio.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Passaggio 5: eseguire il commit della composizione

Chiamare il metodo [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit del batch di comandi in Microsoft DirectComposition per l'elaborazione. Il risultato dell'applicazione del rettangolo di ritaglio viene visualizzato nella finestra di destinazione.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Passaggio 6: liberare gli oggetti DirectComposition

Assicurarsi di liberare l'oggetto di ritaglio rettangolo quando non è più necessario, nonché l'oggetto dispositivo, l'oggetto di destinazione composizione e tutti gli oggetti visivi. Nell'esempio seguente viene chiamata la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti DirectComposition.


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

 

 