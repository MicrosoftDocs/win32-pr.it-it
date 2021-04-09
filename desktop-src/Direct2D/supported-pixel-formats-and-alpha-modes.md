---
title: Formati pixel e modalità alfa supportati
description: Vengono descritti i formati pixel e le modalità Alpha supportati da ogni tipo di destinazione di rendering.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D, formati pixel
- Direct2D, modalità Alpha
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9a3777cac7cc0a258002d1475fb7b1c6dd2546ca
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104118646"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formati pixel e modalità alfa supportati

Questo argomento descrive i formati pixel e le modalità Alpha supportati dalle varie parti di Direct2D, inclusi ogni tipo di destinazione di rendering, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)e [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource). Include le sezioni seguenti:

-   [Formati YUV supportati per l'origine immagine DXGI](#supported-yuv-formats-for-dxgi-image-source)
-   [Specifica di un formato pixel per una destinazione di rendering](#specifying-a-pixel-format-for-a-render-target)
-   [Formati supportati per ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Formati supportati per ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Formati supportati per la destinazione di rendering compatibile](#supported-formats-for-compatible-render-target)
-   [Formati supportati per la destinazione di rendering della superficie di DXGI](#supported-formats-for-dxgi-surface-render-target)
-   [Formati supportati per la destinazione di rendering bitmap WIC](#supported-formats-for-wic-bitmap-render-target)
-   [Formati supportati per ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Specifica di un formato pixel per un ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Formati WIC supportati](#supported-wic-formats)
-   [Uso di un formato non supportato](#using-an-unsupported-format)
-   [Informazioni sulle modalità Alpha](#about-alpha-modes)
    -   [Informazioni sulle modalità alfa premoltiplicata e retta](#about-premultiplied-and-straight-alpha-modes)
    -   [Differenze tra l'alfa lineare e quello premoltiplicato](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Modalità Alpha per le destinazioni di rendering](#alpha-mode-for-render-targets)
    -   [Modalità ClearType e Alpha](#cleartype-and-alpha-modes)
-   [Argomenti correlati](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Formati YUV supportati per l'origine immagine DXGI

Un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) è un provider astratto di pixel. È possibile crearne un'istanza da WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) o [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) supporta lo stesso set di formati di pixel e modalità Alpha di [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

Oltre a quanto sopra, un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) di cui viene creata un'istanza da [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) supporta anche alcuni formati YUV pixel, inclusi i dati planari suddivisi in più aree. Per ulteriori informazioni sui requisiti per ogni formato pixel, vedere [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) .



| Formato                    |
|---------------------------|
| \_formato DXGI \_ AYUV        |
| \_Formato DXGI \_ NV12        |
| \_Formato DXGI \_ YUY2        |
| \_Formato DXGI \_ p208        |
| \_Formato DXGI \_ V208        |
| \_Formato DXGI \_ V408        |
| DXGI \_ formato \_ R8 \_ UNORM   |
| \_Formato DXGI \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Specifica di un formato pixel per una destinazione di rendering

Quando si crea una destinazione di rendering, è necessario specificarne il formato pixel. Per specificare il formato pixel, è possibile usare una struttura di [**\_ \_ formato pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) per impostare il membro **PixelFormat** di una struttura delle [**proprietà della \_ \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) . Quindi passare la struttura al metodo Create appropriato, ad esempio [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

La struttura del [**\_ \_ formato pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) presenta due campi:

-   **Format**, un valore di [ \_ formato DXGI](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) che descrive le dimensioni e la disposizione dei canali in ogni pixel e
-   **alfa**, un valore in [**\_ \_ modalità Alpha d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) che descrive il modo in cui vengono interpretate le informazioni alfa.

Nell'esempio seguente viene creata una struttura di [**\_ \_ formato pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) che viene utilizzata per specificare il formato pixel e la modalità Alpha di un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



Destinazioni di rendering diverse supportano combinazioni di formato e modalità alfa diverse. Nelle sezioni seguenti sono elencate le combinazioni di formato e Alpha supportate da ogni destinazione di rendering.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Formati supportati per ID2D1HwndRenderTarget

I formati supportati per un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dipendono dal fatto che esegua il rendering utilizzando hardware o software o se Direct2D gestisce automaticamente la modalità di rendering per impostazione predefinita.

> [!Note]  
> È consigliabile usare [**DXGI \_ Format \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) come formato pixel per ottenere prestazioni migliori. Questa operazione è particolarmente utile per le destinazioni di rendering software. Le destinazioni del formato BGRA offrono prestazioni migliori rispetto ai formati RGBA.

 

Quando si crea un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), si usa la struttura delle [**\_ proprietà della \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) per specificare le opzioni di rendering. Le opzioni includono il formato pixel, come indicato nella sezione precedente. Il campo tipo di questa struttura consente di specificare se la destinazione di rendering viene sottoposta a rendering su hardware o software o se Direct2D deve determinare automaticamente la modalità di rendering.

Per abilitare Direct2D per determinare se la destinazione di rendering utilizza il rendering hardware o software, utilizzare l'impostazione [**\_ predefinita del \_ \_ tipo \_ di destinazione**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) di rendering d2d1.

La tabella seguente elenca i formati supportati per gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) creati usando l'impostazione [**predefinita del \_ \_ tipo di \_ \_ destinazione di rendering d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .



| Formato                        | Modalità Alpha                       |
|-------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_formato DXGI \_ sconosciuto         | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_formato DXGI \_ sconosciuto         | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_formato DXGI \_ sconosciuto         | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |



 

Per forzare la destinazione di rendering a usare il rendering hardware, usare l'impostazione [**\_ hardware del \_ \_ tipo \_ di destinazione**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) di rendering d2d1. La tabella seguente elenca i formati supportati per gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) che usano in modo esplicito il rendering hardware.



| Formato                        | Modalità Alpha                       |
|-------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_Formato DXGI \_ R8G8B8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ R8G8B8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ R8G8B8A8 \_ UNORM | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_formato DXGI \_ sconosciuto         | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_formato DXGI \_ sconosciuto         | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_formato DXGI \_ sconosciuto         | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |



 

Per forzare la destinazione di rendering a usare il rendering del software, usare l'impostazione [**software del tipo di \_ destinazione di rendering \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . La tabella seguente elenca i formati supportati per gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) che usano in modo esplicito il rendering software.



| Formato                        | Modalità Alpha                       |
|-------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_formato DXGI \_ sconosciuto         | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_formato DXGI \_ sconosciuto         | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_formato DXGI \_ sconosciuto         | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |



 

Indipendentemente dal fatto che [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) sia accelerato dall'hardware, il formato [DXGI formato \_ \_ sconosciuto](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il [ \_ formato DXGI \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) per impostazione predefinita e la modalità Alpha di d2d1 in modalità Alpha [**\_ \_ \_ sconosciuta**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa la **\_ \_ modalità \_** Alpha di d2d1 per impostazione predefinita.

## <a name="supported-formats-for-id2d1devicecontext"></a>Formati supportati per ID2D1DeviceContext

A partire da Windows 8, il [**contesto di dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) sfrutta i vantaggi di un maggior numero di [**formati Direct3D High Color, ad**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) esempio:

-   \_Formato DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Formato DXGI \_ R16G16B16A16 \_ UNORM
-   \_Formato DXGI \_ R16G16B16A16 \_ float
-   \_Formato DXGI \_ R32G32B32A32 \_ float

Usare il metodo [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) per verificare se un formato funziona in un particolare contesto di dispositivo. Questi formati possono anche funzionare in un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).

Questi formati sono in aggiunta ai formati supportati dall'interfaccia [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) in Windows 7. Per ulteriori informazioni, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md) .

## <a name="supported-formats-for-compatible-render-target"></a>Formati supportati per la destinazione di rendering compatibile

Una destinazione di rendering compatibile (un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) creato da uno dei metodi [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) eredita i formati supportati e le modalità Alpha della destinazione di rendering che l'ha creata. Una destinazione di rendering compatibile supporta inoltre le combinazioni di formato e di modalità Alpha seguenti, indipendentemente dal supporto del padre.



| Formato                  | Modalità Alpha                       |
|-------------------------|----------------------------------|
| \_Formato DXGI \_ a8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ a8 \_ UNORM | D2D1 \_ \_ modalità Alpha \_ lineare      |
| \_formato DXGI \_ sconosciuto   | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |



 

Il formato DXGI del formato [ \_ \_ sconosciuto](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il formato di destinazione di rendering padre per impostazione predefinita e la modalità alfa [**\_ \_ \_ sconosciuta in modalità Alpha d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa la modalità Alpha di **d2d1 \_ \_ \_ premoltiplicata** per impostazione predefinita.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formati supportati per la destinazione di rendering della superficie di DXGI

Una destinazione di rendering DXGI è un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creato da uno dei metodi [**ID2D1Factory:: CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) . Supporta le combinazioni di formato e modalità Alpha seguenti.



| Formato                        | Modalità Alpha                       |
|-------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ R8G8B8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ R8G8B8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ a8 \_ UNORM       | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ a8 \_ UNORM       | D2D1 \_ \_ modalità Alpha \_ lineare      |
| \_formato DXGI \_ sconosciuto         | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_formato DXGI \_ sconosciuto         | \_ \_ Ignora modalità Alpha \_ d2d1        |



 

> [!Note]  
> Il formato deve corrispondere al formato della superficie DXGI a cui disegna la destinazione di rendering della superficie di DXGI.

 

Il formato [DXGI \_ formato \_ sconosciuto](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il formato di superficie DXGI per impostazione predefinita. Non usare la modalità Alpha [**d2d1 in \_ modalità Alpha \_ \_ sconosciuta**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con una destinazione di rendering della superficie di dxgi. Non ha un valore predefinito e causerà l'esito negativo della creazione della destinazione di rendering della superficie di DXGI.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formati supportati per la destinazione di rendering bitmap WIC

Una destinazione di rendering bitmap WIC è un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creato da uno dei metodi [**ID2D1Factory:: CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) . Supporta le combinazioni di formato e modalità Alpha seguenti.



| Formato                        | Modalità Alpha                       |
|-------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_Formato DXGI \_ a8 \_ UNORM       | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ a8 \_ UNORM       | D2D1 \_ \_ modalità Alpha \_ lineare      |
| \_Formato DXGI \_ a8 \_ UNORM       | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_formato DXGI \_ sconosciuto         | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_formato DXGI \_ sconosciuto         | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_formato DXGI \_ sconosciuto         | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |



 

Il formato pixel della destinazione bitmap WIC deve corrispondere al formato pixel della bitmap WIC.

Il formato DXGI del formato [ \_ \_ sconosciuto](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il formato bitmap WIC per impostazione predefinita e la modalità alfa [**\_ \_ \_ sconosciuta in modalità Alpha d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa la modalità alpha bitmap di WIC per impostazione predefinita.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formati supportati per ID2D1DCRenderTarget

Un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) supporta le combinazioni di formato e modalità Alpha seguenti.



| Formato                        | Modalità Alpha                       |
|-------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1        |



 

Non usare il formato [DXGI in formato \_ \_ sconosciuto](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) o la modalità Alpha [**d2d1 in modalità Alpha \_ \_ \_ sconosciuta**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Non ha un valore predefinito e causerà l'esito negativo della creazione di **ID2D1DCRenderTarget** .

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Specifica di un formato pixel per un ID2D1Bitmap

In genere, gli oggetti [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) supportano i formati e le modalità Alpha seguenti (con alcune restrizioni, descritti nei paragrafi che seguono).



| Formato                                                      | Modalità Alpha                       |
|-------------------------------------------------------------|----------------------------------|
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM                               | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM                               | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_Formato DXGI \_ B8G8R8A8 \_ UNORM                               | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_Formato DXGI \_ a8 \_ UNORM                                     | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_Formato DXGI \_ a8 \_ UNORM                                     | D2D1 \_ \_ modalità Alpha \_ lineare      |
| \_Formato DXGI \_ a8 \_ UNORM                                     | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| \_formato DXGI \_ sconosciuto                                       | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| \_formato DXGI \_ sconosciuto                                       | \_ \_ Ignora modalità Alpha \_ d2d1        |
| \_formato DXGI \_ sconosciuto                                       | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| DXGI \_ Format \_ B8G8R8X8 \_ UNORM (solo Windows 8.1 e versioni successive, solo) | \_ \_ Ignora modalità Alpha \_ d2d1        |
| DXGI \_ Format \_ BC1 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| DXGI \_ Format \_ BC1 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_ \_ Ignora modalità Alpha \_ d2d1        |
| DXGI \_ Format \_ BC1 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| DXGI \_ Format \_ BC2 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| DXGI \_ Format \_ BC2 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_ \_ Ignora modalità Alpha \_ d2d1        |
| DXGI \_ Format \_ BC2 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |
| DXGI \_ Format \_ BC3 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_Modalità d2d1 \_ alfa \_ premoltiplicata |
| DXGI \_ Format \_ BC3 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_ \_ Ignora modalità Alpha \_ d2d1        |
| DXGI \_ Format \_ BC3 \_ UNORM (solo Windows 8.1 e versioni successive, solo)      | \_Modalità Alpha \_ d2d1 \_ sconosciuta       |



 

Quando si usa il metodo [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) , si usa il campo **PixelFormat** di una struttura di [**\_ \_ proprietà bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) per specificare il formato pixel della nuova destinazione di rendering. Deve corrispondere al formato pixel dell'origine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) .

Quando si usa il metodo [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) , si usa il campo **PixelFormat** di una struttura di [**\_ \_ proprietà bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (anziché il membro **PixelFormat** di una struttura delle [**\_ \_ \_ proprietà della destinazione di rendering d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) ) per specificare il formato pixel della nuova destinazione di rendering. Deve corrispondere al formato pixel dell'origine bitmap WIC.

> [!Note]  
> Per ulteriori informazioni sul supporto dei formati di pixel a blocchi compressi (BCn), vedere [compressione a blocchi](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formati WIC supportati

Quando si usa il metodo [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) per creare una bitmap da una bitmap WIC o quando si usa il metodo [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) con un [**IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock), l'origine WIC deve essere in un formato supportato da Direct2D.



| Formato WIC                     | Formato DXGI corrispondente     | Modalità Alpha corrispondente                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | \_Formato DXGI \_ a8 \_ UNORM       | D2D1 \_ \_ modalità Alpha \_ diretta o d2d1 \_ \_ modalità alfa \_ premoltiplicata |
| GUID \_ WICPixelFormat32bppPRGBA | \_Formato DXGI \_ R8G8B8A8 \_ UNORM | D2D1 \_ \_ modalità alfa \_ premoltiplicata o d2d1 \_ \_ modalità alfa \_ Ignora   |
| GUID \_ WICPixelFormat32bppBGR   | \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_ \_ Ignora modalità Alpha \_ d2d1                                       |
| GUID \_ WICPixelFormat32bppPBGRA | \_Formato DXGI \_ B8G8R8A8 \_ UNORM | \_Modalità d2d1 \_ alfa \_ premoltiplicata                                |



 

Per un esempio in cui viene illustrato come convertire una bitmap WIC in un formato supportato, vedere [come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Uso di un formato non supportato

L'uso di una combinazione diversa dai formati pixel e dalle modalità Alpha elencate nelle tabelle precedenti restituisce un [**\_ \_ \_ formato pixel non supportato D2DERR**](direct2d-error-codes.md) o un errore **\_ INVALIDARG** .

## <a name="about-alpha-modes"></a>Informazioni sulle modalità Alpha

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Informazioni sulle modalità alfa premoltiplicata e retta

L'enumerazione [**d2d1 \_ Alpha \_ mode**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indica se il canale alfa utilizza un valore alfa premoltiplicato, un Alpha retto o deve essere ignorato e considerato opaco. Con l'alfa dritto, il canale alfa indica un valore che corrisponde alla trasparenza di un colore.

I colori vengono sempre trattati come alfa dritti dai comandi e dai pennelli di disegno Direct2D, indipendentemente dal formato di destinazione.

Con l'alfa premoltiplicato, ogni canale di colore viene ridimensionato in base al valore alfa. In genere, nessun valore del canale di colore è maggiore del valore del canale alfa. Se il valore di un canale di colore in un formato premoltiplicato è maggiore del canale alfa, la combinazione di risorse standard per la fusione dei dati matematici crea una Blend additiva.

Il valore del canale alfa è lo stesso sia in alfa sia in quello premoltiplicato.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Differenze tra l'alfa lineare e quello premoltiplicato

Quando si descrive un colore RGBA usando un valore alfa dritto, il valore alfa del colore viene archiviato nel canale alfa. Ad esempio, per descrivere un colore rosso 60% opaco, utilizzare i valori seguenti: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). Il valore 255 indica il colore rosso completo e 153 (60% 255) indica che il colore deve avere un'opacità del 60%.

Quando si descrive un colore RGBA usando un valore alfa premoltiplicato, ogni colore viene moltiplicato per il valore alfa: (255 \* 0,6, 0 \* 0,6, 0 \* 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Indipendentemente dalla modalità Alpha della destinazione di rendering, i [**valori \_ \_ F dei colori d2d1**](d2d1-color-f.md) vengono sempre interpretati come caratteri alfa dritti. Ad esempio, quando si specifica il colore di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) da usare con una destinazione di rendering che usa la modalità alfa premoltiplicata, specificare il colore esattamente come se la destinazione di rendering avesse usato il valore alfa diretto. Quando si disegna con il pennello, Direct2D converte il colore nel formato di destinazione.

### <a name="alpha-mode-for-render-targets"></a>Modalità Alpha per le destinazioni di rendering

Indipendentemente dall'impostazione della modalità Alpha, il contenuto di una destinazione di rendering supporta la trasparenza. Se, ad esempio, si estrae un rettangolo rosso parzialmente trasparente con una destinazione di rendering con la modalità alfa d2d1, il rettangolo verrà visualizzato in rosa (se lo sfondo è bianco). [**\_ \_ \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)

Se si crea un rettangolo rosso parzialmente trasparente quando la modalità Alpha è [**\_ \_ \_ premoltiplicata**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)per la modalità Alpha d2d1, il rettangolo apparirà rosa (presupponendo che lo sfondo sia bianco) e sarà possibile visualizzarlo in qualsiasi altro oggetto dietro la destinazione di rendering. Questa operazione è utile quando si usa un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per eseguire il rendering in una finestra trasparente o quando si usa una destinazione di rendering compatibile (un rendering di destinazione creato dal metodo [**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) per creare una bitmap che supporta la trasparenza.

### <a name="cleartype-and-alpha-modes"></a>Modalità ClearType e Alpha

Se si specifica una modalità Alpha diversa da [**d2d1 \_ Alpha \_ mode \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) per una destinazione di rendering, la modalità di anti-aliasing del testo passa automaticamente dalla modalità [**d2d1 \_ Text \_ antialias \_ mode CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) a **d2d1 \_ Text \_ antialias \_ mode in scala di grigi**. Quando si specifica una modalità Alpha di **d2d1 \_ Alpha \_ mode \_ sconosciuta**, Direct2D imposta l'alfa per l'utente, a seconda del tipo di destinazione di rendering.

È possibile utilizzare il metodo [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) per modificare la modalità di antialias del testo in [**d2d1 \_ Text \_ antialias \_ mode ClearType**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode), ma il rendering del testo CLEARTYPE in una superficie trasparente può generare risultati imprevedibili. Se si desidera eseguire il rendering del testo ClearType in una destinazione di rendering trasparente, è consigliabile utilizzare una delle due tecniche riportate di seguito.

-   Usare il metodo [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) per ritagliare la destinazione di rendering nell'area in cui verrà eseguito il rendering del testo, quindi chiamare il metodo [**Clear**](id2d1rendertarget-clear.md) e specificare un colore opaco, quindi eseguire il rendering del testo.
-   Usare [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) per creare un rettangolo opaco dietro l'area in cui verrà eseguito il rendering del testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_Formato pixel \_ d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**\_Modalità d2d1 Alpha \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[\_formato DXGI](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 