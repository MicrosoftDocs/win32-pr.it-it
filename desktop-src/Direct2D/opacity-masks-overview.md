---
title: Cenni preliminari sulle maschere di opacità
description: 'Questo argomento descrive come usare bitmap e pennelli per definire le maschere di opacità. Include le sezioni seguenti:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104564290"
---
# <a name="opacity-masks-overview"></a>Cenni preliminari sulle maschere di opacità

Questo argomento descrive come usare bitmap e pennelli per definire le maschere di opacità. Include le sezioni seguenti:

-   [Prerequisiti](#prerequisites)
-   [Che cos'è una maschera di opacità?](#what-is-an-opacity-mask)
-   [Usare una bitmap come maschera di opacità con il metodo FillOpacityMask](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Usare un pennello come maschera di opacità con il metodo FillGeometry](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Usare un pennello sfumato lineare come maschera di opacità](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Usare un pennello a sfumatura radiale come maschera di opacità](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Applicare una maschera di opacità a un livello](#apply-an-opacity-mask-to-a-layer)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites"></a>Prerequisiti

In questa panoramica si presuppone che l'utente abbia familiarità con le operazioni di disegno Direct2D di base, come descritto nella procedura dettagliata relativa alla [creazione di un'applicazione Direct2d semplice](direct2d-quickstart.md) . È anche necessario conoscere i diversi tipi di pennelli, come descritto nella panoramica dei [pennelli](direct2d-brushes-overview.md).

## <a name="what-is-an-opacity-mask"></a>Che cos'è una maschera di opacità?

Una maschera di opacità è una maschera, descritta da un pennello o una bitmap, applicata a un altro oggetto per rendere tale oggetto parzialmente o completamente trasparente. Una maschera di opacità usa le informazioni sul canale alfa per specificare la modalità di fusione dei pixel di origine dell'oggetto nella destinazione finale di destinazione. Le parti trasparenti della maschera indicano le aree in cui l'immagine sottostante è nascosta, mentre le parti opache della maschera indicano dove è visibile l'oggetto mascherato.

Esistono diversi modi per applicare una maschera di opacità:

-   Usare il metodo [**ID2D1RenderTarget:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) . Il metodo **FillOpacityMask** disegna un'area rettangolare di una destinazione di rendering e quindi applica una maschera di opacità, definita da una bitmap. Utilizzare questo metodo quando la maschera di opacità è una bitmap e si desidera riempire un'area rettangolare.
-   Usare il metodo [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . Il metodo **FillGeometry** disegna l'interno della geometria con il [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)specificato, quindi applica una maschera di opacità, definita da un pennello. Utilizzare questo metodo quando si desidera applicare una maschera di opacità a una geometria o si desidera utilizzare un pennello come maschera di opacità.
-   Usare un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) per applicare una maschera di opacità. Utilizzare questo approccio quando si desidera applicare una maschera di opacità a un gruppo di contenuto del disegno, non solo a una singola forma o immagine. Per informazioni dettagliate, vedere [Cenni preliminari sui livelli](direct2d-layers-overview.md).

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Usare una bitmap come maschera di opacità con il metodo FillOpacityMask

Il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) disegna un'area rettangolare di una destinazione di rendering e quindi applica una maschera di opacità, definita da un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap). Utilizzare questo metodo quando si dispone di una bitmap che si desidera utilizzare come maschera di opacità per un'area rettangolare.

Il diagramma seguente mostra l'effetto dell'applicazione della maschera di opacità (un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con un'immagine di un fiore) a un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con un'immagine di una pianta felce. L'immagine risultante è una mappa di bit di un impianto ritagliata in forma floreale.

![diagramma di una bitmap floreale usata come maschera di opacità su un'immagine di una pianta di felce](images/brushes-ovw-bitmapopacity.png)

Negli esempi di codice seguenti viene illustrato il modo in cui questa operazione viene eseguita.

Il primo esempio carica la bitmap seguente, *m \_ pBitmapMask*, da usare come maschera di bitmap. Nella figura seguente viene illustrato l'output generato. Si noti che, sebbene la parte opaca della bitmap appaia nera, le informazioni sul colore nella bitmap non hanno effetto sulla maschera di opacità. vengono utilizzate solo le informazioni di opacità di ogni pixel della bitmap. I pixel completamente opachi in questa bitmap sono stati colorati a scopo puramente illustrativo.

![illustrazione della maschera di bit per i fiori](images/bitmapmask.png)

In questo esempio, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) viene caricato da un metodo helper, LoadResourceBitmap, definito altrove nell'esempio.


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



Nell'esempio successivo viene definito il pennello, *m \_ pFernBitmapBrush*, a cui viene applicata la maschera di opacità. In questo esempio viene usato un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) che contiene un'immagine di una felce, ma è invece possibile usare [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) . Nella figura seguente viene illustrato l'output generato.

![illustrazione della bitmap utilizzata dal pennello bitmap](images/fern.png)


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





Ora che la maschera di opacità e il pennello sono definiti, è possibile usare il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) nel metodo di rendering dell'applicazione. Quando si chiama il metodo **FillOpacityMask** , è necessario specificare il tipo di maschera di opacità che si sta usando: d2d1 maschera di opacità **\_ \_ \_ contenuto \_ grafica**, **d2d1 \_ opacità \_ \_ contenuto \_ testo \_ naturale** e **d2d1 \_ Opacity \_ maschera \_ contenuto \_ testo \_ GDI \_ compatibile**. Per i significati di questi tre tipi, vedere [**\_ contenuto della \_ maschera \_ di opacità di d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> A partire da Windows 8, [**il \_ \_ \_ contenuto della maschera di opacità d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) non è obbligatorio. Vedere il metodo [**ID2D1DeviceContext:: FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , che non ha un parametro di **contenuto della \_ \_ maschera \_ di opacità d2d1** .

 

Nell'esempio seguente la modalità di anti-aliasing della destinazione di rendering viene impostata su [**d2d1 \_ antialias \_ mode con \_ alias**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) in modo che la maschera di opacità funzioni correttamente. Chiama quindi il metodo [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) e lo passa alla maschera di opacità (*m \_ pBitmapMask*), al pennello a cui viene applicata la maschera di opacità (*m \_ pFernBitmapBrush*), al tipo di contenuto all'interno della maschera di opacità (immagine del [**contenuto della \_ maschera di opacità \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) e all'area da disegnare. Nella figura seguente viene illustrato l'output generato.

![illustrazione dell'immagine di Fern Plant con una maschera di opacità applicata](images/opacitymaskoutput.png)


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

La sezione precedente descrive come usare un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) come maschera di opacità. Direct2D fornisce anche il metodo [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , che consente di specificare facoltativamente il pennello come maschera di opacità quando si compila un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry). In questo modo è possibile creare maschere di opacità da sfumature (usando [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) e bitmap (usando **ID2D1Bitmap**).

Il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) accetta tre parametri:

-   Il primo parametro, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), definisce la forma da disegnare.
-   Il secondo parametro, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifica il pennello utilizzato per disegnare la geometria. Questo parametro deve essere un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con le modalità di estensione x e y impostate su [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).
-   Il terzo parametro, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifica un pennello da utilizzare come maschera di opacità. Questo pennello può essere [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)o [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). Tecnicamente, è possibile usare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), ma l'uso di un pennello tinta unita come maschera di opacità non produce risultati interessanti.

Le sezioni seguenti descrivono come usare gli oggetti [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) e [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) come maschere di opacità.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Usare un pennello sfumato lineare come maschera di opacità

Il diagramma seguente mostra l'effetto dell'applicazione di un pennello sfumato lineare a un rettangolo riempito con una bitmap di fiori.

![diagramma di una bitmap floreale con un pennello sfumato lineare applicato](images/brushes-ovw-lineargradient-opacitymask.png)

I passaggi seguenti descrivono come ricreare questo effetto.

1.  Definire il contenuto da mascherare. Nell'esempio seguente viene creato un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*. La modalità di estensione x e y per *m \_ pLinearFadeFlowersBitmap* sono impostate su [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) , in modo che possa essere usato con una maschera di opacità dal metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

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

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
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

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
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

    

2.  Definire la maschera di opacità. Nell'esempio di codice successivo viene creato un pennello sfumato lineare diagonale (*m \_ pLinearGradientBrush*) che si dissolve dal nero completamente opaco nella posizione 0 al bianco completamente trasparente nella posizione 1.
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



    

3.  Usare il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . L'esempio finale usa il metodo **FillGeometry** per il pennello del contenuto per riempire [**un ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) e applica una maschera di opacità (*m \_ pLinearGradientBrush*).
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

Il codice è stato omesso da questo esempio.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Usare un pennello a sfumatura radiale come maschera di opacità

Il diagramma seguente illustra l'effetto visivo dell'applicazione di un pennello a sfumatura radiale a un rettangolo riempito con una bitmap di fogliame.

![diagramma di una bitmap fogliame con un pennello a sfumatura radiale applicato](images/brushes-ovw-radialgradient-opacitymask.png)

Nel primo esempio viene creato un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*. In modo che possa essere usato con una maschera di opacità dal metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , la modalità di estensione x e y per *m \_ PRadialFadeFlowersBitmapBrush* sono impostate su [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).


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



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
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

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
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



Nell'esempio successivo viene definito il pennello a sfumatura radiale che verrà utilizzato come maschera di opacità.


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





L'esempio di codice finale USA [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) e la maschera di opacità (*m \_ pRadialGradientBrush*) per riempire un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



Il codice è stato omesso da questo esempio.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Applicare una maschera di opacità a un livello

Quando si chiama [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) per eseguire il push di un [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) su una destinazione di rendering, è possibile usare la struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) per applicare un pennello come maschera di opacità. Nell'esempio di codice seguente viene usato un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) come maschera di opacità.


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



Per ulteriori informazioni sull'utilizzo dei livelli, vedere [Cenni preliminari sui livelli](direct2d-layers-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dei pennelli](direct2d-brushes-overview.md)
</dt> <dt>

[Panoramica sui livelli](direct2d-layers-overview.md)
</dt> </dl>

 

 