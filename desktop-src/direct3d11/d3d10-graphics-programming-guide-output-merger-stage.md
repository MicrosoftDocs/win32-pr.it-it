---
title: Output-Merger fase
description: La fase OM (Output-Merger) genera il colore dei pixel di cui è stato eseguito il rendering finale usando una combinazione di stato della pipeline, i dati pixel generati dai pixel shader, il contenuto delle destinazioni di rendering e il contenuto dei buffer di profondità/stencil.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- Fase di fusione dell'output (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8de2851fdea3a22cc42033d2c13454be72ba8ab
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335215"
---
# <a name="output-merger-stage"></a>Output-Merger fase

La fase OM (Output-Merger) genera il colore pixel finale sottoposto a rendering usando una combinazione di stato della pipeline, i dati pixel generati dai pixel shader, il contenuto delle destinazioni di rendering e il contenuto dei buffer di profondità/stencil. La fase OM è il passaggio finale per determinare quali pixel sono visibili (con test depth-stencil) e per la fusione dei colori dei pixel finali.



Differenze tra Direct3D 9 e Direct3D 10:

- Direct3D 9 implementa il test alfa (usando lo stato [di test](/windows/desktop/direct3d9/alpha-testing-state)alfa) per controllare se un pixel viene scritto in una destinazione di rendering di output.
- Direct3D 10 e versioni successive non implementa un test alfa (o stato di test alfa). Questo può essere controllato usando un pixel shader o con funzionalità di profondità/stencil.



 

## <a name="depth-stencil-testing-overview"></a>Depth-Stencil dei test

Un buffer depth-stencil, creato come risorsa trama, può contenere sia dati di profondità che dati di stencil. I dati di profondità vengono usati per determinare quali pixel si trovano più vicini alla fotocamera e i dati dello stencil vengono usati per mascherare i pixel che possono essere aggiornati. In definitiva, i dati dei valori di profondità e di stencil vengono usati dalla fase di unione dell'output per determinare se un pixel deve essere disegnato o meno. Il diagramma seguente illustra concettualmente come viene eseguito il test depth-stencil.

![Diagramma del funzionamento dei test depth-stencil](images/d3d10-depth-stencil-test.png)

Per configurare il test depth-stencil, vedere [Configuring Depth-Stencil Functionality](d3d10-graphics-programming-guide-depth-stencil.md). Un oggetto depth-stencil incapsula lo stato depth-stencil. Un'applicazione può specificare lo stato depth-stencil oppure la fase OM userà i valori predefiniti. Le operazioni di fusione vengono eseguite in base ai pixel se il multicampionamento è disabilitato. Se il multicampionamento è abilitato, la fusione viene eseguita in base al multicampionamento.

Il processo di utilizzo del buffer di profondità per determinare quale pixel deve essere disegnato è detto buffering di profondità, detto anche z-buffering.

Quando i valori di profondità raggiungono la fase di unione dell'output (proveniente dall'interpolazione o da un pixel shader), vengono sempre regolati: z = min(Viewport.MaxDepth,max(Viewport.MinDepth,z)) in base al formato/precisione del buffer di profondità, usando regole a virgola mobile. Dopo la chiusura, il valore di profondità viene confrontato (usando DepthFunc) con il valore depth-buffer esistente. Se non è associato alcun buffer di profondità, il test di profondità viene sempre superato.

Se non è presente alcun componente stencil nel formato depth-buffer o nessun limite di buffer di profondità, il test degli stencil viene sempre superato. In caso contrario, la funzionalità rimane invariata rispetto a Direct3D 9.

Può essere attivo un solo buffer di profondità/stencil alla volta. Qualsiasi visualizzazione risorse associata deve corrispondere (stesse dimensioni e dimensioni) alla visualizzazione profondità/stencil. Ciò non significa che le dimensioni della risorsa devono corrispondere, ma solo che le dimensioni della visualizzazione devono corrispondere.

Per altre informazioni sui test degli stencil di profondità, vedere [l'esercitazione 14.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)

## <a name="blending-overview"></a>Cenni preliminari sulla fusione

La fusione combina uno o più valori di pixel per creare un colore pixel finale. Il diagramma seguente illustra il processo di fusione dei dati pixel.

![diagramma del funzionamento della fusione dei dati](images/d3d10-blend-state.png)

Concettualmente, è possibile visualizzare questo diagramma di flusso implementato due volte nella fase di unione dell'output: il primo combina i dati RGB, mentre in parallelo un secondo combina i dati alfa. Per informazioni su come usare l'API per creare e impostare lo stato di blend, vedere [Configuring Blending Functionality](d3d10-graphics-programming-guide-blend-state.md).

La blend a funzione fissa può essere abilitata in modo indipendente per ogni destinazione di rendering. Esiste tuttavia un solo set di controlli blend, in modo che la stessa fusione sia applicata a tutti gli oggetti RenderTargets con la fusione abilitata. I valori di blend (incluso BlendFactor) vengono sempre ancorati all'intervallo del formato di destinazione di rendering prima della fusione. Il controllo viene eseguito per ogni destinazione di rendering, rispettando il tipo di destinazione di rendering. L'unica eccezione è per i formati float16, float11 o float10 che non sono ancorati in modo che le operazioni di blend su questi formati possano essere eseguite con almeno uguale precisione/intervallo come formato di output. Gli zeri naN e con segno vengono propagati per tutti i casi (inclusi i pesi di blend 0,0).

Quando si usano destinazioni di rendering sRGB, il runtime converte il colore di destinazione del rendering nello spazio lineare prima di eseguire la fusione. Il runtime converte nuovamente il valore blended finale nello spazio sRGB prima di salvare il valore nella destinazione di rendering.

Differenze tra Direct3D 9 e Direct3D 10:

- In Direct3D 9 la fusione di funzioni fisse può essere abilitata in modo indipendente per ogni destinazione di rendering.
- In Direct3D 10 e versioni successive è presente una descrizione dello stato di blend. Pertanto, è possibile impostare un valore di fusione per tutte le destinazioni di rendering.



 

### <a name="dual-source-color-blending"></a>Dual-Source color blending

Questa funzionalità consente alla fase di unione dell'output di usare contemporaneamente entrambi gli output pixel shader (o0 e o1) come input per un'operazione di fusione con la singola destinazione di rendering nello slot 0. Le operazioni di blend valide includono: add, subtract e revsubtract. Le opzioni di blend valide per SrcBlend, DestBlend, SrcBlendAlpha o DestBlendAlpha includono: **D3D11 \_ BLEND \_ SRC1 \_ COLOR,** **D3D11 \_ BLEND \_ INV \_ SRC1 \_ COLOR,** **D3D11 \_ BLEND \_ SRC1 \_ ALPHA,** **D3D11 \_ BLEND \_ INV \_ SRC1 \_ ALPHA**. L'equazione di blend e la maschera di scrittura di output specificano i componenti pixel shader output. I componenti aggiuntivi vengono ignorati.

La scrittura in pixel shader output (o2, o3 e così via) non è definita. non è possibile scrivere in una destinazione di rendering se non è associata a slot 0. La scrittura di oDepth è valida durante la fusione dei colori a doppia origine.

Per esempi, vedere [Blending pixel shader outputs](d3d10-graphics-programming-guide-blend-state.md).

## <a name="multiple-rendertargets-overview"></a>Cenni preliminari su più rendertargets

Un pixel shader può essere usato per eseguire il rendering di almeno 8 destinazioni di rendering separate, tutte dello stesso tipo (buffer, Texture1D, Texture1DArray e così via). Inoltre, tutte le destinazioni di rendering devono avere le stesse dimensioni in tutte le dimensioni (larghezza, altezza, profondità, dimensioni della matrice, conteggi dei campioni). Ogni destinazione di rendering può avere un formato dati diverso.

È possibile usare qualsiasi combinazione di slot di destinazioni di rendering (fino a 8). Tuttavia, una visualizzazione delle risorse non può essere associata a più slot di destinazione di rendering contemporaneamente. Una vista può essere riutilizzata finché le risorse non vengono usate contemporaneamente.

## <a name="output-write-mask-overview"></a>Cenni preliminari Output-Write mask

Usare una maschera di output/scrittura per controllare (per componente) quali dati possono essere scritti in una destinazione di rendering.

## <a name="sample-mask-overview"></a>Panoramica della maschera di esempio

Una maschera di esempio è una maschera di code coverage multicampionamento a 32 bit che determina quali campioni vengono aggiornati nelle destinazioni di rendering attive. È consentita una sola maschera di esempio. Il mapping dei bit in una maschera di esempio agli esempi in una risorsa è definito da un utente. Per il rendering di n campioni, vengono usati i primi n bit (dall'LSB) della maschera di esempio (32 bit è il numero massimo di bit).


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                    | Descrizione                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configurazione Depth-Stencil funzionalità](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | Questa sezione illustra i passaggi per configurare il buffer depth-stencil e lo stato depth-stencil per la fase di unione dell'output.<br/>                                                                                                                           |
| [Configurazione della funzionalità di blending](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Le operazioni di fusione vengono eseguite su ogni pixel shader output (valore RGBA) prima che il valore di output venga scritto in una destinazione di rendering. Se il multicampionamento è abilitato, la fusione viene eseguita in ogni multicampionamento. In caso contrario, la fusione viene eseguita su ogni pixel.<br/> |
| [Distorsione della profondità](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | I poligoni coplanari nello spazio 3D possono essere visualizzati come se non fossero coplanari aggiungendo una distorsione z (o distorsione della profondità) a ognuno di essi.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

