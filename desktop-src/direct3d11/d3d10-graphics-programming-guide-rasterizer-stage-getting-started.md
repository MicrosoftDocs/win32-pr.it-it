---
title: Introduzione con la fase di rasterizzazione
description: In questa sezione viene descritta l'impostazione del viewport, il rettangolo a forbice, lo stato del rasterizzatore e il campionamento multiplo.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- multicampionamento, stato di rasterizzazione (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337582"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Introduzione con la fase di rasterizzazione

In questa sezione viene descritta l'impostazione del viewport, il rettangolo a forbice, lo stato del rasterizzatore e il campionamento multiplo.

## <a name="set-the-viewport"></a>Imposta il viewport

Un viewport esegue il mapping delle posizioni del vertice (nello spazio di ritaglio) nelle posizioni della destinazione di rendering. Questo passaggio ridimensiona le posizioni 3D nello spazio 2D. Una destinazione di rendering è orientata agli assi Y che puntano verso il basso; a tale scopo, è necessario che le coordinate Y vengano capovolte durante la scala del viewport. Inoltre, gli extent x e y (intervallo dei valori x e y) vengono ridimensionati in modo da adattarsi alle dimensioni del viewport in base alle formule seguenti:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



L'esercitazione 1 crea un viewport 640 × 480 usando il [**\_ viewport d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e chiamando [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



La descrizione del viewport specifica le dimensioni del viewport, l'intervallo in base al quale eseguire il mapping della profondità (tramite *MinDepth* e *MaxDepth*) e la posizione della parte superiore sinistra del viewport. *MinDepth* deve essere minore o uguale a *MaxDepth*; l'intervallo sia per *MinDepth* che per *MaxDepth* è compreso tra 0,0 e 1,0 inclusi. È comune che il viewport esegua il mapping a una destinazione di rendering, ma non è necessario. Inoltre, il viewport non deve avere la stessa dimensione o la stessa posizione della destinazione di rendering.

È possibile creare una matrice di viewport, ma solo uno può essere applicato a un output primitivo da Geometry shader. È possibile impostare un solo viewport come attivo alla volta. La pipeline usa un viewport predefinito (e un rettangolo a forbice, illustrato nella sezione successiva) durante la rasterizzazione. Il valore predefinito è sempre il primo Viewport (o rettangolo a forbice) nella matrice. Per eseguire una selezione per primitiva del viewport in Geometry shader, specificare la semantica ViewportArrayIndex sul componente di output GS appropriato nella dichiarazione della firma di output GS.

Il numero massimo di viewport (e rettangoli a forbice) che possono essere associati alla fase di rasterizzazione in qualsiasi momento è 16 (specificato dal **\_ viewport d3d11 \_ e il numero di \_ \_ oggetti SCISSORRECT \_ \_ per \_ pipeline**).

## <a name="set-the-scissor-rectangle"></a>Impostare il rettangolo a forbice

Un rettangolo a forbice offre un'altra opportunità per ridurre il numero di pixel che verranno inviati alla fase di Unione dell'output. I pixel esterni al rettangolo a forbice vengono eliminati. Le dimensioni del rettangolo a forbice sono specificate in numeri interi. Solo un rettangolo a forbice (basato su *ViewportArrayIndex* nella [semantica di valori di sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) può essere applicato a un triangolo durante la rasterizzazione.

Per abilitare il rettangolo a forbice, usare il membro *ScissorEnable* (in [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)). Il rettangolo a forbice predefinito è un rettangolo vuoto; ovvero tutti i valori Rect sono pari a 0. In altre parole, se non si configura il rettangolo a forbice e la forbice è abilitata, non verrà inviato alcun pixel alla fase di Unione dell'output. La configurazione più comune consiste nell'inizializzare il rettangolo a forbice sulle dimensioni del viewport.

Per impostare una matrice di rettangoli Scissor sul dispositivo, chiamare [**sul ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) con [**d3d11 \_ Rect**](d3d11-rect.md).


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Questo metodo accetta due parametri: (1) il numero di rettangoli nella matrice e (2) una matrice di rettangoli.

La pipeline utilizza un indice rettangolare a forbice predefinito durante la rasterizzazione (il valore predefinito è un rettangolo di dimensioni zero con ritaglio disabilitato). Per eseguire l'override di questa impostazione, specificare la \_ semantica SV ViewportArrayIndex per un componente di output GS nella dichiarazione della firma di output GS. In questo modo la fase GS contrassegna questo componente di output GS come componente generato dal sistema con questa semantica. La fase di rasterizzazione riconosce questa semantica e utilizzerà il parametro a cui è associato come indice del rettangolo a forbice per accedere alla matrice di rettangoli a forbice. Non dimenticare di indicare alla fase di rasterizzazione di usare il rettangolo a forbice definito abilitando il valore *ScissorEnable* nella descrizione del rasterizzatore prima di creare l'oggetto di rasterizzazione.

## <a name="set-rasterizer-state"></a>Imposta lo stato di rasterizzazione

A partire da Direct3D 10, lo stato di rasterizzazione viene incapsulato in un oggetto di stato di rasterizzazione. È possibile creare fino a 4096 oggetti di stato di rasterizzazione che possono quindi essere impostati sul dispositivo passando un handle all'oggetto stato.

Usare [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) per creare un oggetto stato di rasterizzazione da una descrizione del rasterizzatore (vedere [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



Questo set di Stati di esempio esegue probabilmente la configurazione del rasterizzatore più semplice:

-   Modalità di riempimento a tinta unita
-   Eliminare o rimuovere i visi posteriori; presume l'ordine di avvolgimento in senso antiorario per le primitive
-   Disabilitare la distorsione di profondità ma abilitare il buffering di profondità e abilitare il rettangolo a forbice
-   Disattiva il campionamento multiplo e l'anti-aliasing della linea

Inoltre, le operazioni di rasterizzazione di base includono sempre gli elementi seguenti: ritaglio (alla visualizzazione tronco), divisione prospettica e scala del viewport. Dopo aver creato l'oggetto stato di rasterizzazione, impostarlo sul dispositivo come segue:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Multicampionamento

Il campionamento multiplo esegue il campionamento di alcuni o tutti i componenti di un'immagine a una risoluzione più elevata (seguita da sottocampionando alla risoluzione originale) per ridurre il formato di alias più visibile causato dalla creazione di bordi del poligono. Sebbene il multicampionamento richieda esempi di sottopixel, la GPU moderna implementa il campionamento multiplo in modo che una pixel shader venga eseguita una volta per ogni pixel. Ciò garantisce un compromesso accettabile tra le prestazioni, soprattutto in un'applicazione con binding GPU, e l'anti-aliasing dell'immagine finale.

Per usare il campionamento multiplo, impostare il campo Enable nella [**Descrizione della rasterizzazione**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), creare una destinazione di rendering multicampionata e leggere la destinazione di rendering con uno shader per risolvere gli esempi in un singolo colore pixel oppure chiamare [**sul ID3D11DeviceContext:: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) per risolvere gli esempi usando la scheda video. Lo scenario più comune consiste nel disegnare in una o più destinazioni di rendering multicampionate.

Il campionamento multiplo è indipendente dal fatto che venga utilizzata o meno una maschera di esempio, che sia abilitata la funzionalità [alfa per il code coverage](d3d10-graphics-programming-guide-blend-state.md) o le operazioni dello stencil, che vengono sempre eseguite per campione.

I test di profondità sono interessati dal campionamento multiplo:

-   Quando è abilitato il campionamento multiplo, la profondità viene interpolata per esempio e il test di profondità/stencil viene eseguito per campione; il colore di output del pixel shader viene duplicato per tutti gli esempi che passano. Se il pixel shader restituisce la profondità, il valore di profondità viene duplicato per tutti i campioni (sebbene questo scenario perda il vantaggio del campionamento multiplo).
-   Quando il campionamento multiplo è disabilitato, il test profondità/stencil viene ancora eseguito per campione, ma la profondità non è interpolata per campione.

Non esistono restrizioni per combinare il rendering multicampionato e non multicampionato all'interno di una singola destinazione di rendering. Se si Abilita il campionamento multiplo e si crea una destinazione di rendering non multicampionata, si produce lo stesso risultato di se il multicampionamento non è stato abilitato; il campionamento viene eseguito con un singolo campione per pixel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase Rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 