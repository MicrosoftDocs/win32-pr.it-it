---
title: effetto tabella di ricerca 3D
description: Una tabella di ricerca 3D è un effetto generico che viene usato per incapsulare qualsiasi effetto di imaging 1 1, precalcolando il modo in cui l'effetto esegue il mapping degli input agli output per un subset di tutti i valori di input.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874653"
---
# <a name="3d-lookup-table-effect"></a><span data-ttu-id="eb521-103">effetto tabella di ricerca 3D</span><span class="sxs-lookup"><span data-stu-id="eb521-103">3D lookup table effect</span></span>

<span data-ttu-id="eb521-104">Una tabella di ricerca 3D è un effetto generico che viene usato per incapsulare qualsiasi effetto di imaging 1:1, precalcolando il modo in cui l'effetto esegue il mapping degli input agli output per un subset di tutti i valori di input.</span><span class="sxs-lookup"><span data-stu-id="eb521-104">A 3D look-up table is a general-purpose effect that is used to encapsulate any 1:1 imaging effect by pre-computing how the effect maps inputs to outputs for a subset of all input values.</span></span>

<span data-ttu-id="eb521-105">L'effetto della tabella di ricerca 3D (LUT) modifica un'immagine di input usando il valore di colore RGB dell'immagine per indicizzare una trama 3D, in cui la trama contiene un valore di output pre-calcolato di una pipeline di effetto arbitrario.</span><span class="sxs-lookup"><span data-stu-id="eb521-105">The 3D Lookup Table (LUT) effect modifies an input image by using the image's RGB color value to index a 3D texture, where the texture contains a precomputed output value of an arbitrary effect pipeline.</span></span>

<span data-ttu-id="eb521-106">Per poter eseguire il rendering, la LUT 3D deve essere caricata in una risorsa di trama GPU, che può essere costosa a seconda delle dimensioni della trama e delle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb521-106">The 3D LUT must be loaded into a GPU texture resource in order to be rendered, and this can be expensive depending on the size of the texture and the device capabilities.</span></span> <span data-ttu-id="eb521-107">Gli sviluppatori di applicazioni possono specificare quando pagare questo costo usando la risorsa [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D.</span><span class="sxs-lookup"><span data-stu-id="eb521-107">Application developers can specify when to pay this cost using the [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D resource.</span></span> <span data-ttu-id="eb521-108">**ID2D1LookupTable3D** ha gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb521-108">**ID2D1LookupTable3D** has the following attributes:</span></span>

-   <span data-ttu-id="eb521-109">Fornisce una rappresentazione astratta della risorsa GPU di LUT 3D.</span><span class="sxs-lookup"><span data-stu-id="eb521-109">Provides an abstracted representation of 3D LUT's GPU resource.</span></span>
-   <span data-ttu-id="eb521-110">A seconda delle funzionalità del dispositivo, una trama 2D o 3D verrà creata e compilata con i dati LUT specificati.</span><span class="sxs-lookup"><span data-stu-id="eb521-110">Depending on the device capabilities, either a 2D or 3D texture will be created and filled with the provided LUT data.</span></span>
-   <span data-ttu-id="eb521-111">Può essere passato alla proprietà dell'effetto LUT 3D per il rendering.</span><span class="sxs-lookup"><span data-stu-id="eb521-111">Can be passed to the 3D LUT effect's property for rendering.</span></span>

<span data-ttu-id="eb521-112">Il CLSID per questo effetto è CLSID \_ D2D1LookupTable3D.</span><span class="sxs-lookup"><span data-stu-id="eb521-112">The CLSID for this effect is CLSID\_D2D1LookupTable3D.</span></span>

-   [<span data-ttu-id="eb521-113">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="eb521-113">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="eb521-114">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="eb521-114">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="eb521-115">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="eb521-115">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="eb521-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb521-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="eb521-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb521-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="eb521-118">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="eb521-118">Example image</span></span>

![esempio di output di effetto](images/3dlookuptable-effect.png)

## <a name="sample-code"></a><span data-ttu-id="eb521-120">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="eb521-120">Sample code</span></span>

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a><span data-ttu-id="eb521-121">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="eb521-121">Effect properties</span></span>

<span data-ttu-id="eb521-122">Le proprietà per l'effetto della tabella di ricerca 3D sono definite dall'enumerazione [**d2d1 \_ LOOKUPTABLE3D \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) .</span><span class="sxs-lookup"><span data-stu-id="eb521-122">The properties for the 3D lookup table effect are defined by the [**D2D1\_LOOKUPTABLE3D\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb521-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb521-123">Requirements</span></span>



| <span data-ttu-id="eb521-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb521-124">Requirement</span></span> | <span data-ttu-id="eb521-125">Valore</span><span class="sxs-lookup"><span data-stu-id="eb521-125">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="eb521-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb521-126">Minimum supported client</span></span> | <span data-ttu-id="eb521-127">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="eb521-127">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="eb521-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb521-128">Minimum supported server</span></span> | <span data-ttu-id="eb521-129">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="eb521-129">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="eb521-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb521-130">Header</span></span>                   | <span data-ttu-id="eb521-131">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="eb521-131">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="eb521-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb521-132">Library</span></span>                  | <span data-ttu-id="eb521-133">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="eb521-133">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="eb521-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb521-134">Related topics</span></span>

* [<span data-ttu-id="eb521-135">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="eb521-135">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
