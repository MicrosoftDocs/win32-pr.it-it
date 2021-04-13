---
title: 'Panoramica dei pennelli '
description: Vengono descritti i diversi tipi di pennelli forniti da Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399896"
---
# <a name="brushes-overview"></a>Panoramica dei pennelli 

In questa panoramica viene descritto come creare e utilizzare oggetti [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per disegnare aree con colori a tinta unita, sfumature e bitmap. Include le sezioni seguenti:

## <a name="prerequisites"></a>Prerequisiti

In questa panoramica si presuppone che l'utente abbia familiarità con la struttura di un'applicazione Direct2D di base, come descritto in [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md).

## <a name="brush-types"></a>Tipi di pennello

Un pennello "disegna" un'area con l'output. Pennelli diversi hanno diversi tipi di output. Direct2D fornisce quattro tipi di pennello: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) disegna un'area con un colore a tinta unita, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) con una sfumatura lineare, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) con una sfumatura radiale e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con una bitmap.

> [!NOTE]  
> A partire da Windows 8, è anche possibile usare [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), che è simile a un pennello bitmap, ma è anche possibile usare le primitive.

Tutti i pennelli ereditano da [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e condividono un set di funzionalità comuni (impostazione e recupero dell'opacità e trasformazione dei pennelli); vengono creati da [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e sono risorse dipendenti dal dispositivo: l'applicazione deve creare pennelli dopo avere inizializzato la destinazione di rendering con cui verranno usati i pennelli e ricreare i pennelli ogni volta che la destinazione di rendering deve essere ricreata. Per ulteriori informazioni sulle risorse, vedere [Cenni preliminari sulle risorse](resources-and-resource-domains.md).

Nella figura seguente vengono illustrati esempi di ognuno dei diversi tipi di pennelli.

![illustrazione degli effetti visivi da pennelli a tinta unita, pennelli sfumati lineari, pennelli sfumatura radiali e pennelli bitmap](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>Nozioni di base sui colori

Prima di disegnare con un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o un pennello sfumato, è necessario scegliere i colori. In Direct2D i colori sono rappresentati dalla struttura [**d2d1 \_ Color \_ F**](d2d1-color-f.md) (che è in realtà un nuovo nome per la struttura usata da Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).

Prima di Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) usa la codifica sRGB. la codifica sRGB divide i colori in quattro componenti: rosso, verde, blu e alfa. Ogni componente è rappresentato da un valore a virgola mobile con un intervallo normale compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del colore specifico, mentre il valore 1,0 indica che il colore è completamente presente. Per il componente alfa, 0,0 rappresenta un colore completamente trasparente e 1,0 rappresenta un colore completamente opaco.

A partire da Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) accetta anche la codifica di ScRGB. scRGB è un superset di che consente valori di colore superiori a 1,0 e inferiori a 0,0.

Per definire un colore, è possibile usare la struttura [**d2d1 \_ Color \_ F**](d2d1-color-f.md) e inizializzare i campi manualmente oppure è possibile usare la classe [**D2D1:: ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) per creare il colore. La classe **ColorF** fornisce diversi costruttori per la definizione dei colori. Se il valore alfa non è specificato nei costruttori, il valore predefinito è 1,0.

-   Usare il costruttore [**ColorF (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) per specificare un colore predefinito e un valore di canale alfa. Un valore di canale alfa è compreso tra 0,0 e 1,0, dove 0,0 rappresenta un colore completamente trasparente e 1,0 rappresenta un colore completamente opaco. Nella figura seguente vengono illustrati diversi colori predefiniti e i rispettivi equivalenti esadecimali. Per un elenco completo dei colori predefiniti, vedere la sezione relativa alle costanti colore della classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

    ![illustrazione dei colori predefiniti](images/brushes-ovw-colors.png)

    Nell'esempio seguente viene creato un colore predefinito che viene utilizzato per specificare il colore di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   Usare il costruttore [**ColorF (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) per specificare un colore nella sequenza di rosso, verde, blu e alfa, dove ogni elemento ha un valore compreso tra 0,0 e 1,0.

    Nell'esempio seguente vengono specificati i valori rosso, verde, blu e alfa per un colore.

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   Usare il costruttore [**ColorF (UInt32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) per specificare il valore esadecimale di un colore e un valore alfa, come illustrato nell'esempio seguente.
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Modalità Alpha

Indipendentemente dalla modalità Alpha della destinazione di rendering con cui si usa un pennello, i [**valori \_ \_ F dei colori d2d1**](d2d1-color-f.md) vengono sempre interpretati come caratteri alfa dritti.

## <a name="using-solid-color-brushes"></a>Uso di pennelli a tinta unita

Per creare un pennello tinta unita, chiamare il metodo [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , che restituisce un valore HRESULT e un oggetto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) . La figura seguente mostra un quadrato tracciato con un pennello di colore nero e disegnato con un pennello tinta unita con il valore di colore 0x9ACD32.

![illustrazione di un quadrato disegnato con un pennello tinta unita](images/brushes-ovw-solidcolor.png)

Il codice seguente illustra come creare e usare un pennello di colore nero e un pennello con un valore di colore 0x9ACD32 per riempire e creare il quadrato.


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



A differenza di altri pennelli, la creazione di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) è un'operazione relativamente economica. È possibile creare oggetti **ID2D1SolidColorBrush** ogni volta che viene eseguito il rendering con un effetto minimo sulle prestazioni. Questo approccio non è consigliato per i pennelli sfumatura o bitmap.

## <a name="using-linear-gradient-brushes"></a>Uso di pennelli sfumati lineari

Un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) disegna un'area con una sfumatura lineare definita lungo una riga, l'asse delle sfumature. È possibile specificare i colori della sfumatura e la relativa posizione lungo l'asse delle sfumature usando gli oggetti [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) . È anche possibile modificare l'asse delle sfumature, che consente di creare sfumature orizzontali e verticali e invertire la direzione della sfumatura. Per creare un pennello sfumato lineare, chiamare il metodo [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .

Nella figura seguente viene illustrato un quadrato disegnato con un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) con due colori predefiniti, "Yellow" e "ForestGreen".

![illustrazione di un quadrato disegnato con un pennello sfumato lineare di colore giallo e verde della foresta](images/brushes-ovw-lineargradient.png)

Per creare la sfumatura mostrata nell'illustrazione precedente, completare i passaggi seguenti:

1.  Dichiarare due oggetti di [**\_ \_ interruzione sfumatura d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Ogni cursore sfumatura specifica un colore e una posizione. La posizione 0,0 indica l'inizio della sfumatura, mentre la posizione 1,0 indica la fine della sfumatura.

    Il codice seguente crea una matrice di due oggetti di [**\_ \_ interruzione sfumatura d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Il primo arresto specifica il colore "Yellow" nella posizione 0, mentre il secondo stop specifica il colore "ForestGreen" nella posizione 1.

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  Creare un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection). Nell'esempio seguente viene chiamato [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passando la matrice di oggetti di [**\_ \_ interruzione della sfumatura d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , il numero di cursori sfumatura (2), [**d2d1 \_ gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) per l'interpolazione e il [**\_ \_ \_ morsetto della modalità Extend d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) per la modalità di estensione.

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  Creare il [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). Nell'esempio successivo viene chiamato il metodo [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) e vengono passate le proprietà del pennello sfumatura lineare che contengono il punto iniziale in (0,0) e il punto finale in (150, 150) e i cursori sfumatura creati nel passaggio precedente.
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  Usare [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). Nell'esempio di codice successivo viene usato il pennello per eseguire la filleina di un rettangolo.
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>Altre informazioni sui cursori sfumatura

Il [**\_ cursore sfumatura \_ d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) è il blocco predefinito di base di un pennello sfumatura. Un cursore sfumatura specifica il colore e la posizione lungo l'asse delle sfumature. Il valore della posizione della sfumatura è compreso tra 0,0 e 1,0. Più è vicino a 0,0, più il colore è vicino all'inizio della sfumatura. più è vicino a 1,0, più il colore è vicino alla fine della sfumatura.

Nell'illustrazione seguente vengono evidenziati i cursori sfumatura. Il cerchio contrassegna la posizione dei cursori sfumatura e una linea tratteggiata mostra l'asse delle sfumature.

![illustrazione di un pennello sfumato lineare con quattro interruzioni lungo l'asse](images/4stoplineargradient.png)

Il primo cursore sfumatura specifica il colore giallo alla posizione 0,0. Il secondo cursore sfumatura specifica il colore rosso in corrispondenza della posizione 0,25. Da sinistra a destra lungo l'asse delle sfumature, i colori tra queste due interruzioni cambiano gradualmente da giallo a rosso. Il terzo cursore sfumatura specifica il colore blu nella posizione 0,75. I colori tra il secondo e il terzo interruzioni della sfumatura cambiano gradualmente da rosso a blu. Il quarto cursore sfumatura specifica verde limone alla posizione 1,0. I colori tra il terzo e il quarto cursore sfumatura cambiano gradualmente da blu a verde limone.

## <a name="the-gradient-axis"></a>Asse delle sfumature

Come indicato in precedenza, i cursori sfumatura di un pennello sfumato lineare sono posizionati lungo una riga, l'asse delle sfumature. È possibile specificare l'orientamento e la dimensione della linea usando i campi **StartPoint** ed **endpoint** della struttura [**delle \_ \_ proprietà del \_ pennello \_ sfumatura lineare d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) quando si crea un pennello sfumatura lineare. Dopo aver creato un pennello, è possibile modificare l'asse delle sfumature chiamando i metodi [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) e [**seendpoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) del pennello. Modificando il punto iniziale e il punto finale del pennello, è possibile creare sfumature orizzontali e verticali, invertire la direzione della sfumatura e altro ancora.

Nella figura seguente, ad esempio, il punto iniziale è impostato su (0,0) e il punto finale a (150, 50); viene creata una sfumatura diagonale che inizia dall'angolo superiore sinistro e si estende all'angolo inferiore destro dell'area da disegnare. Quando si imposta il punto iniziale su (0, 25) e il punto finale su (150, 25), viene creata una sfumatura orizzontale. Analogamente, impostando il punto iniziale su (75, 0) e il punto finale su (75, 50) viene creata una sfumatura verticale. Impostando il punto iniziale su (0, 50) e il punto finale su (150, 0) viene creata una sfumatura diagonale che inizia dall'angolo inferiore sinistro e si estende all'angolo superiore destro dell'area da disegnare.

![illustrazione di quattro diversi assi sfumatura sullo stesso rettangolo](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>Uso di pennelli con sfumatura radiale

A differenza di un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), che combina due o più colori lungo un asse di sfumatura, un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) disegna un'area con una sfumatura radiale che combina due o più colori in un'ellisse. Mentre un **ID2D1LinearGradientBrush** definisce l'asse delle sfumature con un punto iniziale e un punto finale, un **ID2D1RadialGradientBrush** definisce l'ellisse sfumatura specificando un raggio centrale, orizzontale e verticale e un offset di origine sfumatura.

Analogamente a [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) usa un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) per specificare i colori e le posizioni nella sfumatura.

Nella figura seguente viene illustrato un cerchio disegnato con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush). Il cerchio presenta due cursori sfumatura: il primo specifica un colore predefinito "Yellow" nella posizione 0,0 e il secondo specifica un colore predefinito "ForestGreen" nella posizione 1,0. La sfumatura ha un centro di (75, 75), un offset di origine sfumatura pari a (0,0) e un raggio x e y di 75.

![illustrazione di un cerchio disegnato con un pennello a sfumatura radiale](images/brushes-ovw-radials.png)

Negli esempi di codice seguenti viene illustrato come disegnare questo cerchio con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) con due interruzioni di colore: "Yellow" nella posizione 0,0 e "ForestGreen" nella posizione 1,0. Analogamente alla creazione di un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), l'esempio chiama [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) per creare un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) da una matrice di cursori sfumatura.


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



Per creare un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), usare il metodo [**ID2D1RenderTarget:: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) . **CreateRadialGradientBrush** accetta tre parametri. Il primo parametro, una [**\_ proprietà del \_ \_ pennello \_ sfumatura radiale d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) , specifica il centro, l'offset di origine sfumatura e i raggi orizzontali e verticali della sfumatura. Il secondo parametro è un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) che descrive i colori e le rispettive posizioni nella sfumatura e il terzo parametro è l'indirizzo del puntatore che riceve il nuovo riferimento **ID2D1RadialGradientBrush** . Alcuni overload accettano un parametro aggiuntivo, una struttura di [**\_ \_ proprietà del pennello d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) che specifica un valore di opacità e una trasformazione da applicare al nuovo pennello.

Nell'esempio seguente viene chiamato [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passando la matrice di cursori sfumatura e le proprietà del pennello sfumatura radiale con il valore *Center* impostato su (75, 75), *gradientOriginOffset* impostato su (0, 0) e *radiusX* e *RadiusY* entrambi impostati su 75.


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



Nell'esempio finale viene usato il pennello per riempire un'ellisse.


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>Configurazione di una sfumatura radiale

Valori diversi per *Center*, *gradientOriginOffset*, *RadiusX* e/o *RadiusY* producono gradienti diversi. Nella figura seguente sono illustrate diverse sfumature radiali con offset di origine sfumatura diversi, creando l'aspetto della luce che illumina i cerchi da angoli diversi.

![illustrazione dello stesso cerchio disegnato con pennelli con sfumature radiali con offset di origine diversi](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>Uso di pennelli bitmap

Un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) disegna un'area con una bitmap (rappresentata da un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).

Nella figura seguente viene illustrato un quadrato disegnato con una bitmap di un impianto.

![illustrazione di un quadrato disegnato con una bitmap Plant](images/brushes-ovw-bitmap.png)

Negli esempi seguenti viene illustrato come disegnare questo quadrato con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).

Nel primo esempio viene inizializzato un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) per l'utilizzo con il pennello. **ID2D1Bitmap** viene fornito da un metodo helper, LoadResourceBitmap, definito altrove nell'esempio.


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



Per creare il pennello bitmap, chiamare il metodo [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e specificare [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con cui disegnare. Il metodo restituisce un valore **HRESULT** e un oggetto [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) . Alcuni overload di **CreateBitmapBrush** consentono di specificare opzioni aggiuntive accettando una proprietà del [**\_ pennello d2d1 \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) e una struttura delle [**\_ \_ \_ proprietà del pennello bitmap d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



Nell'esempio seguente viene usato il pennello per riempire un rettangolo.


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>Configurazione delle modalità di estensione

In alcuni casi, la sfumatura di un pennello sfumatura o della bitmap per un pennello bitmap non riempie completamente l'area disegnata.

-   Quando si verifica questa situazione per un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D usa le impostazioni della modalità di estensione orizzontale ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) e verticale ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) del pennello per determinare come riempire l'area rimanente.

-   Quando si verifica questa situazione per un pennello sfumatura, Direct2D determina come riempire l'area rimanente usando il valore del parametro della [**\_ \_ modalità di estensione d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) specificato quando è stato chiamato il [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) per creare il [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)del pennello sfumatura.

Nella figura seguente sono illustrati i risultati di ogni possibile combinazione di modalità di estensione per un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (clamp), **d2d1 \_ extend \_ mode \_ Wrap** (wrap) e **d2d1 \_ extend \_ mirror** (mirror).

![illustrazione di un'immagine originale e delle immagini risultanti da varie modalità di estensione](images/bitmapwrap-clamp-mirror.png)

Nell'esempio seguente viene illustrato come impostare le modalità di estensione x e y del pennello bitmap su [**d2d1 \_ extend \_ mirror**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode). Disegna quindi il rettangolo con [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



Produce l'output come illustrato nella figura seguente.

![illustrazione di un'immagine originale e dell'immagine risultante dopo il mirroring della direzione x e della direzione y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>Trasformazione di pennelli

Quando si disegna con un pennello, dipinge nello spazio delle coordinate della destinazione di rendering. I pennelli non si posizionano automaticamente per allinearsi all'oggetto da disegnare; per impostazione predefinita, iniziano a disegnare nell'origine (0,0) della destinazione di rendering.

È possibile "spostare" la sfumatura definita da un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) in un'area di destinazione impostando il punto iniziale e il punto finale. Analogamente, è possibile spostare la sfumatura definita da un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando il relativo centro e i raggi.

Per allineare il contenuto di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) all'area da disegnare, è possibile usare il metodo [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) per convertire la bitmap nella posizione desiderata. Questa trasformazione influisca solo sul pennello. non influisce sugli altri contenuti creati dalla destinazione di rendering.

Nelle illustrazioni seguenti viene illustrato l'effetto dell'utilizzo di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per riempire un rettangolo situato in (100, 100). L'illustrazione nell'illustrazione a sinistra mostra il risultato del riempimento del rettangolo senza trasformare il pennello: la bitmap viene disegnata in corrispondenza dell'origine della destinazione di rendering. Di conseguenza, nel rettangolo viene visualizzata solo una parte della bitmap. L'illustrazione a destra mostra il risultato della trasformazione del **ID2D1BitmapBrush** in modo che il relativo contenuto venga spostato 50 pixel a destra e 50 pixel in basso. La bitmap riempie ora il rettangolo.

![illustrazione di un quadrato disegnato con un pennello bitmap senza trasformazione del pennello e trasformazione del pennello](images/brushes-ovw-transform.png)

Il codice seguente illustra come eseguire questa operazione. Per prima cosa applicare una traduzione al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), spostandolo il pennello 50 pixel lungo l'asse x e 50 pixel lungo l'asse y. Usare quindi **ID2D1BitmapBrush** per riempire il rettangolo con angolo superiore sinistro in (100, 100) e l'angolo inferiore destro in (200, 200).


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento Direct2D](reference.md)
* [Come creare un pennello tinta unita](how-to-create-a-solid-color-brush.md)
* [Come creare un pennello sfumato lineare](how-to-create-a-linear-gradient-brush.md)
* [Come creare un pennello sfumatura radiale](how-to-create-a-radial-gradient-brush.md)
* [Come creare un pennello bitmap](how-to-create-a-bitmap-brush.md)
