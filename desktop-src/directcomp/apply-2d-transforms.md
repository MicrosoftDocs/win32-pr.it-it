---
title: Come applicare le trasformazioni 2D
description: In questo argomento viene illustrato come applicare le trasformazioni 2D a un oggetto visivo tramite Microsoft DirectComposition.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- come applicare le trasformazioni DirectComposition 2D
- Trasformazioni 2D DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399519"
---
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="75009-105">Come applicare le trasformazioni 2D</span><span class="sxs-lookup"><span data-stu-id="75009-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="75009-106">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="75009-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="75009-107">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="75009-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="75009-108">In questo argomento viene illustrato come applicare le trasformazioni 2D a un oggetto visivo tramite Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="75009-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="75009-109">Nell'esempio riportato in questo argomento viene applicato un gruppo di trasformazioni che:</span><span class="sxs-lookup"><span data-stu-id="75009-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="75009-110">Ruotare l'oggetto visivo di 180 gradi.</span><span class="sxs-lookup"><span data-stu-id="75009-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="75009-111">Ridimensionare l'oggetto visivo fino a tre volte le dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="75009-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="75009-112">Trasla (sposta) l'oggetto visivo 150 pixel a destra della posizione originale.</span><span class="sxs-lookup"><span data-stu-id="75009-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="75009-113">Le schermate seguenti mostrano l'oggetto visivo prima e dopo l'applicazione delle trasformazioni 2D.</span><span class="sxs-lookup"><span data-stu-id="75009-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![risultato dell'applicazione di un gruppo di trasformazioni 2D a un oggetto visivo](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="75009-115">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="75009-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="75009-116">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="75009-116">Technologies</span></span>

-   [<span data-ttu-id="75009-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="75009-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="75009-118">Grafica Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="75009-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="75009-119">Infrastruttura grafica DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="75009-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="75009-120">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="75009-120">Prerequisites</span></span>

-   <span data-ttu-id="75009-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="75009-121">C/C++</span></span>
-   <span data-ttu-id="75009-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="75009-122">Microsoft Win32</span></span>
-   <span data-ttu-id="75009-123">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="75009-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="75009-124">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="75009-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="75009-125">Passaggio 1: inizializzare gli oggetti DirectComposition</span><span class="sxs-lookup"><span data-stu-id="75009-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="75009-126">Creare l'oggetto dispositivo e l'oggetto di destinazione della composizione.</span><span class="sxs-lookup"><span data-stu-id="75009-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="75009-127">Creare un oggetto visivo, impostarne il contenuto e aggiungerlo alla struttura ad albero visuale.</span><span class="sxs-lookup"><span data-stu-id="75009-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="75009-128">Per ulteriori informazioni, vedere [come inizializzare DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="75009-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="75009-129">Passaggio 2: creare la matrice del gruppo di trasformazione</span><span class="sxs-lookup"><span data-stu-id="75009-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="75009-130">Passaggio 3: creare gli oggetti Transform, impostarne le proprietà e aggiungerli alla matrice del gruppo Transform</span><span class="sxs-lookup"><span data-stu-id="75009-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="75009-131">Usare i metodi [**IDCompositionDevice:: CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)e [**:: CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) per creare gli oggetti Transform.</span><span class="sxs-lookup"><span data-stu-id="75009-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="75009-132">Utilizzare le funzioni membro delle interfacce [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)e [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) per impostare le proprietà delle trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="75009-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="75009-133">Copiare i puntatori dell'interfaccia di trasformazione nella matrice del gruppo di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="75009-133">Copy the transform interface pointers to the transform group array.</span></span>


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="75009-134">Passaggio 4: creare l'oggetto gruppo di trasformazione</span><span class="sxs-lookup"><span data-stu-id="75009-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="75009-135">Chiamare il metodo [**IDCompositionDevice:: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) per creare l'oggetto gruppo di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="75009-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="75009-136">Passaggio 5: applicare l'oggetto gruppo di trasformazione all'oggetto visivo</span><span class="sxs-lookup"><span data-stu-id="75009-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="75009-137">Usare il metodo [**IDCompositionVisual:: setransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) per associare la proprietà Transform dell'oggetto visivo all'oggetto gruppo Transform.</span><span class="sxs-lookup"><span data-stu-id="75009-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="75009-138">Passaggio 6: eseguire il commit della composizione</span><span class="sxs-lookup"><span data-stu-id="75009-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="75009-139">Chiamare il metodo [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) per eseguire il commit degli aggiornamenti nell'oggetto visivo in DirectComposition per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="75009-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="75009-140">Il risultato dell'applicazione del gruppo di trasformazioni 2D viene visualizzato nella finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="75009-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="75009-141">Passaggio 7: liberare gli oggetti DirectComposition</span><span class="sxs-lookup"><span data-stu-id="75009-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="75009-142">Assicurarsi di liberare il gruppo di oggetti trasformazione 2D quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="75009-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="75009-143">Nell'esempio seguente viene chiamata la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definita dall'applicazione per liberare gli oggetti Transform.</span><span class="sxs-lookup"><span data-stu-id="75009-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="75009-144">Ricordare anche di liberare l'oggetto dispositivo, l'oggetto di destinazione della composizione e gli oggetti visivi prima che l'applicazione venga chiusa.</span><span class="sxs-lookup"><span data-stu-id="75009-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="75009-145">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="75009-145">Complete example</span></span>


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="75009-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75009-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75009-147">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="75009-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 