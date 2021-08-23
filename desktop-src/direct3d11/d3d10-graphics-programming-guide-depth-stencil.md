---
title: Configurazione Depth-Stencil funzionalità
description: Questa sezione illustra i passaggi per configurare il buffer depth-stencil e lo stato depth-stencil per la fase di unione dell'output.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e994c5a11215d245d8101edff410a91ffb788583b07f651fdfbd1f2771d7deab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990191"
---
# <a name="configuring-depth-stencil-functionality"></a>Configurazione Depth-Stencil funzionalità

Questa sezione illustra i passaggi per configurare il buffer depth-stencil e lo stato depth-stencil per la fase di unione dell'output.

-   [Creare una Depth-Stencil risorsa](#create-a-depth-stencil-resource)
-   [Creare Depth-Stencil stato](#create-depth-stencil-state)
-   [Associare Depth-Stencil dati alla fase OM](#bind-depth-stencil-data-to-the-om-stage)

Dopo aver spiegato come usare il buffer depth-stencil e lo stato depth-stencil corrispondente, fare riferimento [alle tecniche di stencil avanzato.](#advanced-stencil-techniques)

## <a name="create-a-depth-stencil-resource"></a>Creare una Depth-Stencil risorsa

Creare il buffer depth-stencil usando una risorsa trama.


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



## <a name="create-depth-stencil-state"></a>Creare Depth-Stencil stato

Lo stato depth-stencil indica alla fase di unione dell'output come eseguire il [test di profondità-stencil](d3d10-graphics-programming-guide-output-merger-stage.md). Il test di profondità-stencil determina se deve essere disegnato o meno un determinato pixel.


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



DepthEnable e StencilAbilita abilitano (e disabilitano) i test di profondità e stencil. Impostare DepthEnable su **FALSE per disabilitare** il test di profondità e impedire la scrittura nel buffer di profondità. Impostare StencilEnable su **FALSE** per disabilitare il test degli stencil e impedire la scrittura nel buffer degli stencil (quando DepthEnable **è FALSE** e StencilEnable è **TRUE,** il test di profondità passa sempre nell'operazione stencil).

DepthEnable influisce solo sulla fase di unione dell'output: non influisce sul ritaglio, sulla distorsione della profondità o sulla chiusura dei valori prima che i dati vengono immessi in un pixel shader.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Associare Depth-Stencil dati alla fase OM

Associare lo stato depth-stencil.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Associare la risorsa depth-stencil usando una visualizzazione.


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



Una matrice di visualizzazioni di destinazione di rendering può essere passata in [**ID3D11DeviceContext::OMSetRenderTargets,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)tuttavia tutte le visualizzazioni di destinazione di rendering corrisponderanno a una singola visualizzazione depth stencil rendering. La matrice di destinazione di rendering in Direct3D 11 è una funzionalità che consente a un'applicazione di eseguire il rendering su più destinazioni di rendering contemporaneamente a livello primitivo. Le matrici di destinazione di rendering offrono prestazioni migliori rispetto all'impostazione singola delle destinazioni di rendering con più chiamate a **ID3D11DeviceContext::OMSetRenderTargets** (essenzialmente il metodo utilizzato in Direct3D 9).

Le destinazioni di rendering devono essere tutte dello stesso tipo di risorsa. Se si usa l'anti-aliasing multicampionamento, tutte le destinazioni di rendering associate e i buffer di profondità devono avere gli stessi conteggi dei campioni.

Quando un buffer viene usato come destinazione di rendering, i test di profondità-stencil e più destinazioni di rendering non sono supportati.

-   Fino a 8 destinazioni di rendering possono essere associate contemporaneamente.
-   Tutte le destinazioni di rendering devono avere le stesse dimensioni in tutte le dimensioni (larghezza e altezza e profondità per le dimensioni 3D o matrice per i \* tipi array).
-   Ogni destinazione di rendering può avere un formato dati diverso.
-   Le maschere di scrittura controllano quali dati vengono scritti in una destinazione di rendering. Il controllo delle maschere di scrittura di output in una destinazione di rendering, a livello di singolo componente, indica quali dati vengono scritti nelle destinazione o nelle destinazione di rendering.

## <a name="advanced-stencil-techniques"></a>Tecniche di stencil avanzate

La parte stencil del buffer depth-stencil può essere usata per creare effetti di rendering, ad esempio composizione, decalcomania e struttura.

-   [Compositing](#compositing)
-   [Decalcommentazione](#decaling)
-   [Contorni e recinti](#outlines-and-silhouettes)
-   [Stencil a due lati](#two-sided-stencil)
-   [Lettura del buffer Depth-Stencil come trama](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Compositing

L'applicazione può usare il buffer degli stencil per creare immagini 2D o 3D composite in una scena 3D. Una maschera nel buffer degli stencil viene usata per occludere un'area della superficie di destinazione di rendering. Le informazioni 2D archiviate, ad esempio testo o bitmap, possono quindi essere scritte nell'area occluded. In alternativa, l'applicazione può eseguire il rendering di primitive 3D aggiuntive nell'area con maschera stencil della superficie di destinazione del rendering. Può anche eseguire il rendering di un'intera scena.

I giochi spesso si uniscono più scene 3D. Ad esempio, i giochi di guida in genere visualizzano un mirror retrovisore. Il mirror contiene la vista della scena 3D dietro il driver. Si tratta essenzialmente di una seconda scena 3D composita con la visualizzazione in avanti del driver.

### <a name="decaling"></a>Decalcommentazione

Le applicazioni Direct3D usano la decalcommentazione per controllare quali pixel di una particolare immagine primitiva vengono disegnati sulla superficie di destinazione del rendering. Le applicazioni applicano decalcomanie alle immagini di primitive per consentire il rendering corretto dei poligoni coplanari.

Ad esempio, quando si applicano i segni di gomme e le linee gialle a una strada, i contrassegni devono essere visualizzati direttamente sopra la strada. Tuttavia, i valori z dei contrassegni e della strada sono gli stessi. Pertanto, il buffer di profondità potrebbe non produrre una netta separazione tra i due. È possibile eseguire il rendering di alcuni pixel nella primitiva posteriore sopra la primitiva anteriore e viceversa. L'immagine risultante viene visualizzata come s shi shi shi sempre da un frame all'altro. Questo effetto è denominato z-fighting o fliluming.

Per risolvere questo problema, usare uno stencil per mascherare la sezione della primitiva back in cui verrà visualizzata la decalcomania. Disattivare z-buffering ed eseguire il rendering dell'immagine della primitiva anteriore nell'area mascherata della superficie di destinazione di rendering.

Per risolvere questo problema, è possibile usare la fusione di più trame.

### <a name="outlines-and-silhouettes"></a>Contorni e recinti

È possibile usare il buffer degli stencil per effetti più astratti, ad esempio struttura e silhouetting.

Se l'applicazione esegue due passaggi di rendering, uno per generare la maschera di stencil e il secondo per applicare la maschera di stencil all'immagine, ma con le primitive leggermente più piccole nel secondo passaggio, l'immagine risultante conterrà solo il contorno della primitiva. L'applicazione può quindi riempire l'area con maschera stencil dell'immagine con un colore a tinta unita, dando alla primitiva un aspetto in rilievo.

Se la maschera di stencil ha le stesse dimensioni e la stessa forma della primitiva di cui si esegue il rendering, l'immagine risultante contiene un foro in cui deve essere la primitiva. L'applicazione può quindi riempire il foro di nero per produrre una parte della primitiva.

### <a name="two-sided-stencil"></a>Two-Sided stencil

I volumi ombreggiati vengono usati per disegnare ombreggiature con il buffer degli stencil. L'applicazione calcola i volumi ombreggiati espressi dalla geometria occluding, calcolando i bordi della superficie ed estrudendoli dalla luce in un set di volumi 3D. Il rendering di questi volumi viene quindi eseguito due volte nel buffer degli stencil.

Il primo rendering disegna poligoni rivolti in avanti e incrementa i valori stencil-buffer. Il secondo rendering disegna i poligoni rivolti all'indietro del volume dell'ombreggiatura e decrementa i valori del buffer degli stencil. In genere, tutti i valori incrementati e decrementati si annullano a vicenda. Tuttavia, il rendering della scena è già stato eseguito con una geometria normale, causando l'esito negativo del test z-buffer di alcuni pixel durante il rendering del volume dell'ombreggiatura. I valori lasciati nel buffer degli stencil corrispondono ai pixel nell'ombreggiatura. Questi contenuti rimanenti dello stencil-buffer vengono usati come maschera, per eseguire la fusione alfa di un quad nero ampio e incomprenso nella scena. Con il buffer degli stencil che funge da maschera, il risultato è l'ombreggiatura dei pixel che si trova nelle ombreggiature.

Ciò significa che la geometria dell'ombreggiatura viene disegnata due volte per ogni sorgente di luce, di conseguenza la pressione sulla velocità effettiva dei vertici della GPU. La funzionalità stencil a due lati è stata progettata per attenuare questa situazione. In questo approccio sono presenti due set di stato degli stencil (denominati di seguito), uno impostato per i triangoli rivolti anteriore e l'altro per i triangoli rivolti all'indietro. In questo modo, viene disegnato un solo passaggio per volume di ombreggiatura, per ogni luce.

Un esempio di implementazione dello stencil a due lati è disponibile nell'esempio [ShadowVolume10.](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Lettura del buffer Depth-Stencil come trama

Un buffer depth-stencil inattivo può essere letto da uno shader come trama. Un'applicazione che legge un buffer depth-stencil durante il rendering di una trama in due passaggi, il primo passaggio scrive nel buffer depth-stencil e il secondo passa le operazioni di lettura dal buffer. Ciò consente a uno shader di confrontare i valori di profondità o stencil scritti in precedenza nel buffer con il valore del pixel sottoposto a rendering. Il risultato del confronto può essere usato per creare effetti come il mapping delle ombreggiatura o le particelle soft in un sistema di particelle.

Per creare un buffer depth-stencil che può essere usato sia come risorsa depth-stencil che come risorsa shader, è necessario apportare [alcune](#create-a-depth-stencil-resource) modifiche al codice di esempio nella sezione Creare una risorsa di Depth-Stencil profondità.

-   La risorsa depth-stencil deve avere un formato senza tipo, ad esempio DXGI \_ FORMAT \_ R32 \_ TYPELESS.
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   La risorsa depth-stencil deve usare i flag di associazione D3D10 BIND DEPTH STENCIL e \_ \_ \_ D3D10 \_ BIND \_ SHADER \_ RESOURCE.
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

È anche necessario creare una visualizzazione delle risorse shader per il buffer di profondità usando una struttura [**\_ \_ \_ \_ DESC D3D11 SHADER RESOURCE VIEW**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) e [**ID3D11Device::CreateShaderResourceView.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) La visualizzazione delle risorse shader userà un formato tipiato, ad esempio **DXGI \_ FORMAT \_ R32 \_ FLOAT,** equivalente al formato senza tipi specificato al momento della creazione della risorsa depth-stencil.

Nel primo passaggio di rendering il buffer di profondità viene associato come descritto nella sezione [Associare Depth-Stencil dati alla fase OM.](#bind-depth-stencil-data-to-the-om-stage) Si noti che il formato passato [**a D3D11 \_ DEPTH STENCIL VIEW \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Il formato userà un formato tipiato, ad esempio **DXGI \_ FORMAT \_ D32 \_ FLOAT.** Dopo il primo passaggio di rendering, il buffer di profondità conterrà i valori di profondità per la scena.

Nel secondo passaggio di rendering viene usata la funzione [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) per impostare la visualizzazione dello stencil di profondità su **NULL** o su una risorsa stencil di profondità diversa e la visualizzazione delle risorse shader viene passata allo shader [**usando ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md). In questo modo lo shader può cercare i valori di profondità calcolati nel primo passaggio di rendering. Si noti che sarà necessario applicare una trasformazione per recuperare i valori di profondità se il punto di vista del primo passaggio di rendering è diverso dal secondo passaggio di rendering. Ad esempio, se viene usata una tecnica di mapping delle ombreggiatura, il primo passaggio di rendering sarà dal punto di vista di una sorgente di luce, mentre il secondo passaggio di rendering sarà dal punto di vista del visualizzatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase di unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 