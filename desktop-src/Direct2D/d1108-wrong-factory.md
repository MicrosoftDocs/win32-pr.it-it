---
title: D1108 Factory errata
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: La risorsa è stata allocata dalla factory 1 e usata con la factory 2.
keywords:
- D1108 Factory errato Direct2D
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 20021472467d7861aa2b9cabd5602b5a167f20ab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622157"
---
# <a name="d1108-wrong-factory"></a>D1108: Factory errata

La risorsa \[ *è stata* \] allocata dalla factory \[ *1* \] e usata con la factory \[ *2.* \]

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Risorsa*
</dt> <dd>

Indirizzo dell'interfaccia.

</dd> <dt>

<span id="factory_1"></span><span id="FACTORY_1"></span>*factory 1*
</dt> <dd>

Indirizzo della factory che ha allocato *la risorsa*.

</dd> <dt>

<span id="factory_2"></span><span id="FACTORY_2"></span>*factory 2*
</dt> <dd>

Indirizzo della factory con cui è *stata usata* la risorsa.

</dd> </dl> 




 

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono prima creati due oggetti [**ID2D1Factory abilitati**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) per il debug. crea quindi una geometria dalla prima factory e un pennello dalla seconda factory. Infine, chiama [**FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)passando la geometria e il pennello.


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif


        // Domain violation. Create a second Direct2D factory.
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory1
            );

        // Create a geometry from the second factory.
        hr = m_pD2DFactory1->CreateRectangleGeometry(
            D2D1::RectF(100, 50, 400, 160),
            &m_pRectangleGeometry
            );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        // Create a render target from the first factory.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
                &m_pBlackBrush
                );
        }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        m_pRenderTarget->FillGeometry(
            m_pRectangleGeometry,   //The rectangle geometry created from the second factory.
            m_pBlackBrush   //The black brush created from the first factory.
            );</code></pre></td>
</tr>
</tbody>
</table>



Questo esempio genera il messaggio di debug seguente:


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a>Possibili cause

Utilizzo delle risorse non valido. Una risorsa allocata da una factory è stata usata con un'altra factory.

 

 
