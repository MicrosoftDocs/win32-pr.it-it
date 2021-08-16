---
title: Panoramica dei livelli
description: Descrive le nozioni di base dei livelli Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, livelli
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a54c5336b26d2b84f46df4f688101367686d3dbe60be33d8bac5d8c584151daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825713"
---
# <a name="layers-overview"></a>Panoramica dei livelli

Questa panoramica descrive le nozioni di base sull'uso dei livelli Direct2D. Include le sezioni seguenti:

-   [Che cosa sono i livelli?](#what-are-layers)
-   [Livelli in Windows 8 e versioni successive](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext e PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ LAYER \_ PARAMETERS1 e D2D1 \_ LAYER \_ OPTIONS1](/windows)
    -   [Modalità di fusione](#blend-modes)
    -   [Interazione](#interoperation)
-   [Creazione di livelli](#creating-layers)
-   [Limiti di contenuto](#content-bounds)
-   [Maschere geometriche](#geometric-masks)
-   [Maschere di opacità](#opacity-masks)
-   [Alternative ai livelli](#alternatives-to-layers)
-   [Ritaglio di una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [Clip allineate all'asse](#axis-aligned-clips)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-layers"></a>Che cosa sono i livelli?

I livelli, rappresentati da [**oggetti ID2D1Layer,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) consentono a un'applicazione di modificare un gruppo di operazioni di disegno. È possibile usare un livello "push" su una destinazione di rendering. Le operazioni di disegno successive da parte della destinazione di rendering vengono indirizzate al livello. Dopo aver completato il livello, si "pop" il livello dalla destinazione di rendering, che composito il contenuto del livello alla destinazione di rendering.

Analogamente ai pennelli, i livelli sono risorse dipendenti dal dispositivo create dalle destinazioni di rendering. I livelli possono essere usati in qualsiasi destinazione di rendering nello stesso dominio di risorse che contiene la destinazione di rendering che la ha creata. Tuttavia, una risorsa livello può essere usata solo da una destinazione di rendering alla volta. Per altre informazioni sulle risorse, vedere Panoramica [delle risorse](resources-and-resource-domains.md).

Anche se i livelli offrono una potente tecnica di rendering per produrre effetti interessanti, un numero eccessivo di livelli in un'applicazione può influire negativamente sulle prestazioni, a causa dei vari costi associati alla gestione dei livelli e delle risorse del livello. Ad esempio, è necessario riempire o cancellare il livello e quindi combinarlo nuovamente, in particolare nell'hardware di fascia superiore. È quindi necessario gestire le risorse del livello. Se si riallocano questi elementi di frequente, il problema più significativo sarà lo stallo risultante rispetto alla GPU. Quando si progetta l'applicazione, provare a ottimizzare il riutilizzo delle risorse del livello.

## <a name="layers-in-windows-8-and-later"></a>Livelli in Windows 8 e versioni successive

Windows 8 sono state introdotte nuove API correlate ai livelli che semplificano, migliorano le prestazioni di e aggiungono funzionalità ai livelli.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext e PushLayer

[**L'interfaccia ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) deriva dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) ed è fondamentale per visualizzare il contenuto Direct2D in Windows 8. Per altre informazioni su questa interfaccia, vedere [Dispositivi](devices-and-device-contexts.md)e contesti di dispositivo . Con l'interfaccia del contesto di dispositivo, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare NULL al metodo [**ID2D1DeviceContext::P ushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) Direct2D gestisce automaticamente la risorsa livello e può condividere le risorse tra i livelli e i grafici degli effetti.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ LAYER \_ PARAMETERS1 e D2D1 \_ LAYER \_ OPTIONS1

La [**struttura D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) è uguale a [**D2D1 \_ LAYER \_ PARAMETERS,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)ad eccezione del fatto che il membro finale della struttura è ora [**un'enumerazione D2D1 \_ LAYER \_ OPTIONS1.**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)

[**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) non ha l'opzione ClearType e ha due diverse opzioni che è possibile usare per migliorare le prestazioni:

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D esegue il rendering delle primitive al livello senza cancellarlo con il nero trasparente. Questa non è l'impostazione predefinita, ma nella maggior parte dei casi comporta prestazioni migliori.

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ IGNORE \_ ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): se la superficie sottostante è impostata su [**D2D1 \_ ALPHA MODE \_ \_ IGNORE,**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)questa opzione consente a Direct2D di evitare di modificare il canale alfa del livello. Non usarlo in altri casi.

### <a name="blend-modes"></a>Modalità di fusione

A partire Windows 8, il contesto di dispositivo ha una modalità di blend [**primitiva**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) che determina la modalità di fusione di ogni primitiva con la superficie di destinazione. Questa modalità si applica anche ai livelli quando si chiama il [**metodo PushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))

Ad esempio, se si usa un livello per ritagliare primitive con trasparenza, impostare la modalità [**D2D1 \_ PRIMITIVE \_ BLEND \_ COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) nel contesto di dispositivo per ottenere risultati corretti. La modalità di copia rende lineare il contesto di dispositivo interpolando tutti e 4 i canali di colore, incluso il canale alfa, di ogni pixel con il contenuto della superficie di destinazione in base alla maschera geometrica del livello.

### <a name="interoperation"></a>Interazione

A partire da Windows 8, Direct2D supporta l'interoperabilità con Direct3D e GDI durante il push di un livello o di un clip. Si chiama [**ID2D1GdiInteropRenderTarget::GetDC mentre**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) viene inserito un livello per interagire con GDI. Chiamare [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) e quindi eseguire il rendering sulla superficie sottostante per interagire con Direct3D. È responsabilità dell'utente eseguire il rendering all'interno del livello o del clip con Direct3D o GDI. Se si tenta di eseguire il rendering all'esterno del livello o di ritagliare i risultati non sono definiti.

## <a name="creating-layers"></a>Creazione di livelli

L'uso dei livelli richiede familiarità con i metodi [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) e con la struttura [**D2D1 \_ LAYER \_ PARAMETERS,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) che contiene un set di dati parametrici che definisce come usare il livello. Nell'elenco seguente vengono descritti i metodi e la struttura .

-   Chiamare il [**metodo CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare una risorsa di livello.
    > [!Note]  
    > A partire Windows 8, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare NULL al metodo [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) nell'interfaccia [**ID2D1DeviceContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Questo approccio è più semplice e consente a Direct2D di gestire automaticamente la risorsa del livello e di condividere le risorse tra i livelli e i grafici degli effetti.

     

-   Dopo che la destinazione di rendering ha iniziato a disegnare (dopo la chiamata al metodo [**BeginDraw),**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) è possibile usare il [**metodo PushLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) Il **metodo PushLayer** aggiunge il livello specificato alla destinazione di rendering, in modo che la destinazione riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) Questo metodo accetta un [**oggetto ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) restituito chiamando [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e *un oggetto layerParameters* nella [**struttura D2D1 \_ LAYER \_ PARAMETERS.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) Nella tabella seguente vengono descritti i campi della struttura . 

    | Campo                 | Descrizione|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **contentBounds**     | Limiti di contenuto del livello. Il rendering del contenuto non viene eseguito al di fuori di questi limiti. Il valore predefinito di questo parametro [**è InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Quando viene usato il valore predefinito, i limiti di contenuto vengono effettivamente usati come limiti della destinazione di rendering. |
    | **geometricMask**     | (Facoltativo) Area, definita da [**id2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)a cui deve essere ritagliato il livello. Impostare su **NULL** se il livello non deve essere ritagliato in una geometria. |
    | **maskAntialiasMode** | Valore che specifica la modalità di antialias per la maschera geometrica specificata dal **campo geometricMask.** |
    | **maskTransform**     | Valore che specifica la trasformazione applicata alla maschera geometrica durante la composizione del livello. Questo valore è relativo alla trasformazione del mondo.  |
    | **Opacità**           | Valore di opacità del livello. L'opacità di ogni risorsa nel livello viene moltiplicata con questo valore durante la composizione nella destinazione.  |
    | **opacityBrush**      | (Facoltativo) Pennello usato per modificare l'opacità del livello. Il pennello viene mappato al livello e il canale alfa di ogni pixel del pennello mappato viene moltiplicato rispetto al pixel del livello corrispondente. Impostare su **NULL se** il livello non deve avere una maschera di opacità.   |
    | **layerOptions**      | Valore che specifica se il livello intende eseguire il rendering del testo con l'antialiasing ClearType. Per impostazione predefinita, questo parametro è disattivato. L'attivazione consente il corretto funzionamento di ClearType, ma comporta una velocità di rendering leggermente più lenta.    |

    

     

    > [!Note]  
    > A partire Windows 8, non è possibile eseguire il rendering con ClearType in un livello, pertanto il **parametro layerOptions** deve essere sempre impostato su [**D2D1 \_ LAYER OPTIONS \_ \_ NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    Per praticità, Direct2D fornisce il [**metodo D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) che consente di creare strutture [**D2D1 \_ LAYER \_ PARAMETERS.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)

-   Per creare un composito del contenuto del livello nella destinazione di rendering, chiamare il [**metodo PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) È necessario chiamare il **metodo PopLayer** prima di chiamare il [**metodo EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)

Nell'esempio seguente viene illustrato come [**usare CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer). Tutti i campi nella struttura [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sui valori predefiniti, ad eccezione di **opacityBrush**, che è impostato su [**ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)


```C++
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
```



Il codice è stato omesso da questo esempio.

Si noti che quando si chiamano [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), assicurarsi che ogni **PushLayer** abbia una **chiamata PopLayer** corrispondente. Se sono presenti più **chiamate PopLayer** rispetto alle **chiamate PushLayer,** la destinazione di rendering viene inserita in uno stato di errore. Se [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato prima che tutti i livelli in sospeso siano visualizzati, la destinazione di rendering viene inserita in uno stato di errore e restituisce un errore. Per cancellare lo stato di errore, [**usare EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Limiti di contenuto

**contentBounds** imposta il limite di ciò che deve essere disegnato sul livello. Solo gli elementi all'interno dei limiti di contenuto vengono compositi nella destinazione di rendering.

L'esempio seguente illustra come specificare **contentBounds** in modo che l'immagine originale sia ritagliata ai limiti del contenuto con l'angolo superiore sinistro in corrispondenza di (10, 108) e l'angolo inferiore destro in corrispondenza di (121, 177). La figura seguente mostra l'immagine originale e il risultato del ritaglio dell'immagine ai limiti del contenuto.

![Illustrazione dei limiti di contenuto in un'immagine originale e dell'immagine ritagliata risultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



Il codice è stato omesso da questo esempio.

> [!Note]
>
> L'immagine ritagliata risultante è ulteriormente interessata se si specifica **un oggetto geometricMask**. Per altre [informazioni, vedere](#geometric-masks) la sezione Maschere geometriche.

 

## <a name="geometric-masks"></a>Maschere geometriche

Una maschera geometrica è una clip o un ritaglio, definito da un [**oggetto ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) che maschera un livello quando viene disegnato da una destinazione di rendering. È possibile usare il **campo geometricMask** della struttura [**D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) per mascherare i risultati in una geometria. Ad esempio, se si vuole visualizzare un'immagine mascherata da una lettera a blocchi "A", è prima possibile creare una geometria che rappresenta la lettera a blocchi "A" e usare tale geometria come maschera geometrica per un livello. Quindi, dopo aver spinto il livello, è possibile disegnare l'immagine. Se si fa clic sul livello, l'immagine viene ritagliata nella forma "A" a blocchi.

L'esempio seguente illustra come creare un [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) contenente una forma di una cima e quindi passare la geometria del percorso a [**PushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) Disegna quindi una bitmap e quadrati. Se è presente solo una bitmap nel livello di cui eseguire il rendering, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap con chiusura per migliorare l'efficienza. L'immagine seguente illustra l'output dell'esempio.

![illustrazione di un'immagine di una foglia e dell'immagine risultante dopo l'applicazione di una maschera geometrica di una monta](images/layers-bitmapmask.png)

Il primo esempio definisce la geometria da usare come maschera.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



L'esempio successivo usa la geometria come maschera per il livello.


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

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



Il codice è stato omesso da questo esempio.

> [!Note]
>
> In generale, se si specifica **un oggetto geometricMask**, è possibile usare il valore [**predefinito, InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), per **contentBounds**.
>
> Se **contentBounds** è NULL e **geometricMask** è diverso da NULL, i limiti di contenuto sono effettivamente i limiti della maschera geometrica dopo l'applicazione della trasformazione maschera.
>
> Se **contentBounds** è diverso da NULL e **geometricMask** è diverso da NULL, la maschera geometrica trasformata viene ritagliata in modo efficace rispetto ai limiti di contenuto e si presuppone che i limiti di contenuto siano infiniti.

 

## <a name="opacity-masks"></a>Maschere di opacità

Una maschera di opacità è una maschera, descritta da un pennello o da una bitmap, applicata a un altro oggetto per rendere l'oggetto parzialmente o completamente trasparente. Consente di usare il canale alfa di un pennello come maschera di contenuto. Ad esempio, è possibile definire un pennello sfumatura radiale che varia da opaco a trasparente per creare un effetto di vignetta.

L'esempio seguente usa [**id2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) come maschera di opacità. Disegna quindi una bitmap e quadrati. Se è presente solo una bitmap nel livello di cui eseguire il rendering, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap con chiusura per migliorare l'efficienza. Nella figura seguente viene illustrato l'output di questo esempio.

![illustrazione di un'immagine degli alberi e dell'immagine risultante dopo l'applicazione di una maschera di opacità](images/layers-opacitymask.png)


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



Il codice è stato omesso da questo esempio.

> [!Note]  
> Questo esempio usa un livello per applicare una maschera di opacità a un singolo oggetto per mantenere l'esempio il più semplice possibile. Quando si applica una maschera di opacità a un singolo oggetto, è più efficiente usare i metodi [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) [**o FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) anziché un livello.

 

Per istruzioni su come applicare una maschera di opacità senza usare un livello, vedere Panoramica delle maschere [di opacità.](opacity-masks-overview.md)

## <a name="alternatives-to-layers"></a>Alternative ai livelli

Come accennato in precedenza, un numero eccessivo di livelli può influire negativamente sulle prestazioni dell'applicazione. Per migliorare le prestazioni, evitare di usare i livelli quando possibile; usare invece le alternative. L'esempio di codice seguente illustra come usare [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per ritagliare un'area, in alternativa all'uso di un livello con limiti di contenuto.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



Analogamente, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap con chiusura come alternativa all'uso di un livello con una maschera di opacità quando è presente un solo contenuto nel livello di cui eseguire il rendering, come illustrato nell'esempio seguente.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



In alternativa all'uso di un livello con una maschera geometrica, è consigliabile usare una maschera bitmap per ritagliare un'area, come illustrato nell'esempio seguente.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Infine, se si vuole applicare l'opacità a una singola primitiva, è necessario moltiplicare l'opacità in nel colore del pennello e quindi eseguire il rendering della primitiva. Non è necessario un livello o una bitmap della maschera di opacità.


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>Ritaglio di una forma arbitraria

La figura seguente mostra il risultato dell'applicazione di un clip a un'immagine.

![immagine che mostra un esempio di immagine prima e dopo un clip.](images/clip.png)

È possibile ottenere questo risultato usando i livelli con una maschera geometrica o il [**metodo FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello di opacità.

Ecco un esempio che usa un livello:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Ecco un esempio che usa il [**metodo FillGeometry:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



In questo esempio di codice, quando si chiama il metodo PushLayer, non si passa un livello creato dall'app. Direct2D crea automaticamente un livello. Direct2D è in grado di gestire l'allocazione e la distruzione di questa risorsa senza alcun coinvolgimento dell'app. In questo modo Direct2D può riutilizzare i livelli internamente e applicare le ottimizzazioni di gestione delle risorse.

> [!Note]  
> In Windows 8 sono state apportate molte ottimizzazioni all'uso dei livelli ed è consigliabile provare a usare le API dei livelli anziché [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) quando possibile.

 

### <a name="axis-aligned-clips"></a>Clip allineate all'asse

Se l'area da ritagliare è allineata all'asse della superficie di disegno, anziché arbitraria. Questo caso è adatto per l'uso di un rettangolo di ritaglio anziché di un livello. Il miglioramento delle prestazioni è più per la geometria con alias che per la geometria con antialias. Per altre informazioni sulle clip allineate all'asse, vedere [**l'argomento PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Direct2D](reference.md)
</dt> </dl>

 

 