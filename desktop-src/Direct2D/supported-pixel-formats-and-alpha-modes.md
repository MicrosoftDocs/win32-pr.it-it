---
title: Formati pixel e modalità alfa supportati
description: Descrive i formati pixel e le modalità alfa supportati da ogni tipo di destinazione di rendering.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D, formati pixel
- Direct2D, modalità alfa
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d5b260741cae6aebb447a11692f03dad6e35498a19f33221aa77ac8a8507144a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917161"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formati pixel e modalità alfa supportati

Questo argomento descrive i formati pixel e le modalità alfa supportati dalle varie parti di Direct2D, tra cui ogni tipo di destinazione di rendering, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)e [**ID2D1ImageSource.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) Include le sezioni seguenti:

-   [Formati YUV supportati per l'origine immagine DXGI](#supported-yuv-formats-for-dxgi-image-source)
-   [Specifica di un formato pixel per una destinazione di rendering](#specifying-a-pixel-format-for-a-render-target)
-   [Formati supportati per ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Formati supportati per ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Formati supportati per la destinazione di rendering compatibile](#supported-formats-for-compatible-render-target)
-   [Formati supportati per la destinazione di rendering della superficie DXGI](#supported-formats-for-dxgi-surface-render-target)
-   [Formati supportati per la destinazione di rendering bitmap WIC](#supported-formats-for-wic-bitmap-render-target)
-   [Formati supportati per ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Specifica di un formato pixel per un oggetto ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Formati WIC supportati](#supported-wic-formats)
-   [Uso di un formato non supportato](#using-an-unsupported-format)
-   [Informazioni sulle modalità alfa](#about-alpha-modes)
    -   [Informazioni sulle modalità alfa premoltilied e straight](#about-premultiplied-and-straight-alpha-modes)
    -   [Differenze tra straight e premultiplied Alpha](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Modalità alfa per destinazioni di rendering](#alpha-mode-for-render-targets)
    -   [Modalità ClearType e Alpha](#cleartype-and-alpha-modes)
-   [Argomenti correlati](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Formati YUV supportati per l'origine immagine DXGI

[**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) è un provider di pixel astratto. È possibile crearne un'istanza da WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) o [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) supporta lo stesso set di formati pixel e modalità alfa di [**ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

Oltre a quelli elencati in precedenza, [**un oggetto ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) di cui viene creata un'istanza [**da IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) supporta anche alcuni formati di pixel YUV, inclusi i dati planari suddivisi in più superfici. Per altre informazioni sui requisiti per ogni formato pixel, vedere [**CreateImageSourceFromDxgi.**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)



| Formato                    |
|---------------------------|
| FORMATO DXGI \_ \_ AYUV        |
| FORMATO DXGI \_ \_ NV12        |
| FORMATO DXGI \_ \_ YUY2        |
| FORMATO DXGI \_ \_ P208        |
| FORMATO DXGI \_ \_ V208        |
| FORMATO DXGI \_ \_ V408        |
| DXGI \_ FORMAT \_ R8 \_ UNORM   |
| DXGI \_ FORMAT \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Specifica di un formato pixel per una destinazione di rendering

Quando si crea una destinazione di rendering, è necessario specificarne il formato pixel. Per specificare il formato pixel, usare una struttura [**D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) per impostare il membro **pixelFormat** di una [**struttura D2D1 \_ RENDER TARGET \_ \_ PROPERTIES.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Passare quindi la struttura al metodo Create appropriato, ad esempio [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

La [**struttura D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) include due campi:

-   **format**, un [valore DXGI \_ FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) che descrive le dimensioni e la disposizione dei canali in ogni pixel e
-   **alpha**, un [**valore D2D1 \_ ALPHA \_ MODE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) che descrive come vengono interpretate le informazioni alfa.

L'esempio seguente crea una struttura [**D2D1 \_ PIXEL \_ FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) e la usa per specificare il formato pixel e la modalità alfa di [**id2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)


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



Destinazioni di rendering diverse supportano combinazioni di formato e modalità alfa diverse. Le sezioni seguenti elencano le combinazioni di formato e alfa supportate da ogni destinazione di rendering.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Formati supportati per ID2D1HwndRenderTarget

I formati supportati per [**id2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dipendono dal fatto che il rendering sia eseguito usando hardware o software o che Direct2D gestisca automaticamente la modalità di rendering per impostazione predefinita.

> [!Note]  
> È consigliabile usare [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) come formato pixel per ottenere prestazioni migliori. Ciò è particolarmente utile per le destinazioni di rendering software. Le destinazioni di formato BGRA hanno prestazioni migliori rispetto ai formati RGBA.

 

Quando si crea un [**ID2D1HwndRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)si usa la struttura PROPRIETÀ DESTINAZIONE RENDERING [**D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) per specificare le opzioni di rendering. Le opzioni includono il formato pixel, come illustrato nella sezione precedente. Il campo type di questa struttura consente di specificare se la destinazione di rendering esegue il rendering in hardware o software o se Direct2D deve determinare automaticamente la modalità di rendering.

Per consentire a Direct2D di determinare se la destinazione di rendering usa il rendering hardware o software, usare l'impostazione [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)

Nella tabella seguente sono elencati i formati supportati per gli oggetti [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) creati usando l'impostazione [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)



| Formato                        | Modalità alfa                       |
|-------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |



 

Per forzare una destinazione di rendering a usare il rendering hardware, usare l'impostazione HARDWARE [**D2D1 \_ RENDER \_ TARGET \_ \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . Nella tabella seguente sono elencati i formati supportati per gli [**oggetti ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) che usano in modo esplicito il rendering hardware.



| Formato                        | Modalità alfa                       |
|-------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |



 

Per forzare una destinazione di rendering a usare il rendering software, usare l'impostazione SOFTWARE [**D2D1 \_ RENDER \_ TARGET \_ \_ TYPE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) Nella tabella seguente sono elencati i formati supportati per gli [**oggetti ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) che usano in modo esplicito il rendering software.



| Formato                        | Modalità alfa                       |
|-------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |



 

Indipendentemente dal fatto che [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) sia accelerato dall'hardware, il formato [DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa [DXGI \_ FORMAT \_ B8G8R8A8 per](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) impostazione predefinita e la modalità alfa [**D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa **D2D1 \_ ALPHA MODE \_ \_ IGNORE** per impostazione predefinita.

## <a name="supported-formats-for-id2d1devicecontext"></a>Formati supportati per ID2D1DeviceContext

A partire Windows 8 contesto [**di**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) dispositivo sfrutta più formati di colori [**elevati Direct3D,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) ad esempio:

-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM
-   FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT
-   FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT

Usare il [**metodo ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) per verificare se un formato funziona in un contesto di dispositivo specifico. Questi formati possono funzionare anche su [**id2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)

Questi formati sono oltre ai formati supportati [**dall'interfaccia ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) in Windows 7. Per [altre informazioni, vedere Dispositivi e contesti](devices-and-device-contexts.md) di dispositivo.

## <a name="supported-formats-for-compatible-render-target"></a>Formati supportati per la destinazione di rendering compatibile

Una destinazione di rendering compatibile [**(ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) creata da uno dei metodi [**ID2D1RenderTarget::CreateCompatibleRenderTarget)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) eredita i formati supportati e le modalità alfa della destinazione di rendering che l'ha creata. Una destinazione di rendering compatibile supporta anche le combinazioni di formato e modalità alfa seguenti, indipendentemente da ciò che supporta l'elemento padre.



| Formato                  | Modalità alfa                       |
|-------------------------|----------------------------------|
| FORMATO DXGI \_ \_ A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| FORMATO DXGI \_ \_ SCONOSCIUTO   | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |



 

Il formato [DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il formato di destinazione di rendering padre per impostazione predefinita e la modalità alfa [**D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa **D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED** per impostazione predefinita.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formati supportati per la destinazione di rendering della superficie DXGI

Una destinazione di rendering DXGI è un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creato da uno dei metodi [**ID2D1Factory::CreateDxgiSurfaceRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) Supporta le combinazioni di formato e modalità alfa seguenti.



| Formato                        | Modalità alfa                       |
|-------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |



 

> [!Note]  
> Il formato deve corrispondere al formato della superficie DXGI a cui viene disegnata la destinazione di rendering della superficie DXGI.

 

Il [formato DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il formato di superficie DXGI per impostazione predefinita. Non usare la modalità alfa [**D2D1 \_ ALPHA \_ MODE \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con una destinazione di rendering della superficie DXGI. Non ha alcun valore predefinito e causerà l'esito negativo della creazione della destinazione di rendering della superficie DXGI.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formati supportati per la destinazione di rendering bitmap WIC

Una destinazione di rendering bitmap WIC è un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) creato da uno dei metodi [**ID2D1Factory::CreateWicBitmapRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) Supporta le combinazioni di formato e modalità alfa seguenti.



| Formato                        | Modalità alfa                       |
|-------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ SCONOSCIUTO         | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |



 

Il formato pixel della destinazione bitmap WIC deve corrispondere al formato pixel della bitmap WIC.

Il [formato DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa il formato bitmap WIC per impostazione predefinita e la modalità alfa [**D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa la modalità alfa bitmap WIC per impostazione predefinita.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formati supportati per ID2D1DCRenderTarget

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) supporta le combinazioni di formato e modalità alfa seguenti.



| Formato                        | Modalità alfa                       |
|-------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |



 

Non usare il formato [DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) o la modalità alfa [**D2D1 \_ ALPHA MODE \_ \_ UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) con [**ID2D1DCRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) Non ha alcun valore predefinito e causerà l'esito negativo della creazione di **ID2D1DCRenderTarget.**

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Specifica di un formato pixel per un oggetto ID2D1Bitmap

In genere, [**gli oggetti ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) supportano i formati e le modalità alfa seguenti (con alcune restrizioni, descritte nei paragrafi seguenti).



| Formato                                                      | Modalità alfa                       |
|-------------------------------------------------------------|----------------------------------|
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM                               | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM                               | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ A8 \_ UNORM                                     | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ A8 \_ UNORM                                     | D2D1 \_ ALPHA \_ MODE \_ STRAIGHT      |
| FORMATO DXGI \_ \_ A8 \_ UNORM                                     | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| FORMATO DXGI \_ \_ SCONOSCIUTO                                       | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| FORMATO DXGI \_ \_ SCONOSCIUTO                                       | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| FORMATO DXGI \_ \_ SCONOSCIUTO                                       | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (solo Windows 8.1 e versioni successive) | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (solo Windows 8.1 versioni successive)      | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (solo Windows 8.1 versioni successive)      | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC1 \_ UNORM (solo Windows 8.1 versioni successive)      | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (solo Windows 8.1 versioni successive)      | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (solo Windows 8.1 versioni successive)      | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC2 \_ UNORM (solo Windows 8.1 versioni successive)      | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (solo Windows 8.1 versioni successive)      | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_ |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (solo Windows 8.1 versioni successive)      | D2D1 \_ ALPHA \_ MODE \_ IGNORE        |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (solo Windows 8.1 versioni successive)      | MODALITÀ ALFA D2D1 \_ \_ \_ SCONOSCIUTA       |



 

Quando si usa il metodo [**ID2D1RenderTarget::CreateSharedBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) si usa il campo **pixelFormat** di una struttura [**PROPRIETÀ \_ BITMAP \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) per specificare il formato pixel della nuova destinazione di rendering. Deve corrispondere al formato pixel [**dell'origine ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

Quando si usa il metodo [**CreateBitmapFromWicBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) si usa il campo **pixelFormat** di una struttura [**D2D1 \_ BITMAP \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (anziché il membro **pixelFormat** di una struttura [**D2D1 \_ RENDER TARGET \_ \_ PROPERTIES)**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) per specificare il formato pixel della nuova destinazione di rendering. Deve corrispondere al formato pixel dell'origine bitmap WIC.

> [!Note]  
> Per altre informazioni sul supporto per i formati di pixel compressi a blocchi (BCn), vedere [Compressione a blocchi](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formati WIC supportati

Quando si usa il [**metodo CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) per creare una bitmap da una bitmap WIC o quando si usa il metodo [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) con [**un oggetto IWICBitmapLock,**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock)l'origine WIC deve essere in un formato supportato da Direct2D.



| Formato WIC                     | Formato DXGI corrispondente     | Modalità alfa corrispondente                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | FORMATO DXGI \_ \_ A8 \_ UNORM       | MODALITÀ ALFA D2D1 \_ \_ STRAIGHT o \_ D2D1 \_ ALPHA \_ \_ PREMOLTIMULLIED |
| GUID \_ WICPixelFormat32bppPRGBA | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED o D2D1 \_ ALPHA MODE \_ \_ IGNORE   |
| GUID \_ WICPixelFormat32bppBGR   | FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | D2D1 \_ ALPHA \_ MODE \_ IGNORE                                       |
| GUID \_ WICPixelFormat32bppPBGRA | FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM | \_PREMOLTIMAZIONE DELLA MODALITÀ ALFA D2D1 \_ \_                                |



 

Per un esempio che illustra come convertire una bitmap WIC in un formato supportato, vedere Come caricare una [bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Uso di un formato non supportato

L'uso di qualsiasi combinazione diversa dai formati pixel e dalle modalità alfa elencate nelle tabelle precedenti comporta un errore [**D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**](direct2d-error-codes.md) o **E \_ INVALIDARG.**

## <a name="about-alpha-modes"></a>Informazioni sulle modalità alfa

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Informazioni sulle modalità alfa premoltilied e straight

[**L'enumerazione D2D1 \_ ALPHA \_ MODE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indica se il canale alfa usa alfa premoltilied, alfa diritto o deve essere ignorato e considerato opaco. Con alfa diritto, il canale alfa indica un valore che corrisponde alla trasparenza di un colore.

I colori vengono sempre considerati alfa rette dai comandi e dai pennelli di disegno Direct2D, indipendentemente dal formato di destinazione.

Con il valore alfa premoltilied, ogni canale di colore viene ridimensionato in base al valore alfa. In genere, nessun valore del canale di colore è maggiore del valore del canale alfa. Se il valore di un canale di colore in un formato pre-moltiplicato è maggiore del canale alfa, la matematica standard di fusione source-over crea una fusione additiva.

Il valore del canale alfa stesso è lo stesso sia in alfa diritto che pre-moltiplicato.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>Differenze tra straight e premultiplied Alpha

Quando si descrive un colore RGBA usando alfa diritto, il valore alfa del colore viene archiviato nel canale alfa. Ad esempio, per descrivere un colore rosso opaco al 60%, usare i valori seguenti: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). Il valore 255 indica il rosso pieno e 153 (ovvero il 60% di 255) indica che il colore deve avere un'opacità del 60%.

Quando si descrive un colore RGBA usando un alfa premoltiplicato, ogni colore viene moltiplicato per il valore alfa: (255 \* 0,6, \* 0 0,6, \* 0 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Indipendentemente dalla modalità alfa della destinazione di rendering, i [**valori D2D1 \_ COLOR \_ F**](d2d1-color-f.md) vengono sempre interpretati come alfa diritto. Ad esempio, quando si specifica il colore di un [**oggetto ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) da usare con una destinazione di rendering che usa la modalità alfa premoltilied, specificare il colore come si farebbe se la destinazione di rendering usasse un alfa diritto. Quando si disegna con il pennello, Direct2D converte il colore nel formato di destinazione.

### <a name="alpha-mode-for-render-targets"></a>Modalità alfa per destinazioni di rendering

Indipendentemente dall'impostazione della modalità alfa, il contenuto di una destinazione di rendering supporta la trasparenza. Ad esempio, se si disegna un rettangolo rosso parzialmente trasparente con una destinazione di rendering con modalità alfa [**D2D1 \_ ALPHA \_ MODE \_ IGNORE,**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)il rettangolo apparirà rosa (se lo sfondo è bianco).

Se si disegna un rettangolo rosso parzialmente trasparente quando la modalità alfa è [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED,**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)il rettangolo verrà visualizzato di colore rosa (presupponendo che lo sfondo sia bianco) ed è possibile vedere attraverso di esso tutto ciò che si trova dietro la destinazione di rendering. Ciò è utile quando si usa [**id2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per eseguire il rendering in una finestra trasparente o quando si usa una destinazione di rendering compatibile (un rendering di destinazione creato dal [**metodo CreateCompatibleRenderTarget)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) per creare una bitmap che supporta la trasparenza.

### <a name="cleartype-and-alpha-modes"></a>Modalità ClearType e Alpha

Se si specifica una modalità alfa diversa da [**D2D1 \_ ALPHA \_ MODE \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) per una destinazione di rendering, la modalità antialiasing del testo cambia automaticamente da [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) a **D2D1 \_ TEXT \_ ANTIALIAS \_ MODE GRAYSCALE**. Quando si specifica una modalità alfa **D2D1 \_ ALPHA \_ MODE \_ UNKNOWN,** Direct2D imposta automaticamente il valore alfa, a seconda del tipo di destinazione di rendering.

È possibile usare il [**metodo SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) per modificare la modalità antialias del testo in [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode)ma il rendering del testo ClearType su una superficie trasparente può creare risultati imprevedibili. Se si vuole eseguire il rendering del testo ClearType in una destinazione di rendering trasparente, è consigliabile usare una delle due tecniche seguenti.

-   Usare il [**metodo PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) per ritagliare la destinazione di rendering nell'area in cui verrà eseguito il rendering del testo, quindi chiamare il metodo [**Clear**](id2d1rendertarget-clear.md) e specificare un colore opaco, quindi eseguire il rendering del testo.
-   Usare [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) per disegnare un rettangolo opaco dietro l'area in cui verrà eseguito il rendering del testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**FORMATO PIXEL D2D1 \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**MODALITÀ ALFA \_ D2D1 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[FORMATO \_ DXGI](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 