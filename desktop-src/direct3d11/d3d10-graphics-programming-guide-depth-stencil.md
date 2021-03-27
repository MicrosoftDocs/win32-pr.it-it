---
title: Configurazione della funzionalità Depth-Stencil
description: In questa sezione vengono illustrati i passaggi per configurare il buffer di stencil Depth e lo stato depth-stencil per la fase di Unione dell'output.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728743"
---
# <a name="configuring-depth-stencil-functionality"></a>Configurazione della funzionalità Depth-Stencil

In questa sezione vengono illustrati i passaggi per configurare il buffer di stencil Depth e lo stato depth-stencil per la fase di Unione dell'output.

-   [Creare una risorsa Depth-Stencil](#create-a-depth-stencil-resource)
-   [Crea stato Depth-Stencil](#create-depth-stencil-state)
-   [Associare i dati Depth-Stencil alla fase OM](#bind-depth-stencil-data-to-the-om-stage)

Quando si è a conoscenza di come utilizzare il buffer di stencil Depth e lo stato di stencil Depth corrispondente, fare riferimento alle [tecniche di stencil avanzati](#advanced-stencil-techniques).

## <a name="create-a-depth-stencil-resource"></a>Creare una risorsa Depth-Stencil

Creare il buffer di stencil Depth usando una risorsa di trama.


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a>Crea stato Depth-Stencil

Lo stato depth-stencil indica alla fase di Unione dell'output come eseguire il [test di stencil di profondità](d3d10-graphics-programming-guide-output-merger-stage.md). Il test di stencil Depth determina se deve essere disegnato o meno un pixel specificato.


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



DepthEnable e StencilEnable abilitano (e disabilitano) la profondità e il test di stencil. Impostare DepthEnable su **false** per disabilitare il test di profondità e impedire la scrittura nel buffer di profondità. Impostare StencilEnable su **false** per disabilitare il test dello stencil e impedire la scrittura nel buffer dello stencil. quando DepthEnable è **false** e StencilEnable è **true**, il test di profondità passa sempre nell'operazione dello stencil.

DepthEnable influisce solo sulla fase di Unione dell'output. non influisce sul ritaglio, sulla distorsione della profondità o sul fissaggio dei valori prima che i dati vengano inseriti in un pixel shader.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Associare i dati Depth-Stencil alla fase OM

Associare lo stato di stencil Depth.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Associare la risorsa stencil Depth utilizzando una visualizzazione.


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



Una matrice di visualizzazioni di destinazione di rendering può essere passata in [**sul ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), tuttavia tutte le visualizzazioni di destinazione di rendering corrisponderanno a una singola vista depth stencil. La matrice di destinazione di rendering in Direct3D 11 è una funzionalità che consente a un'applicazione di eseguire il rendering simultaneamente su più destinazioni di rendering a livello primitivo. Le matrici di destinazione di rendering offrono prestazioni migliori rispetto all'impostazione individuale di destinazioni di rendering con più chiamate a **sul ID3D11DeviceContext:: OMSetRenderTargets** (essenzialmente il metodo utilizzato in Direct3D 9).

Le destinazioni di rendering devono essere tutte dello stesso tipo di risorsa. Se viene usato l'anti-aliasing di multicampionamento, tutti gli obiettivi di rendering associati e i buffer di profondità devono avere gli stessi conteggi di esempio.

Quando un buffer viene usato come destinazione di rendering, i test di stencil Depth e più destinazioni di rendering non sono supportati.

-   Fino a 8 destinazioni di rendering possono essere associati simultaneamente.
-   Tutte le destinazioni di rendering devono avere le stesse dimensioni in tutte le dimensioni (larghezza e altezza e profondità per la dimensione 3D o della matrice per i \* tipi di matrice).
-   Ogni destinazione di rendering può avere un formato dati diverso.
-   Write Masks consente di controllare quali dati vengono scritti in una destinazione di rendering. Il controllo Write mask di output in una destinazione per rendering, a livello di componente, i dati vengono scritti nelle destinazioni di rendering.

## <a name="advanced-stencil-techniques"></a>Tecniche avanzate degli stencil

La parte stencil del buffer di stencil depth può essere usata per creare effetti di rendering, ad esempio composizione, derivazione e struttura.

-   [Composizione](#compositing)
-   [Decaing](#decaling)
-   [Strutture e sagome](#outlines-and-silhouettes)
-   [Stencil a due lati](#two-sided-stencil)
-   [Lettura del buffer Depth-Stencil come trama](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Composizione

L'applicazione può usare il buffer dello stencil per le immagini 2D o 3D composite su una scena 3D. Una maschera nel buffer dello stencil viene utilizzata per occludere un'area della superficie di destinazione del rendering. Le informazioni 2D archiviate, ad esempio testo o bitmap, possono quindi essere scritte nell'area. In alternativa, l'applicazione è in grado di eseguire il rendering di primitive 3D nell'area mascherata dallo stencil della superficie di destinazione per il rendering. È anche possibile eseguire il rendering di un'intera scena.

I giochi spesso compostano contemporaneamente più scene 3D. Ad esempio, per la guida dei giochi viene in genere visualizzato un mirror di visualizzazione posteriore. Il mirror contiene la visualizzazione della scena 3D dietro il driver. Si tratta essenzialmente di una seconda scena 3D composita con la visualizzazione in diretta del driver.

### <a name="decaling"></a>Decaing

Le applicazioni Direct3D usano il decaing per controllare quali pixel di una determinata immagine primitiva vengono disegnati nell'area di destinazione del rendering. Le applicazioni applicano le decalcomanie alle immagini delle primitive per consentire il rendering corretto dei poligoni complanari.

Ad esempio, quando si applicano segni di pneumatico e linee gialle a una carreggiata, i contrassegni devono essere visualizzati direttamente sopra la strada. Tuttavia, i valori z dei contrassegni e della strada sono gli stessi. Il buffer di profondità potrebbe pertanto non produrre una netta separazione tra i due. È possibile che venga eseguito il rendering di alcuni pixel della primitiva in primo piano sulla primitiva e viceversa. L'immagine risultante sembra riflessi da frame a frame. Questo effetto è detto z-Fighting o flimmering.

Per risolvere questo problema, usare uno stencil per mascherare la sezione della primitiva di sfondo in cui verrà visualizzata la decalcomania. Disattivare la memorizzazione nel buffer z ed eseguire il rendering dell'immagine della primitiva di primo piano nell'area nascosta della superficie di destinazione di rendering.

Per risolvere questo problema, è possibile usare più miscele di trame.

### <a name="outlines-and-silhouettes"></a>Strutture e sagome

È possibile utilizzare il buffer dello stencil per gli effetti più astratti, ad esempio la struttura e silhouetting.

Se l'applicazione esegue due passaggi di rendering, uno per generare la maschera dello stencil e il secondo per applicare la maschera dello stencil all'immagine, ma con le primitive leggermente più piccole alla seconda sessione, l'immagine risultante conterrà solo il contorno della primitiva. L'applicazione può quindi riempire l'area con maschera di stencil dell'immagine con un colore a tinta unita, assegnando alla primitiva un aspetto in rilievo.

Se la maschera dello stencil ha le stesse dimensioni e la stessa forma della primitiva di cui si sta eseguendo il rendering, l'immagine risultante contiene un foro in cui la primitiva deve essere. L'applicazione può quindi riempire il foro con il nero per produrre una silhouette della primitiva.

### <a name="two-sided-stencil"></a>Stencil Two-Sided

I volumi shadow vengono utilizzati per disegnare le ombre con il buffer dello stencil. Tramite l'applicazione vengono calcolati i volumi shadow di cui viene eseguito il cast dalla geometria occlusione, calcolando i bordi della siluetta e estrattando i bordi dalla luce in un set di volumi 3D. Questi volumi vengono quindi sottoposti a rendering due volte nel buffer dello stencil.

Il primo rendering disegna i poligoni rivolte verso il futuro e incrementa i valori del buffer dello stencil. Il secondo oggetto render disegna i poligoni sul retro del volume shadow e decrementa i valori del buffer dello stencil. In genere, tutti i valori incrementati e decrementati vengono annullati. Tuttavia, la scena è già stata sottoposta a rendering con la geometria normale causando la mancata riuscita del test del buffer z durante il rendering del volume shadow. I valori rimanenti nel buffer dello stencil corrispondono ai pixel presenti nell'ombreggiatura. Questi rimanenti contenuti del buffer dello stencil vengono usati come maschera, per alfa-blend di un quadrato nero di grandi dimensioni, che include tutto il doppio nella scena. Con il buffer dello stencil che funge da maschera, il risultato è quello di scurire i pixel presenti nelle ombreggiature.

Ciò significa che la geometria dell'ombreggiatura viene disegnata due volte per ogni sorgente di luce, di conseguenza la pressione sulla velocità effettiva del vertice della GPU. La funzionalità stencil a due lati è stata progettata per attenuare questa situazione. In questo approccio sono disponibili due set di stato dello stencil, denominati di seguito, uno per i triangoli in primo piano e l'altro per i triangoli rivolti verso il retro. In questo modo viene disegnato un solo passaggio per ogni volume ombreggiato, per luce.

Un esempio di implementazione di stencil a due lati è disponibile nell' [esempio ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Lettura del buffer Depth-Stencil come trama

Un buffer di stencil profondità inattivo può essere letto da uno shader come trama. Un'applicazione che legge un buffer di stencil Depth come trama esegue il rendering in due passaggi, il primo passaggio scrive nel buffer di stencil Depth e il secondo passaggio legge dal buffer. Ciò consente a uno shader di confrontare i valori di profondità o stencil scritti in precedenza nel buffer rispetto al valore per il Currrently di pixel di cui viene eseguito il rendering. Il risultato del confronto può essere utilizzato per creare effetti quali il mapping delle ombreggiature o le particelle morbide in un sistema particellare.

Per creare un buffer di stencil depth che può essere usato come una risorsa di stencil di profondità e una risorsa shader, è necessario apportare alcune modifiche al codice di esempio nella sezione [creare una risorsa Depth-Stencil](#create-a-depth-stencil-resource) .

-   La risorsa di stencil Depth deve avere un formato privo di tipo, ad esempio DXGI \_ Format \_ R32 \_ tipo.
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   La risorsa di stencil Depth deve usare sia i flag di profondità di binding D3D10 \_ \_ \_ che D3D10 \_ binding \_ shader \_ .
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

Inoltre, è necessario creare una visualizzazione delle risorse dello shader per il buffer di profondità usando una struttura [**desc di d3d11 \_ shader \_ Resource \_ View \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) e [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview). La visualizzazione risorse dello shader utilizzerà un formato tipizzato, ad esempio **DXGI \_ Format \_ R32 \_ float** equivalente al formato non tipizzato specificato quando è stata creata la risorsa di stencil Depth.

Nel primo passaggio di rendering il buffer di profondità viene associato come descritto nella sezione [associare dati Depth-Stencil alla fase om](#bind-depth-stencil-data-to-the-om-stage) . Si noti che il formato passato a [**d3d11 \_ Depth \_ stencil \_ View \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Format utilizzerà un formato tipizzato, ad esempio **DXGI \_ Format \_ D32 \_ float**. Dopo il primo passaggio di rendering, il buffer di profondità conterrà i valori di profondità per la scena.

Nel secondo passaggio di rendering viene usata la funzione [**sul ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) per impostare la visualizzazione depth-stencil su **null** o una risorsa di stencil Depth diversa e la visualizzazione delle risorse dello shader viene passata allo shader usando [**ID3D11EffectShaderResourceVariable:: seresource**](id3dx11effectshaderresourcevariable-setresource.md). Questo consente allo shader di cercare i valori di profondità calcolati nel primo passaggio di rendering. Si noti che è necessario applicare una trasformazione per recuperare i valori di profondità se il punto di visualizzazione del primo passaggio di rendering è diverso dal secondo passaggio di rendering. Se, ad esempio, viene usata una tecnica di mapping Shadow, il primo passaggio di rendering sarà dalla prospettiva di una sorgente di luce mentre il secondo passaggio di rendering verrà dal punto di vista del visualizzatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Output-fase di Unione](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 