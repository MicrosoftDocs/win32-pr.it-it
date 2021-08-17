---
title: Attività iniziali con la fase rasterizzatore
description: Questa sezione descrive l'impostazione del viewport, il rettangolo delle forbici, lo stato del rasterizzatore e il campionamento multiplo.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- multicampionamento, stato rasterizzatore (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e819dd92dd9c07a71f3830d3b67e371bc3d0e0c98f62fa36fdcf8ee3550ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914002"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Attività iniziali con la fase rasterizzatore

Questa sezione descrive l'impostazione del viewport, il rettangolo delle forbici, lo stato del rasterizzatore e il campionamento multiplo.

## <a name="set-the-viewport"></a>Impostare il viewport

Un viewport esegue il mapping delle posizioni dei vertici (nello spazio della clip) nelle posizioni di destinazione di rendering. Questo passaggio ridimensiona le posizioni 3D nello spazio 2D. Una destinazione di rendering è orientata con gli assi Y che puntano verso il basso; ciò richiede che le coordinate Y vengono capovolte durante la scala del viewport. Inoltre, gli extent x e y (intervallo dei valori x e y) vengono ridimensionati in base alle dimensioni del viewport in base alle formule seguenti:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



L'esercitazione 1 crea un viewport 640 × 480 [**usando \_ VIEWPORT D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e chiamando [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


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



La descrizione del viewport specifica le dimensioni del viewport, l'intervallo a cui eseguire il mapping della profondità (usando *MinDepth* e *MaxDepth)* e la posizione in alto a sinistra del viewport. *MinDepth* deve essere minore o uguale a *MaxDepth*; l'intervallo per *MinDepth* e *MaxDepth* è compreso tra 0,0 e 1,0, inclusi. Il mapping del viewport a una destinazione di rendering è comune, ma non è necessario; Inoltre, il viewport non deve avere le stesse dimensioni o posizione della destinazione di rendering.

È possibile creare una matrice di viewport, ma solo uno può essere applicato a un output primitivo dallo shader geometry. È possibile impostare un solo viewport attivo alla volta. La pipeline usa un viewport predefinito (e un rettangolo di forbice, descritto nella sezione successiva) durante la rasterizzazione. Il valore predefinito è sempre il primo riquadro di visualizzazione (o rettangolo di forbice) nella matrice. Per eseguire una selezione per primitiva del viewport nel geometry shader, specificare la semantica ViewportArrayIndex nel componente di output GS appropriato nella dichiarazione della firma di output GS.

Il numero massimo di viewport (e rettangoli di forbici) che possono essere associati alla fase del rasterizzatore in qualsiasi momento è 16 (specificato da **D3D11 \_ VIEWPORT \_ E \_ SCISSORRECT \_ OBJECT COUNT PER \_ \_ \_ PIPELINE).**

## <a name="set-the-scissor-rectangle"></a>Impostare il rettangolo di forbice

Un rettangolo di forbice offre un'altra opportunità per ridurre il numero di pixel che verranno inviati alla fase di unione dell'output. I pixel all'esterno del rettangolo della forbice vengono eliminati. Le dimensioni del rettangolo della forbice sono specificate in numeri interi. Durante la rasterizzazione è possibile applicare un solo rettangolo di forbice (basato su *ViewportArrayIndex* nella [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)dei valori di sistema).

Per abilitare il rettangolo di forbice, usare il membro *ScissorEnable* (in [**D3D11 \_ RASTERIZER \_ DESC1).**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) Il rettangolo di forbice predefinito è un rettangolo vuoto. in altri, tutti i valori rect sono 0. In altre parole, se non si configura il rettangolo di forbice e la forbice è abilitata, non si invieranno pixel alla fase di unione dell'output. La configurazione più comune è inizializzare il rettangolo della forbice alle dimensioni del viewport.

Per impostare una matrice di rettangoli di forbici sul dispositivo, chiamare [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) con [**D3D11 \_ RECT.**](d3d11-rect.md)


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Questo metodo accetta due parametri: (1) il numero di rettangoli nella matrice e (2) una matrice di rettangoli.

La pipeline usa un indice del rettangolo di forbice predefinito durante la rasterizzazione (il valore predefinito è un rettangolo di dimensioni zero con ritaglio disabilitato). Per eseguire l'override, specificare la semantica SV \_ ViewportArrayIndex in un componente di output GS nella dichiarazione della firma di output GS. In questo modo la fase GS contrassegnerà questo componente di output GS come componente generato dal sistema con questa semantica. La fase del rasterizzatore riconosce questa semantica e userà il parametro a cui è associata come indice del rettangolo di forbice per accedere alla matrice di rettangoli di forbice. Non dimenticare di indicare alla fase del rasterizzatore di usare il rettangolo di forbice definito abilitando il *valore ScissorEnable* nella descrizione del rasterizzatore prima di creare l'oggetto rasterizzatore.

## <a name="set-rasterizer-state"></a>Impostare lo stato del rasterizzatore

A partire da Direct3D 10, lo stato del rasterizzatore viene incapsulato in un oggetto stato del rasterizzatore. È possibile creare fino a 4096 oggetti di stato del rasterizzatore che possono quindi essere impostati sul dispositivo passando un handle all'oggetto stato.

Usare [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) per creare un oggetto stato del rasterizzatore da una descrizione del rasterizzatore (vedere [**D3D11 \_ RASTERIZER \_ DESC1).**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)


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



Questo set di stato di esempio consente di eseguire la configurazione del rasterizzatore più semplice:

-   Modalità riempimento a tinta unita
-   Rimuovere o rimuovere i visi posteriore; presupporre un ordine di avvolgimento in senso antiorario per le primitive
-   Disattivare la distorsione della profondità, ma abilitare il buffering della profondità e abilitare il rettangolo di forbice
-   Disattivare il multicampionamento e l'anti-aliasing delle righe

Inoltre, le operazioni di rasterizzazione di base includono sempre quanto segue: ritaglio (al frustum di visualizzazione), divisione prospettica e scala del viewport. Dopo aver creato correttamente l'oggetto stato del rasterizzatore, impostarlo sul dispositivo nel modo seguente:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Multicampionamento

Il multicampionamento esemplifica alcuni o tutti i componenti di un'immagine a una risoluzione superiore (seguita dal downsampling alla risoluzione originale) per ridurre la forma più visibile di aliasing causata dal disegno di bordi poligono. Anche se il multicampionamento richiede esempi di sub-pixel, la GPU moderna implementa il multicampionamento in modo che un'pixel shader venga eseguita una volta per pixel. Ciò offre un compromesso accettabile tra le prestazioni (in particolare in un'applicazione associata a GPU) e l'anti-aliasing dell'immagine finale.

Per usare il multicampionamento, impostare il campo enable nella descrizione [**della rasterizzazione,**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)creare una destinazione di rendering multicampionata e leggere la destinazione di rendering con uno shader per risolvere gli esempi in un singolo colore pixel oppure chiamare [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) per risolvere gli esempi usando la scheda video. Lo scenario più comune consiste nel disegnare in una o più destinazioni di rendering multicampionato.

Il multicampionamento è indipendente dal fatto che sia usata o meno una maschera di esempio, che sia abilitata la funzione [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) o che le operazioni di stencil (che vengono sempre eseguite per ogni campione).

Il test di profondità è interessato dal multicampionamento:

-   Quando il multicampionamento è abilitato, la profondità viene interpolata per ogni campione e il test di profondità/stencil viene eseguito per ogni campione; il pixel shader di output viene duplicato per tutti i campioni di passaggio. Se il pixel shader restituisce la profondità, il valore di profondità viene duplicato per tutti gli esempi,anche se questo scenario perde il vantaggio del multicampionamento.
-   Quando il multicampionamento è disabilitato, il test di profondità/stencil viene comunque eseguito per ogni campione, ma la profondità non viene interpolata per ogni campione.

Non esistono restrizioni per la combinazione di rendering multicampionato e non multicampionato all'interno di una singola destinazione di rendering. Se si abilita il multicampionamento e si disegna in una destinazione di rendering non multicampionata, si produce lo stesso risultato di se il multicampionamento non fosse abilitato. il campionamento viene eseguito con un singolo campione per pixel.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase Rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 