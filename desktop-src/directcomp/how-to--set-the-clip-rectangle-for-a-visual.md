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
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="c6775-103">Come eseguire il clip con un oggetto rettangolo clip</span><span class="sxs-lookup"><span data-stu-id="c6775-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="c6775-104">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c6775-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="c6775-105">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="c6775-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="c6775-106">In questo argomento viene illustrato come utilizzare un oggetto clip rettangolare per ritagliare una struttura ad albero visuale o visuale.</span><span class="sxs-lookup"><span data-stu-id="c6775-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="c6775-107">Nell'esempio riportato in questo argomento viene definita una clip rettangolare centrata sulla posizione del mouse e viene applicata la clip a un oggetto visivo centrato nell'area client della finestra di destinazione della composizione.</span><span class="sxs-lookup"><span data-stu-id="c6775-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="c6775-108">Questa schermata mostra il risultato dell'applicazione dell'oggetto di ritaglio rettangolo all'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="c6775-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![risultato dell'applicazione di un oggetto di ritaglio rettangolo a un oggetto visivo](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="c6775-110">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="c6775-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c6775-111">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="c6775-111">Technologies</span></span>

-   [<span data-ttu-id="c6775-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c6775-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="c6775-113">Grafica Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c6775-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="c6775-114">Infrastruttura grafica DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="c6775-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="c6775-115">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c6775-115">Prerequisites</span></span>

-   <span data-ttu-id="c6775-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="c6775-116">C/C++</span></span>
-   <span data-ttu-id="c6775-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="c6775-117">Microsoft Win32</span></span>
-   <span data-ttu-id="c6775-118">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="c6775-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="c6775-119">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c6775-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="c6775-120">Passaggio 1: inizializzare gli oggetti DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c6775-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="c6775-121">Creare l'oggetto dispositivo e l'oggetto di destinazione della composizione.</span><span class="sxs-lookup"><span data-stu-id="c6775-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="c6775-122">Creare un oggetto visivo, impostarne il contenuto e aggiungerlo alla struttura ad albero visuale.</span><span class="sxs-lookup"><span data-stu-id="c6775-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="c6775-123">Per ulteriori informazioni, vedere [come inizializzare DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="c6775-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="c6775-124">Passaggio 2: creare l'oggetto rettangolo clip</span><span class="sxs-lookup"><span data-stu-id="c6775-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="c6775-125">Usare il metodo [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) per creare un'istanza dell'oggetto rettangolo di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="c6775-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="c6775-126">Passaggio 3: impostare le proprietà dell'oggetto rettangolo clip</span><span class="sxs-lookup"><span data-stu-id="c6775-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="c6775-127">Chiamare i metodi dell'interfaccia [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) dell'oggetto clip Rectangle per impostare le proprietà del rettangolo di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="c6775-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="c6775-128">Nell'esempio seguente viene definito un rettangolo di ritaglio centrato attorno alla posizione corrente del mouse.</span><span class="sxs-lookup"><span data-stu-id="c6775-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="c6775-129">Le `m_offsetX` `m_offsetY` variabili membro e contengono i valori delle proprietà OffsetX e OffsetY dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="c6775-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


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



<span data-ttu-id="c6775-130">Si noti che l'interfaccia [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) include i metodi seguenti per la definizione di un rettangolo di ritaglio con angoli arrotondati:</span><span class="sxs-lookup"><span data-stu-id="c6775-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="c6775-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="c6775-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="c6775-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="c6775-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="c6775-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="c6775-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="c6775-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="c6775-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="c6775-135">Passaggio 4: impostare la proprietà clip dell'oggetto visivo</span><span class="sxs-lookup"><span data-stu-id="c6775-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="c6775-136">Usare il metodo [**IDCompositionVisual:: seclip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) per associare la proprietà clip dell'oggetto visivo all'oggetto rettangolo di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="c6775-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="c6775-137">Passaggio 5: eseguire il commit della composizione</span><span class="sxs-lookup"><span data-stu-id="c6775-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="c6775-138">Chiamare il metodo [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit del batch di comandi in Microsoft DirectComposition per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="c6775-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="c6775-139">Il risultato dell'applicazione del rettangolo di ritaglio viene visualizzato nella finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c6775-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="c6775-140">Passaggio 6: liberare gli oggetti DirectComposition</span><span class="sxs-lookup"><span data-stu-id="c6775-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="c6775-141">Assicurarsi di liberare l'oggetto di ritaglio rettangolo quando non è più necessario, nonché l'oggetto dispositivo, l'oggetto di destinazione composizione e tutti gli oggetti visivi.</span><span class="sxs-lookup"><span data-stu-id="c6775-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="c6775-142">Nell'esempio seguente viene chiamata la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="c6775-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="c6775-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6775-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6775-144">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="c6775-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 