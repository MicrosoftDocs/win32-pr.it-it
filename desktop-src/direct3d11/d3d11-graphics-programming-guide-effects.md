---
title: Effetti (Direct3D 11)
description: Un effetto DirectX è una raccolta dello stato della pipeline, impostata dalle espressioni scritte in HLSL e da una sintassi specifica per il Framework degli effetti.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8952a35e1212f7d50956cc54e7a046db9f87b3b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728399"
---
# <a name="effects-direct3d-11"></a>Effetti (Direct3D 11)

Un effetto DirectX è una raccolta dello stato della pipeline, impostata dalle espressioni scritte in [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) e da una sintassi specifica per il Framework degli effetti.

Dopo la compilazione di un effetto, utilizzare le API del Framework effetti per eseguire il rendering. La funzionalità degli effetti può variare da qualcosa di semplice come un vertex shader che trasforma la geometria e un pixel shader che restituisce un colore a tinta unita, a una tecnica di rendering che richiede più sessioni, utilizza ogni fase della pipeline grafica e modifica lo stato dello shader, nonché lo stato della pipeline non associato agli shader programmabili.

Il primo passaggio consiste nell'organizzare lo stato che si vuole controllare in un effetto. Sono inclusi lo stato dello shader (Vertex, Hull, Domain, Geometry, pixel e compute shader), lo stato di trama e campionatore usato dagli shader e altro stato della pipeline non programmabile. È possibile creare un effetto in memoria come una stringa di testo, ma in genere la dimensione diventa sufficientemente grande da poter archiviare lo stato dell'effetto in un file di effetti (un file di testo che termina con l'estensione FX). Per usare un effetto, è necessario compilarlo (per verificare la sintassi di HLSL e la sintassi del Framework di effetto), inizializzare lo stato dell'effetto tramite chiamate API e modificare il ciclo di rendering per chiamare le API di rendering.

Un effetto incapsula tutto lo stato di rendering richiesto da un particolare effetto in una singola funzione di rendering denominata tecnica. Un passaggio è un subset di una tecnica che contiene lo stato di rendering. Per implementare un effetto di rendering a più passaggi, implementare uno o più passaggi all'interno di una tecnica. Si immagini, ad esempio, di voler eseguire il rendering di una geometria con un set di buffer di profondità/stencil, quindi disegnare alcuni sprite. È possibile implementare il rendering Geometry nel primo passaggio e il disegno sprite nel secondo passaggio. Per eseguire il rendering dell'effetto, è sufficiente eseguire il rendering di entrambi i passaggi nel ciclo di rendering. È possibile implementare un numero qualsiasi di tecniche in un effetto. Naturalmente, maggiore è il numero di tecniche, maggiore è il tempo di compilazione per l'effetto. Un modo per sfruttare questa funzionalità consiste nel creare effetti con tecniche progettate per l'esecuzione su hardware diverso. Questo consente a un'applicazione di eseguire correttamente il downgrade delle prestazioni in base alle funzionalità hardware rilevate.

Un set di tecniche può essere raggruppato in un gruppo (che usa la sintassi "FXGroup"). Le tecniche possono essere raggruppate in qualsiasi modo. È ad esempio possibile creare più gruppi, uno per materiale; ogni materiale può avere una tecnica per ogni livello di hardware; ogni tecnica avrà un set di passaggi che definiscono il materiale nell'hardware specifico.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                | Descrizione                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organizzazione dello stato in un effetto](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture.<br/>                                                                   |
| [Interfacce di sistema effetti](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | Il sistema degli effetti definisce diverse interfacce per la gestione dello stato dell'effetto.<br/>                                                                                  |
| [Interfacce specializzate](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispone di diversi metodi per eseguire il cast dell'interfaccia in un particolare tipo di interfaccia necessaria.<br/> |
| [Interfacce e classi negli effetti](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Esistono diversi modi per usare le classi e le interfacce in Effects 11.<br/>                                                                                         |
| [Rendering di un effetto](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato.<br/>                                                                         |
| [Clonazione di un effetto](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | La clonazione di un effetto crea una seconda copia pressoché identica dell'effetto.<br/>                                                                                 |
| [Sintassi di Stream out](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Un geometry shader con flusso in uscita viene dichiarato con una particolare sintassi.<br/>                                                                                  |
| [Differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | In questo argomento vengono illustrate le differenze tra gli effetti 10 e gli effetti 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

