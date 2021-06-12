---
title: Effetti (Direct3D 11)
description: Informazioni sugli effetti di Direct3D 11. Un effetto è lo stato della pipeline, impostato da espressioni scritte in HLSL e da una sintassi specifica del framework degli effetti.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063b554e28786b48a467de12042bf6ada99645a9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010644"
---
# <a name="effects-direct3d-11"></a>Effetti (Direct3D 11)

Un effetto DirectX è una raccolta di stato della pipeline, impostata da espressioni scritte in [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) e da una sintassi specifica del framework degli effetti.

Dopo aver eseguito la compilazione di un effetto, usare le API del framework degli effetti per il rendering. La funzionalità degli effetti può variare da un elemento semplice come un vertex shader che trasforma la geometria e un pixel shader che restituisce un colore a tinta unita, a una tecnica di rendering che richiede più passaggi, usa ogni fase della pipeline grafica e modifica lo stato dello shader e lo stato della pipeline non associato agli shader programmabili.

Il primo passaggio consiste nell'organizzare lo stato che si vuole controllare in un effetto. Sono inclusi lo stato dello shader (vertice, struttura, dominio, geometria, pixel e compute shader), lo stato della trama e del campionatore usato dagli shader e altri stati della pipeline non programmabili. È possibile creare un effetto in memoria come stringa di testo, ma in genere le dimensioni sono sufficienti per archiviare lo stato dell'effetto in un file di effetto (un file di testo che termina con un'estensione fx). Per usare un effetto, è necessario compilarlo (per controllare la sintassi HLSL e la sintassi del framework degli effetti), inizializzare lo stato dell'effetto tramite chiamate API e modificare il ciclo di rendering per chiamare le API di rendering.

Un effetto incapsula tutto lo stato di rendering richiesto da un determinato effetto in una singola funzione di rendering denominata tecnica. Un passaggio è un sotto-set di una tecnica, che contiene lo stato di rendering. Per implementare un effetto di rendering a più passaggi, implementare uno o più passaggi all'interno di una tecnica. Si supponga, ad esempio, di voler eseguire il rendering di una geometria con un set di buffer di profondità/stencil e quindi di disegnare alcuni sprite sopra di questo. È possibile implementare il rendering della geometria nel primo passaggio e il disegno dello sprite nel secondo passaggio. Per eseguire il rendering dell'effetto, è sufficiente eseguire il rendering di entrambi i passaggi nel ciclo di rendering. È possibile implementare un numero qualsiasi di tecniche in un effetto. Naturalmente, maggiore è il numero di tecniche, maggiore sarà il tempo di compilazione per l'effetto. Un modo per sfruttare questa funzionalità consiste nel creare effetti con tecniche progettate per l'esecuzione su hardware diverso. Ciò consente a un'applicazione di eseguire normalmente il downgrade delle prestazioni in base alle funzionalità hardware rilevate.

Un set di tecniche può essere raggruppato in un gruppo (che usa la sintassi "fxgroup"). Le tecniche possono essere raggruppate in qualsiasi modo. Ad esempio, è possibile creare più gruppi, uno per ogni materiale. ogni materiale può avere una tecnica per ogni livello hardware; ogni tecnica avrebbe un set di passaggi che definiscono il materiale sull'hardware specifico.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                | Descrizione                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organizzazione dello stato in un effetto](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Con Direct3D 11, lo stato dell'effetto per determinate fasi della pipeline è organizzato in base alle strutture.<br/>                                                                   |
| [Interfacce del sistema di effetti](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | Il sistema di effetti definisce diverse interfacce per la gestione dello stato dell'effetto.<br/>                                                                                  |
| [Specializing Interfaces](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) include diversi metodi per eseguire il cast dell'interfaccia nel tipo specifico di interfaccia necessario.<br/> |
| [Interfacce e classi negli effetti](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Esistono molti modi per usare classi e interfacce in Effects 11.<br/>                                                                                         |
| [Rendering di un effetto](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Un effetto può essere usato per archiviare informazioni o per eseguire il rendering usando un gruppo di stato.<br/>                                                                         |
| [Clonazione di un effetto](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | La clonazione di un effetto crea una seconda copia quasi identica dell'effetto.<br/>                                                                                 |
| [Sintassi di flusso in uscita](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Un geometry shader con flusso out viene dichiarato con una particolare sintassi.<br/>                                                                                  |
| [Differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | Questo argomento illustra le differenze tra Effetti 10 ed Effetti 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

