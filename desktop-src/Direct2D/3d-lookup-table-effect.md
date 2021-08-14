---
title: Effetto tabella di ricerca 3D
description: Una tabella di ricerca 3D è un effetto generico usato per incapsulare qualsiasi effetto di creazione di immagini 11 pre-calcolando il modo in cui l'effetto esegue il mapping degli input agli output per un subset di tutti i valori di input.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b6d7cee4d21af5f7bc56ee4982f64523e892e616263b3cf5ed7ea84294fbb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161027"
---
# <a name="3d-lookup-table-effect"></a>Effetto tabella di ricerca 3D

Una tabella di ricerca 3D è un effetto generico usato per incapsulare qualsiasi effetto di creazione di immagini 1:1 pre-calcolando il modo in cui l'effetto esegue il mapping degli input agli output per un subset di tutti i valori di input.

L'effetto Tabella di ricerca 3D (LUT) modifica un'immagine di input usando il valore del colore RGB dell'immagine per indicizzare una trama 3D, in cui la trama contiene un valore di output pre-ricalcolato di una pipeline di effetti arbitrari.

L'LUT 3D deve essere caricato in una risorsa di trama GPU per poter essere sottoposto a rendering e questo può essere costoso a seconda delle dimensioni della trama e delle funzionalità del dispositivo. Gli sviluppatori di applicazioni possono specificare quando pagare questo costo usando la [**risorsa D2D ID2D1LookupTable3D.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) **ID2D1LookupTable3D** ha gli attributi seguenti:

-   Fornisce una rappresentazione astratta della risorsa GPU di 3D LUT.
-   A seconda delle funzionalità del dispositivo, verrà creata e riempita una trama 2D o 3D con i dati LUT forniti.
-   Può essere passato alla proprietà dell'effetto LUT 3D per il rendering.

Il CLSID per questo effetto è CLSID \_ D2D1LookupTable3D.

-   [Immagine di esempio](#example-image)
-   [Codice di esempio](#sample-code)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![Esempio di output dell'effetto](images/3dlookuptable-effect.png)

## <a name="sample-code"></a>Codice di esempio

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

## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto tabella di ricerca 3D sono definite dall'enumerazione [**D2D1 \_ LOOKUPTABLE3D \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
