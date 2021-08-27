---
title: Cenni preliminari sulle maschere di opacità
description: 'Questo argomento descrive come usare bitmap e pennelli per definire le maschere di opacità. Include le sezioni seguenti:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513365474ed6b1f6f42d34f9b876226e00ba6e85
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786377"
---
# <a name="opacity-masks-overview"></a>Cenni preliminari sulle maschere di opacità

Questo argomento descrive come usare bitmap e pennelli per definire le maschere di opacità. Include le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Che cos'è una maschera di opacità?](#what-is-an-opacity-mask)
-   [Usare una bitmap come maschera di opacità con il metodo FillOpacityMask](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Usare un pennello come maschera di opacità con il metodo FillGeometry](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Usare un pennello a sfumatura lineare come maschera di opacità](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Usare un pennello sfumatura radiale come maschera di opacità](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Applicare una maschera di opacità a un livello](#apply-an-opacity-mask-to-a-layer)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

Questa panoramica presuppone che si abbia familiarità con le operazioni di disegno Direct2D di base, come descritto nella procedura dettagliata Creazione di [un'applicazione Direct2D](direct2d-quickstart.md) semplice. È anche necessario avere familiarità con i diversi tipi di pennelli, come descritto in [Cenni preliminari sui pennelli](direct2d-brushes-overview.md).

## <a name="what-is-an-opacity-mask"></a>Che cos'è una maschera di opacità?

Una maschera di opacità è una maschera, descritta da un pennello o da una bitmap, applicata a un altro oggetto per rendere l'oggetto parzialmente o completamente trasparente. Una maschera di opacità usa le informazioni del canale alfa per specificare la modalità di fusione dei pixel di origine dell'oggetto nella destinazione finale. Le parti trasparenti della maschera indicano le aree in cui l'immagine sottostante è nascosta, mentre le parti opache della maschera indicano dove è visibile l'oggetto mascherato.

Esistono diversi modi per applicare una maschera di opacità:

-   Usare il [**metodo ID2D1RenderTarget::FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md) Il **metodo FillOpacityMask** disegna un'area rettangolare di una destinazione di rendering e quindi applica una maschera di opacità, definita da una bitmap. Usare questo metodo quando la maschera di opacità è una bitmap e si vuole riempire un'area rettangolare.
-   Usare il [**metodo ID2D1RenderTarget::FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Il **metodo FillGeometry** disegna l'interno della geometria con l'oggetto [**ID2D1BitmapBrush specificato,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)quindi applica una maschera di opacità, definita da un pennello. Usare questo metodo quando si vuole applicare una maschera di opacità a una geometria o si vuole usare un pennello come maschera di opacità.
-   Usare [**id2D1Layer per**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) applicare una maschera di opacità. Usare questo approccio quando si vuole applicare una maschera di opacità a un gruppo di contenuti di disegno, non solo a una singola forma o immagine. Per informazioni dettagliate, vedere Panoramica [dei livelli](direct2d-layers-overview.md).

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Usare una bitmap come maschera di opacità con il metodo FillOpacityMask

Il [**metodo FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) disegna un'area rettangolare di una destinazione di rendering e quindi applica una maschera di opacità, definita da [**id2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) Usare questo metodo quando si dispone di una bitmap che si vuole usare come maschera di opacità per un'area rettangolare.

Il diagramma seguente illustra un effetto dell'applicazione della maschera di opacità [**(id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con un'immagine di un fiore) a [**un oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con un'immagine di una pianta felce. L'immagine risultante è una bitmap di una pianta ritagliata alla forma del fiore.

![diagramma di una bitmap di fiori usata come maschera di opacità su un'immagine di una pianta felce](images/brushes-ovw-bitmapopacity.png)

Gli esempi di codice seguenti illustrano come eseguire questa operazione.

Nel primo esempio viene caricata la bitmap *m \_ pBitmapMask* seguente da usare come maschera bitmap. La figura seguente mostra l'output prodotto. Si noti che, anche se la parte opaca della bitmap appare nera, le informazioni sul colore nella bitmap non hanno alcun effetto sulla maschera di opacità. vengono usate solo le informazioni sull'opacità di ogni pixel nella bitmap. I pixel completamente opachi in questa bitmap sono stati colorati di nero solo a scopo illustrativo.

![illustrazione della maschera bitmap dei fiori](images/bitmapmask.png)

In questo esempio [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) viene caricato da un metodo helper, LoadResourceBitmap, definito altrove nell'esempio.


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



L'esempio successivo definisce il *pennello, m \_ pFernBitmapBrush,* a cui viene applicata la maschera di opacità. Questo esempio usa un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) che contiene un'immagine di una felce, ma è possibile usare [**id2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)o [**ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) La figura seguente mostra l'output prodotto.

![Illustrazione della bitmap usata dal pennello bitmap](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





Dopo aver definito la maschera di opacità e il pennello, è possibile usare il [**metodo FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) nel metodo di rendering dell'applicazione. Quando si chiama il metodo **FillOpacityMask,** è necessario specificare il tipo di maschera di opacità in uso: **D2D1 \_ OPACITY \_ MASK CONTENT \_ \_ GRAPHICS,** **D2D1 \_ OPACITY MASK CONTENT \_ TEXT \_ \_ \_ NATURAL** e **D2D1 \_ OPACITY MASK CONTENT TEXT \_ \_ \_ \_ GDI \_ COMPATIBLE**. Per i significati di questi tre tipi, vedere [**CONTENUTO MASCHERA \_ OPACITÀ \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> A partire da Windows 8, il [**CONTENUTO MASCHERA OPACITÀ D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) non è necessario. Vedere il [**metodo ID2D1DeviceContext::FillOpacityMask,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) senza parametro **CONTENT \_ OPACITY \_ MASK \_ D2D1.**

 

L'esempio successivo imposta la modalità di antialiasing della destinazione di rendering su [**D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) in modo che la maschera di opacità funzioni correttamente. Chiama quindi il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) e le passa la maschera di opacità (*m \_ pBitmapMask*), il pennello a cui viene applicata la maschera di opacità (*m \_ pFernBitmapBrush*), il tipo di contenuto all'interno della maschera di opacità ([**D2D1 \_ OPACITY MASK CONTENT \_ \_ \_ GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) e l'area da disegnare. La figura seguente mostra l'output prodotto.

![Illustrazione dell'immagine della pianta felce con una maschera di opacità applicata](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





Il codice è stato omesso da questo esempio.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Usare un pennello come maschera di opacità con il metodo FillGeometry

La sezione precedente descrive come usare [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) come maschera di opacità. Direct2D fornisce anche il metodo [**ID2D1RenderTarget::FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) che consente di specificare facoltativamente il pennello come maschera di opacità quando si riempie [**un oggetto ID2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) In questo modo è possibile creare maschere di opacità da sfumature (usando [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) o [**ID2D1RadialGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)e bitmap (usando **ID2D1Bitmap).**

Il [**metodo FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) accetta tre parametri:

-   Il primo parametro, [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)definisce la forma da disegnare.
-   Il secondo parametro, [**ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)specifica il pennello usato per disegnare la geometria. Questo parametro deve essere un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con le modalità di estensione x e y impostate su [**D2D1 \_ EXTEND MODE \_ \_ CLAMP.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)
-   Il terzo parametro, [**ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)specifica un pennello da usare come maschera di opacità. Questo pennello può essere [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)o [**ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) Tecnicamente, è possibile usare un [**oggetto ID2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)ma l'uso di un pennello a tinta unita come maschera di opacità non produce risultati interessanti.

Le sezioni seguenti descrivono come usare [**gli oggetti ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) e [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) come maschere di opacità.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Usare un pennello a sfumatura lineare come maschera di opacità

Il diagramma seguente illustra l'effetto dell'applicazione di un pennello sfumato lineare a un rettangolo riempito con una bitmap di fiori.

![Diagramma di una bitmap di fiori con un pennello sfumato lineare applicato](images/brushes-ovw-lineargradient-opacitymask.png)

I passaggi seguenti descrivono come creare nuovamente questo effetto.

1.  Definire il contenuto da mascherare. L'esempio seguente crea [**un oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*. La modalità di estensione x e y- per *m \_ pLinearFadeFlowersBitmap* è impostata su [**D2D1 \_ EXTEND MODE \_ \_ CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) in modo che possa essere usata con una maschera di opacità dal [**metodo FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    
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
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    
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
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  Definire la maschera di opacità. L'esempio di codice successivo crea un pennello a sfumatura lineare diagonale (*m \_ pLinearGradientBrush*) che dissolve dal nero completamente opaco alla posizione 0 al bianco completamente trasparente nella posizione 1.
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  Usare il [**metodo FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) L'esempio finale usa il metodo **FillGeometry** per riempire un [**oggetto ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) con [**un oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) e applica una maschera di opacità (*m \_ pLinearGradientBrush*).
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

Il codice è stato omesso da questo esempio.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Usare un pennello sfumatura radiale come maschera di opacità

Il diagramma seguente illustra l'effetto visivo dell'applicazione di un pennello sfumatura radiale a un rettangolo riempito con una bitmap di fogliame.

![Diagramma di una bitmap fogliare con un pennello sfumatura radiale applicato](images/brushes-ovw-radialgradient-opacitymask.png)

Il primo esempio crea un [**oggetto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*. In modo che possa essere usata con una maschera di opacità dal metodo [**FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) le modalità di estensione x e y per *m \_ pRadialFadeFlowersBitmapBrush* sono impostate su [**D2D1 \_ EXTEND MODE \_ \_ CLAMP.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```





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
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>



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
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



L'esempio successivo definisce il pennello sfumatura radiale che verrà usato come maschera di opacità.


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





L'esempio di codice finale usa [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) e la maschera di opacità (*m \_ pRadialGradientBrush*) per riempire un [**oggetto ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



Il codice è stato omesso da questo esempio.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Applicare una maschera di opacità a un livello

Quando si chiama [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) per eseguire il push di [**un oggetto ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) in una destinazione di rendering, è possibile usare la struttura [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) per applicare un pennello come maschera di opacità. L'esempio di codice seguente usa [**id2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) come maschera di opacità.


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



Per altre informazioni sull'uso dei livelli, vedere Panoramica [dei livelli](direct2d-layers-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> <dt>

[Panoramica dei livelli](direct2d-layers-overview.md)
</dt> </dl>

 

 
