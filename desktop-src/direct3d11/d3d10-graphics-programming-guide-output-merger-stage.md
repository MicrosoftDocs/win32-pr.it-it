---
title: Fase Output-Merger
description: La fase di Unione degli output genera il colore del pixel finale sottoposto a rendering utilizzando una combinazione di stato della pipeline, i dati dei pixel generati dai pixel shader, il contenuto delle destinazioni di rendering e il contenuto dei buffer di profondità/stencil.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- fase Unione output (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec77eaff506a0be87a3f0e98de691b50c27c0c3f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399940"
---
# <a name="output-merger-stage"></a>Fase Output-Merger

La fase di Unione degli output genera il colore del pixel finale sottoposto a rendering utilizzando una combinazione di stato della pipeline, i dati dei pixel generati dai pixel shader, il contenuto delle destinazioni di rendering e il contenuto dei buffer di profondità/stencil. La fase OM è il passaggio finale per determinare quali pixel sono visibili (con test di stencil Depth) e fondere i colori finali dei pixel.



|                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10: Direct3D 9 implementa il test Alfa (usando [lo stato di test alfa](/windows/desktop/direct3d9/alpha-testing-state)) per controllare se un pixel viene scritto in una destinazione di rendering dell'output.<br/> Direct3D 10 e versioni successive non implementa un test Alfa (o uno stato di test alfa). Questa operazione può essere controllata utilizzando un pixel shader o con la funzionalità depth/stencil.<br/> |



 

## <a name="depth-stencil-testing-overview"></a>Panoramica sul test di Depth-Stencil

Un buffer di stencil Depth, creato come una risorsa di trama, può contenere sia dati di profondità che dati di stencil. I dati di profondità vengono utilizzati per determinare quali pixel si trovano più vicini alla fotocamera e i dati dello stencil vengono utilizzati per mascherare i pixel che è possibile aggiornare. Infine, i dati relativi ai valori di profondità e stencil vengono usati dalla fase di Unione dell'output per determinare se un pixel deve essere disegnato o meno. Il diagramma seguente illustra concettualmente il modo in cui viene eseguito il test di stencil Depth.

![diagramma del funzionamento del test di stencil Depth](images/d3d10-depth-stencil-test.png)

Per configurare il test di stencil Depth, vedere [configurazione Depth-Stencil funzionalità](d3d10-graphics-programming-guide-depth-stencil.md). Un oggetto stencil Depth incapsula lo stato di stencil Depth. Un'applicazione può specificare lo stato di stencil Depth oppure la fase OM utilizzerà i valori predefiniti. Se il campionamento multiplo è disabilitato, le operazioni di fusione vengono eseguite in base ai singoli pixel. Se è abilitato il campionamento multiplo, la fusione si verifica in base a ogni singolo campione.

Il processo di utilizzo del buffer di profondità per determinare il pixel da disegnare viene definito buffering di profondità, anche a volte definito buffer z.

Una volta che i valori di profondità raggiungono la fase di Unione dell'output (sia proveniente dall'interpolazione che da un pixel shader), vengono sempre bloccati: z = min (viewport. MaxDepth, Max (viewport. MinDepth, z)) in base al formato o alla precisione del buffer di profondità, usando le regole a virgola mobile. Dopo la chiusura, il valore di profondità viene confrontato (usando DepthFunc) con il valore del buffer di profondità esistente. Se non è associato alcun buffer di profondità, il test di profondità viene sempre superato.

Se non è presente alcun componente dello stencil nel formato del buffer di profondità o nessun limite di buffer di profondità, il test di stencil viene sempre superato. In caso contrario, la funzionalità è invariata da Direct3D 9.

Può essere attivo un solo buffer di profondità/stencil alla volta. qualsiasi visualizzazione delle risorse associata deve corrispondere (dimensione e dimensioni uguali) alla visualizzazione profondità/stencil. Questo non significa che le dimensioni della risorsa devono corrispondere, solo che le dimensioni della vista devono corrispondere.

Per ulteriori informazioni sui test di stencil Depth, vedere l' [esercitazione 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="blending-overview"></a>Panoramica della fusione

La fusione combina uno o più valori di pixel per creare un colore finale del pixel. Il diagramma seguente illustra il processo richiesto per la fusione dei dati pixel.

![diagramma di come funziona la fusione dei dati](images/d3d10-blend-state.png)

Dal punto di vista concettuale, è possibile visualizzare questo diagramma di flusso implementato due volte nella fase di Unione dell'output: la prima combina i dati RGB, mentre in parallelo un secondo combina i dati alfa. Per informazioni su come usare l'API per creare e impostare lo stato di Blend, vedere [configurazione della funzionalità di fusione](d3d10-graphics-programming-guide-blend-state.md).

La funzione Fixed-Blend può essere abilitata in modo indipendente per ogni destinazione di rendering. Tuttavia è presente un solo set di controlli Blend, in modo che la stessa Blend venga applicata a tutti RenderTargets con la fusione abilitata. I valori di Blend (incluso BlendFactor) vengono sempre bloccati nell'intervallo del formato di destinazione di rendering prima della fusione. Il blocco viene eseguito per ogni destinazione di rendering, rispettando il tipo di destinazione di rendering. L'unica eccezione riguarda i formati float16, float11 o float10 che non vengono bloccati, in modo che le operazioni di Blend in questi formati possano essere eseguite con una precisione o un intervallo almeno uguale a quello del formato di output. I NaN e gli zeri con segno vengono propagati per tutti i casi (compresi i pesi di 0,0 Blend).

Quando si usano le destinazioni di rendering sRGB, il runtime converte il colore della destinazione di rendering in uno spazio lineare prima di eseguire la fusione. Il runtime converte nuovamente il valore di Blend finale nello spazio sRGB prima di salvarlo di nuovo nella destinazione di rendering.



|                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10: in Direct3D 9, la fusione di funzioni fisse può essere abilitata in modo indipendente per ogni destinazione di rendering.<br/> In Direct3D 10 e versioni successive è presente una descrizione dello stato di Blend. Pertanto, è possibile impostare un valore di fusione per tutte le destinazioni di rendering.<br/> |



 

### <a name="dual-source-color-blending"></a>Fusione di colori Dual-Source

Questa funzionalità consente alla fase di Unione dell'output di usare contemporaneamente entrambi gli output pixel shader (o0 e O1) come input per un'operazione di fusione con la singola destinazione di rendering nello slot 0. Le operazioni di Blend valide includono: Add, Subtract e RevSubtract. Le opzioni di Blend valide per SrcBlend, DestBlend, SrcBlendAlpha o DestBlendAlpha includono: **d3d11 \_ Blend \_ src1 \_ color**, **d3d11 \_ Blend \_ inv \_ src1 \_**, **d3d11 \_ Blend \_ src1 \_ Alpha**, **d3d11 \_ Blend \_ inv \_ src1 \_ Alpha**. L'equazione di Blend e la maschera di scrittura di output specificano i componenti che l'pixel shader sta inserendo. I componenti aggiuntivi vengono ignorati.

La scrittura in altri output pixel shader (O2, O3 e così via) non è definita. non è possibile scrivere in una destinazione di rendering se non è associato allo slot 0. La scrittura di oDepth è valida durante la combinazione di colori di origine doppia.

Per esempi, vedere [blending pixel shader Outputs](d3d10-graphics-programming-guide-blend-state.md).

## <a name="multiple-rendertargets-overview"></a>Panoramica di più RenderTargets

È possibile utilizzare un pixel shader per eseguire il rendering di almeno 8 destinazioni di rendering separate, che devono essere dello stesso tipo (buffer, Texture1D, Texture1DArray e così via). Inoltre, tutte le destinazioni di rendering devono avere le stesse dimensioni in tutte le dimensioni (larghezza, altezza, profondità, dimensioni della matrice, conteggi di esempio). Ogni destinazione di rendering può avere un formato dati diverso.

È possibile utilizzare qualsiasi combinazione di slot di destinazioni di rendering (fino a 8). Tuttavia, una visualizzazione delle risorse non può essere associata a più slot di destinazione di rendering simultaneamente. Una vista può essere riutilizzata purché le risorse non vengano utilizzate simultaneamente.

## <a name="output-write-mask-overview"></a>Panoramica di Output-Write mask

Usare una maschera di scrittura di output per controllare (per componente) quali dati possono essere scritti in una destinazione di rendering.

## <a name="sample-mask-overview"></a>Panoramica della maschera di esempio

Una maschera di esempio è una maschera di code coverage multisample a 32 bit che determina quali esempi vengono aggiornati nelle destinazioni di rendering attive. È consentita una sola maschera di esempio. Il mapping dei bit in una maschera di esempio agli esempi in una risorsa è definito da un utente. Per il rendering n-Sample, vengono usati i primi n bit (dal LSB) della maschera di esempio (32 bit il numero massimo di bit).


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                    | Descrizione                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurazione della funzionalità Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | In questa sezione vengono illustrati i passaggi per configurare il buffer di stencil Depth e lo stato depth-stencil per la fase di Unione dell'output.<br/>                                                                                                                           |
| [Configurazione della funzionalità di fusione](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Le operazioni di fusione vengono eseguite ogni pixel shader output (valore RGBA) prima che il valore di output venga scritto in una destinazione di rendering. Se è abilitato il campionamento multiplo, il blending viene eseguito in ogni multicampione; in caso contrario, la fusione viene eseguita su ogni pixel.<br/> |
| [Distorsione profondità](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | È possibile fare in modo che i poligoni complanari nello spazio 3D vengano visualizzati come se non fossero complanari aggiungendo a ognuno una distorsione z (o una distorsione di profondità).<br/>                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

