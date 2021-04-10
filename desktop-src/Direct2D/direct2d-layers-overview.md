---
title: Panoramica sui livelli
description: Descrive le nozioni di base dei livelli Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, livelli
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0e86b32296718a975ebabccd5fc4ef0ee30cf289
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963287"
---
# <a name="layers-overview"></a>Panoramica sui livelli

Questa panoramica descrive le nozioni di base sull'uso dei livelli Direct2D. Include le sezioni seguenti:

-   [Che cosa sono i livelli?](#what-are-layers)
-   [Livelli in Windows 8 e versioni successive](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext e PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ Layer \_ PARAMETERS1 e d2d1 \_ Layer \_ OPTIONS1](/windows)
    -   [Modalità di fusione](#blend-modes)
    -   [Interazione](#interoperation)
-   [Creazione di livelli](#creating-layers)
-   [Limiti del contenuto](#content-bounds)
-   [Maschere geometriche](#geometric-masks)
-   [Maschere di opacità](#opacity-masks)
-   [Alternative ai livelli](#alternatives-to-layers)
-   [Ritaglio di una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [Clip allineate asse](#axis-aligned-clips)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-layers"></a>Che cosa sono i livelli?

I livelli, rappresentati da oggetti [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , consentono a un'applicazione di modificare un gruppo di operazioni di disegno. Si usa un livello eseguendone il push in una destinazione di rendering. Le successive operazioni di disegno da parte della destinazione di rendering vengono indirizzate al livello. Una volta terminato il livello, si "estrae" il livello dalla destinazione di rendering, che compone nuovamente il contenuto del livello nella destinazione di rendering.

Analogamente ai pennelli, i livelli sono risorse dipendenti dal dispositivo create dalle destinazioni di rendering. I livelli possono essere usati in qualsiasi destinazione di rendering nello stesso dominio delle risorse che contiene la destinazione di rendering che l'ha creata. Tuttavia, una risorsa livello può essere usata solo da una destinazione di rendering alla volta. Per ulteriori informazioni sulle risorse, vedere [Panoramica delle risorse](resources-and-resource-domains.md).

Sebbene i livelli offrano una tecnica di rendering potente per produrre effetti interessanti, un numero eccessivo di livelli in un'applicazione può influire negativamente sulle prestazioni, a causa dei diversi costi associati alla gestione di livelli e risorse del livello. Ad esempio, il costo del riempimento o della cancellazione del livello e la successiva fusione, soprattutto sull'hardware di fascia superiore. Quindi, esiste il costo della gestione delle risorse del livello. Se questi vengono riallocati di frequente, i blocchi risultanti rispetto alla GPU saranno il problema più significativo. Quando si progetta un'applicazione, provare a massimizzare il riutilizzo delle risorse di livello.

## <a name="layers-in-windows-8-and-later"></a>Livelli in Windows 8 e versioni successive

In Windows 8 sono state introdotte nuove API correlate ai livelli che semplificano, migliorano le prestazioni di e aggiungono funzionalità a livelli.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext e PushLayer

L'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) è derivata dall'interfaccia [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) ed è fondamentale per visualizzare il contenuto Direct2D in Windows 8. per ulteriori informazioni su questa interfaccia, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md). Con l'interfaccia del contesto di dispositivo, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare null al metodo [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . Direct2D gestisce automaticamente la risorsa livello e può condividere le risorse tra i livelli e i grafici degli effetti.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ Layer \_ PARAMETERS1 e d2d1 \_ Layer \_ OPTIONS1

La [**struttura \_ \_ PARAMETERS1 di livello d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) è uguale a quella dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), ad eccezione del fatto che il membro finale della struttura è ora un'enumerazione [**d2d1 \_ Layer \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .

[**D2d1 \_ Il livello \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) non dispone di un'opzione ClearType e prevede due opzioni diverse che è possibile utilizzare per migliorare le prestazioni:

-   [**D2d1 \_ LIVELLO \_ OPTIONS1 \_ Inizializza \_ da \_ background**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D esegue il rendering delle primitive nel livello senza cancellarlo con un nero trasparente. Questo non è il valore predefinito, ma nella maggior parte dei casi produce prestazioni migliori.

-   [**D2d1 \_ LAYER \_ OPTIONS1 \_ Ignore \_ Alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): se la superficie sottostante è impostata su [**d2d1 \_ Alpha \_ mode \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), questa opzione consente a Direct2D di evitare di modificare il canale alfa del livello. Non utilizzarlo in altri casi.

### <a name="blend-modes"></a>Modalità di fusione

A partire da Windows 8, il contesto di dispositivo ha una [**modalità di Blend primitiva**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) che determina il modo in cui ogni primitiva viene fusa con la superficie di destinazione. Questa modalità si applica anche ai livelli quando si chiama il metodo [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .

Se, ad esempio, si usa un livello per ritagliare le primitive con trasparenza, impostare la modalità di [**\_ \_ \_ copia primitiva di d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) nel contesto di dispositivo per ottenere risultati appropriati. La modalità di copia rende il contesto di dispositivo lineare interpolare tutti i 4 canali dei colori, incluso il canale alfa, di ogni pixel con il contenuto della superficie di destinazione in base alla maschera geometrica del livello.

### <a name="interoperation"></a>Interazione

A partire da Windows 8, Direct2D supporta l'interoperabilità con Direct3D e GDI mentre viene eseguito il push di un livello o di una clip. È possibile chiamare [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) mentre viene eseguito il push di un livello per interagire con GDI. È possibile chiamare [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) e quindi eseguire il rendering sulla superficie sottostante per interagire con Direct3D. È responsabilità dell'utente eseguire il rendering all'interno del livello o della clip con Direct3D o GDI. Se si tenta di eseguire il rendering al di fuori del livello o di ritagliare i risultati non sono definiti.

## <a name="creating-layers"></a>Creazione di livelli

Per lavorare con i livelli è necessaria una certa familiarità con i metodi [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) e con la struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , che contiene un set di dati parametrici che definiscono il modo in cui è possibile utilizzare il livello. Nell'elenco seguente vengono descritti i metodi e la struttura.

-   Chiamare il metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) per creare una risorsa livello.
    > [!Note]  
    > A partire da Windows 8, è possibile ignorare la chiamata al metodo [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e quindi passare null al metodo [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) sull'interfaccia [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) . Si tratta di una soluzione più semplice che consente a Direct2D di gestire automaticamente la risorsa di livello e di condividere le risorse tra i livelli e i grafici di effetto.

     

-   Dopo che la destinazione di rendering ha iniziato a disegnare (dopo che è stato chiamato il metodo [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ), è possibile usare il metodo [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . Il metodo **PushLayer** aggiunge il livello specificato alla destinazione di rendering, in modo che la destinazione riceva tutte le operazioni di disegno successive fino a quando non viene chiamato [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . Questo metodo accetta un oggetto [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) restituito chiamando [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e un *layerParameters* nella struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) . Nella tabella seguente vengono descritti i campi della struttura. 

    | Campo                 | Descrizione                                                                                                                                                                                                                                                                 |     |
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
    | **contentBounds**     | Limiti del contenuto del livello. Non è garantito il rendering del contenuto al di fuori di questi limiti. Il valore predefinito di questo parametro è [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Quando viene utilizzato il valore predefinito, i limiti del contenuto vengono effettivamente considerati i limiti della destinazione di rendering. |     |
    | **geometricMask**     | Opzionale Area, definita da un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), a cui deve essere ritagliato il livello. Impostare su **null** se il livello non deve essere ritagliato in una geometria.                                                                                           |     |
    | **maskAntialiasMode** | Valore che specifica la modalità di anti-aliasing per la maschera geometrica specificata dal campo **geometricMask** .                                                                                                                                                               |     |
    | **maskTransform**     | Valore che specifica la trasformazione applicata alla maschera geometrica quando si compone il livello. Questa operazione è relativa alla trasformazione globale.                                                                                                                               |     |
    | **opacità**           | Valore di opacità del livello. L'opacità di ogni risorsa nel livello viene moltiplicata con questo valore durante la composizione della destinazione.                                                                                                                                     |     |
    | **opacityBrush**      | Opzionale Pennello usato per modificare l'opacità del livello. Il pennello viene mappato al livello e il canale alfa di ogni pixel del pennello mappato viene moltiplicato per il pixel del livello corrispondente. Impostare su **null** se il livello non deve avere una maschera di opacità.    |     |
    | **layerOptions**      | Valore che specifica se il livello intende eseguire il rendering del testo con anti-aliasing ClearType. Per impostazione predefinita, questo parametro è disattivato. La sua attivazione consente il corretto funzionamento di ClearType, ma comporta una velocità di rendering leggermente più lenta.                                          |     |

    

     

    > [!Note]  
    > A partire da Windows 8, non è possibile eseguire il rendering con ClearType in un livello, quindi il parametro **layerOptions** deve essere sempre impostato su [**d2d1 \_ Layer \_ Options \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    Per praticità, Direct2D fornisce il metodo [**D2D1:: LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) per semplificare la creazione di strutture di [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .

-   Per comporre il contenuto del livello nella destinazione di rendering, chiamare il metodo [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) . Prima di chiamare il metodo [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , è necessario chiamare il metodo **PopLayer** .

Nell'esempio seguente viene illustrato come utilizzare [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer). Tutti i campi nella struttura dei [**\_ \_ parametri del livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sono impostati sulle impostazioni predefinite, ad eccezione di **opacityBrush**, che è impostato su un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).


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

Si noti che quando si chiamano [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), assicurarsi che ogni **PushLayer** disponga di una chiamata **PopLayer** corrispondente. Se sono presenti più chiamate **PopLayer** rispetto alle chiamate di **PushLayer** , la destinazione di rendering viene inserita in uno stato di errore. Se [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) viene chiamato prima che vengano estratti tutti i livelli in attesa, la destinazione di rendering viene inserita in uno stato di errore e restituisce un errore. Per cancellare lo stato di errore, usare [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Limiti del contenuto

**ContentBounds** imposta il limite di elementi da disegnare sul livello. Solo gli elementi all'interno dei limiti del contenuto vengono ricomposti alla destinazione di rendering.

Nell'esempio seguente viene illustrato come specificare **ContentBounds** in modo che l'immagine originale venga ritagliata nei limiti del contenuto con l'angolo superiore sinistro in corrispondenza di (10, 108) e l'angolo inferiore destro in (121, 177). Nella figura seguente viene illustrata l'immagine originale e il risultato del ritaglio dell'immagine ai limiti del contenuto.

![illustrazione dei limiti del contenuto in un'immagine originale e nell'immagine ritagliata risultante](images/layers-contentbounds.png)


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
> L'immagine ritagliata risultante viene interessata ulteriormente se si specifica un **geometricMask**. Per ulteriori informazioni, vedere la sezione [maschere geometriche](#geometric-masks) .

 

## <a name="geometric-masks"></a>Maschere geometriche

Una maschera geometrica è una clip o un ritaglio, definito da un oggetto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , che maschera un livello quando viene disegnato da una destinazione di rendering. È possibile usare il campo **geometricMask** della struttura [**\_ \_ parametri livello d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) per mascherare i risultati in una geometria. Se, ad esempio, si desidera visualizzare un'immagine mascherata da una lettera di blocco "A", è possibile creare innanzitutto una geometria che rappresenta la lettera di blocco "A" e utilizzare tale geometria come maschera geometrica per un livello. Quindi, dopo aver eseguito il push del livello, è possibile creare l'immagine. Se si schiocca il livello, l'immagine viene ritagliata nella forma della lettera di blocco "A".

Nell'esempio seguente viene illustrato come creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) contenente una forma di una montagna, quindi passare la geometria del percorso al [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)). Quindi disegna una bitmap e i quadrati. Se è presente solo una bitmap nel livello di cui eseguire il rendering, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap bloccato per migliorare l'efficienza. L'immagine seguente illustra l'output dell'esempio.

![illustrazione di un'immagine di una foglia e dell'immagine risultante dopo che è stata applicata una maschera geometrica di una montagna](images/layers-bitmapmask.png)

Nel primo esempio viene definita la geometria da utilizzare come maschera.


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



Nell'esempio seguente viene usata la geometria come maschera per il livello.


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
> In generale, se si specifica un **geometricMask**, è possibile usare il valore predefinito [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)per **ContentBounds**.
>
> Se **ContentBounds** è null e **geometricMask** è diverso da null, i limiti del contenuto sono in effetti i limiti della maschera geometrica dopo l'applicazione della trasformazione della maschera.
>
> Se **ContentBounds** è diverso da null e **geometricMask** è diverso da null, la maschera geometrica trasformata viene effettivamente ritagliata rispetto ai limiti del contenuto e si presuppone che i limiti del contenuto siano infiniti.

 

## <a name="opacity-masks"></a>Maschere di opacità

Una maschera di opacità è una maschera, descritta da un pennello o una bitmap, applicata a un altro oggetto per rendere tale oggetto parzialmente o completamente trasparente. Consente di utilizzare il canale alfa di un pennello da utilizzare come maschera di contenuto. Ad esempio, è possibile definire un pennello a sfumatura radiale che varia da opaco a trasparente per creare un effetto vignette.

Nell'esempio seguente viene usato un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) come maschera di opacità. Quindi disegna una bitmap e i quadrati. Se è presente solo una bitmap nel livello di cui eseguire il rendering, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap bloccato per migliorare l'efficienza. La figura seguente mostra l'output di questo esempio.

![illustrazione di un'immagine di alberi e dell'immagine risultante dopo l'applicazione di una maschera di opacità](images/layers-opacitymask.png)


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
> Questo esempio usa un livello per applicare una maschera di opacità a un singolo oggetto per rendere l'esempio il più semplice possibile. Quando si applica una maschera di opacità a un singolo oggetto, è più efficiente usare i metodi [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) o [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) anziché un livello.

 

Per istruzioni su come applicare una maschera di opacità senza usare un livello, vedere [Cenni preliminari sulle maschere di opacità](opacity-masks-overview.md).

## <a name="alternatives-to-layers"></a>Alternative ai livelli

Come indicato in precedenza, un numero eccessivo di livelli può influire negativamente sulle prestazioni dell'applicazione. Per migliorare le prestazioni, evitare di usare i livelli laddove possibile; usare invece le alternative. Nell'esempio di codice seguente viene illustrato come utilizzare [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) per ritagliare un'area, in alternativa all'utilizzo di un livello con limiti di contenuto.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



Analogamente, usare [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello bitmap clampato come alternativa all'uso di un livello con una maschera di opacità quando è presente un solo contenuto del livello di cui eseguire il rendering, come illustrato nell'esempio seguente.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



In alternativa all'uso di un livello con una maschera geometrica, provare a usare una maschera di bitmap per ritagliare un'area, come illustrato nell'esempio seguente.


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



Infine, se si desidera applicare l'opacità a una singola primitiva, è necessario moltiplicare l'opacità nell'oggetto nel colore del pennello e quindi eseguire il rendering della primitiva. Non è necessario un livello o una bitmap maschera di opacità.


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

La figura seguente mostra il risultato dell'applicazione di una clip a un'immagine.

![immagine che mostra un esempio di immagine prima e dopo un clip.](images/clip.png)

È possibile ottenere questo risultato usando i livelli con una maschera di geometria o il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pennello di opacità.

Di seguito è riportato un esempio che usa un livello:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Di seguito è riportato un esempio che usa il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


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



In questo esempio di codice, quando si chiama il metodo PushLayer, non si passa un livello creato dall'app. Direct2D crea automaticamente un livello. Direct2D è in grado di gestire l'allocazione e l'eliminazione di questa risorsa senza alcun intervento da parte dell'app. Questo consente a Direct2D di riutilizzare i livelli internamente e di applicare le ottimizzazioni di gestione delle risorse.

> [!Note]  
> In Windows 8 sono state apportate numerose ottimizzazioni all'utilizzo dei livelli ed è consigliabile provare a usare le API di livello anziché [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) quando possibile.

 

### <a name="axis-aligned-clips"></a>Clip allineate asse

Se l'area da ritagliare è allineata all'asse della superficie di disegno, anziché arbitraria. Questo caso è adatto per l'utilizzo di un rettangolo di ritaglio anziché di un livello. Il miglioramento delle prestazioni è maggiore per la geometria con alias rispetto alla geometria con alias. Per altre informazioni sulle clip allineate asse, vedere l'argomento [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Direct2D](reference.md)
</dt> </dl>

 

 