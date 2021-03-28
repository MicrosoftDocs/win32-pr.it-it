---
title: Configurazione della funzionalità di fusione
description: Le operazioni di fusione vengono eseguite ogni pixel shader output (valore RGBA) prima che il valore di output venga scritto in una destinazione di rendering. Se è abilitato il campionamento multiplo, il blending viene eseguito in ogni multicampione; in caso contrario, la fusione viene eseguita su ogni pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993392"
---
# <a name="configuring-blending-functionality"></a>Configurazione della funzionalità di fusione

Le operazioni di fusione vengono eseguite ogni pixel shader output (valore RGBA) prima che il valore di output venga scritto in una destinazione di rendering. Se è abilitato il campionamento multiplo, il blending viene eseguito in ogni multicampione; in caso contrario, la fusione viene eseguita su ogni pixel.

-   [Creare lo stato di Blend](#create-the-blend-state)
-   [Associa lo stato di Blend](#bind-the-blend-state)
-   [Argomenti di blending avanzati](#advanced-blending-topics)
    -   [Da Alpha a code coverage](#alpha-to-coverage)
    -   [Fusione di output di pixel shader](#blending-pixel-shader-outputs)
-   [Argomenti correlati](#related-topics)

## <a name="create-the-blend-state"></a>Creare lo stato di Blend

Lo stato di Blend è una raccolta di stati usati per controllare la fusione. Questi stati (definiti in [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) vengono usati per creare l'oggetto di stato Blend chiamando [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).

Ad esempio, di seguito è riportato un esempio molto semplice di creazione dello stato di Blend che disabilita la fusione alfa e non usa la maschera dei pixel per componente.


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



Questo esempio è simile all' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="bind-the-blend-state"></a>Associa lo stato di Blend

Dopo aver creato l'oggetto di stato Blend, associare l'oggetto di stato Blend alla fase di Unione dell'output chiamando [**sul ID3D11DeviceContext:: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



Questa API accetta tre parametri: l'oggetto di stato Blend, un fattore di fusione a quattro componenti e una maschera di esempio. È possibile passare un **valore null** per l'oggetto di stato Blend per specificare lo stato di Blend predefinito oppure passare un oggetto di stato Blend. Se è stato creato l'oggetto di stato Blend con [**d3d11 \_ Blend \_ Blend \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) o [**d3d11 \_ Blend \_ inv \_ Blend \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), è possibile passare un fattore di fusione per modulare i valori per il pixel shader, la destinazione di rendering o entrambi. Se non è stato creato l'oggetto di stato Blend con **d3d11 \_ Blend \_ Blend \_ Factor** o **d3d11 \_ Blend \_ inv \_ Blend \_**, è comunque possibile passare un fattore di Blend non null, ma la fase di fusione non usa il fattore di Blend. il runtime archivia il fattore di Blend ed è quindi possibile chiamare [**sul ID3D11DeviceContext:: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) per recuperare il fattore di Blend. Se si passa **null**, il runtime USA o archivia un fattore di fusione uguale a {1, 1, 1, 1}. La maschera di esempio è una maschera definita dall'utente che determina come campionare la destinazione di rendering esistente prima di aggiornarla. La maschera di campionamento predefinita è 0xFFFFFFFF, che definisce il campionamento dei punti.

Nella maggior parte degli schemi di buffering, il pixel più vicino alla fotocamera è quello che viene disegnato. Quando si [Configura lo stato depth stencil](d3d10-graphics-programming-guide-depth-stencil.md), il membro **DepthFunc** di [**d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) può essere qualsiasi funzione di [**\_ confronto d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func). In genere, è preferibile che **DepthFunc** il **\_ confronto d3d11 \_ meno**, in modo che i pixel più vicini alla fotocamera sovrascrivano i pixel sottostanti. Tuttavia, a seconda delle esigenze dell'applicazione, è possibile usare qualsiasi altra funzione di confronto per eseguire il test di profondità.

## <a name="advanced-blending-topics"></a>Argomenti di blending avanzati

-   [Da Alpha a code coverage](#alpha-to-coverage)
-   [Fusione di output di pixel shader](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>Da Alpha a code coverage

Alpha-to-coverage è una tecnica di campionamento multiplo particolarmente utile per situazioni come il fogliame denso in cui sono presenti diversi poligoni sovrapposti che usano la trasparenza alpha per definire i bordi all'interno della superficie.

È possibile usare il membro **AlphaToCoverageEnable** di [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) o [**d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) per indicare se il runtime converte il. un componente (alfa) del registro di output [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 dalla pixel shader a una maschera di code coverage n-Step (dato un n-Sample **renderTarget**). Il runtime esegue un'operazione **e** di questa maschera con la tipica copertura di esempio per il pixel della primitiva (oltre alla maschera di esempio) per determinare gli esempi da aggiornare in tutti i **renderTarget** attivi.

Se il pixel shader restituisce [il \_ code coverage SV](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), il runtime Disabilita l'alfa per la copertura.

> [!Note]  
> Durante il campionamento multiplo, il runtime condivide solo una copertura per tutti i **renderTarget**. Il fatto che il runtime legga e converta. a [dalla \_ destinazione SV](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)di output 0 al code coverage quando **AlphaToCoverageEnable** è true non modifica. un valore che passa a Blender in **renderTarget** 0 (se viene impostato un **renderTarget** ). In generale, se si Abilita la funzionalità Alpha-to-coverage, non si influisce sul modo in cui tutti gli output dei colori dei pixel shader interagiscono con **renderTarget** tramite la [fase di Unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md) , ad eccezione del fatto che il runtime esegue un'operazione **e** della maschera di code coverage con la maschera da Alpha a code coverage. L'Alpha a code coverage funziona indipendentemente dal fatto che il Runtime sia in grado di fondere **renderTarget** o se si usa la fusione in **renderTarget**.

 

L'hardware grafico non specifica esattamente il modo in cui converte pixel shader [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (Alpha) in una maschera di code coverage, ad eccezione del fatto che alfa di 0 (o meno) deve eseguire il mapping a nessuna copertura e Alpha di 1 (o superiore) deve eseguire il mapping alla copertura completa (prima che il runtime esegua un'operazione **and** con una copertura primitiva effettiva) Poiché Alpha va da 0 a 1, il code coverage risultante dovrebbe in genere aumentare in modo monotono. Tuttavia, l'hardware può eseguire la rethering dell'area per fornire una migliore quantizzazione dei valori alfa al costo della risoluzione spaziale e del rumore. Un valore alfa di NaN (non un numero) comporta una maschera senza copertura (zero).

L'Alpha a code coverage viene usato tradizionalmente anche per la trasparenza dello schermo o per la definizione di sagome dettagliate per Sprite altrimenti opachi.

### <a name="blending-pixel-shader-outputs"></a>Fusione di output di pixel shader

Questa funzionalità consente all'Unione di output di usare contemporaneamente gli output pixel shader come origini di input in un'operazione di fusione con la singola destinazione di rendering nello slot 0.

Questo esempio accetta due risultati e li combina in un unico passaggio, fondendone uno nella destinazione con un moltiplicatore e l'altro con un valore di aggiunta:


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



Questo esempio Mostra come configurare il primo output pixel shader come colore di origine e il secondo output come fattore di Blend di componenti per colore.


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



Questo esempio illustra il modo in cui i fattori di Blend devono corrispondere allo shader swizzles:


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Insieme, i fattori di Blend e il codice dello shader implicano che il pixel shader è necessario per restituire almeno o0. r e O1. a. I componenti di output aggiuntivi possono essere restituiti dallo shader, ma verrebbero ignorati e un numero inferiore di componenti produrrebbe risultati non definiti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Output-fase di Unione](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 