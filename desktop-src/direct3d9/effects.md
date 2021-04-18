---
description: Un effetto Microsoft DirectX consente l'integrazione di Vertex e pixel shader con lo stato della pipeline per il rendering degli oggetti. Gli effetti rappresentano il passaggio logico successivo nella combinazione degli shader per produrre condizioni di rendering univoche.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Effetti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48d2ff5548dff29ede4b360bd2c319f85fafa3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304100"
---
# <a name="effects-direct3d-9"></a>Effetti (Direct3D 9)

Un effetto Microsoft DirectX consente l'integrazione di Vertex e pixel shader con lo stato della pipeline per il rendering degli oggetti. Gli effetti rappresentano il passaggio logico successivo nella combinazione degli shader per produrre condizioni di rendering univoche.

Gli effetti forniscono anche un modo pratico per scrivere shader per versioni hardware diverse. Poiché schede video diverse supportano funzionalità diverse, un'applicazione può scrivere diverse tecniche che vengono eseguite su una vasta gamma di dispositivi. In questo modo, se l'applicazione è in esecuzione nell'hardware più recente e più recente, l'applicazione può eseguire la tecnica degli effetti più sofisticata. D'altra parte, le tecniche di effetto meno sofisticate possono essere scelte automaticamente per l'esecuzione su hardware meno costosi o meno idonei.

Un effetto può sostituire l'elaborazione del vertice e parte dell'elaborazione dei pixel eseguita dalla pipeline grafica. Un esempio di effetto che usa un vertex shader e un pixel shader è nell'esempio BasicHLSL. È possibile ottenere questo esempio e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

Per ulteriori informazioni sugli effetti, vedere gli argomenti seguenti:

-   [Scrittura di un effetto](writing-an-effect.md)
-   [Uso di un effetto](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Effetti e pipeline 3D

Il diagramma seguente illustra la pipeline.

![diagramma della pipeline 3D](images/effects-block-diagram.png)

La pipeline trasforma i dati di input in pixel di output che riempiono il buffer del frame. I dati di input provengono da oggetti costituiti da vertici nello spazio degli oggetti o da aree di ordine superiore create da N-patch, patch rettangolari e patch di triangolo. Una volta che i dati di input sono stati tassellati, la pipeline esegue l'elaborazione dei vertici, l'elaborazione primitiva e i pixel prima di generare i colori finali dei pixel.

L'elaborazione dei vertici e dei pixel può essere eseguita dalla pipeline della funzione fissa oppure può essere implementata con shader programmabili. I dati di input a mosaico, elaborazione primitive e output dei dati sono controllati dallo stato della pipeline. Tutto questo può essere integrato in un effetto. Un effetto imposta lo stato che controlla la modalità di funzionamento della pipeline. Gli effetti gestiscono shader programmabili nonché lo stato della funzione fissa.

Gli effetti possono salvare e ripristinare lo stato, lasciando il dispositivo nello stesso stato di prima dell'esecuzione dell'effetto. I tipi di stato che un effetto può gestire includono:

-   Stato dello shader. Sono incluse la creazione e l'eliminazione di shader, l'impostazione di costanti shader, l'impostazione dello stato dello shader e il rendering con gli shader.
-   Stato di trama e campionatore. Sono inclusi i file di trama, l'inizializzazione di fasi di trama, la creazione di oggetti Sampler e l'impostazione dello stato del campionatore
-   Altro stato della pipeline. Sono inclusi gli Stati per l'impostazione di trasformazioni, illuminazione, materiali e opzioni di rendering. Possono essere variabili globali o locali. Le variabili possono essere impostate sia dall'effetto stesso che dall'applicazione.

Gli effetti contengono più opzioni di rendering denominate tecniche. Ogni tecnica incapsula le variabili globali, lo stato della pipeline, lo stato della trama e del campionatore e lo stato dello shader. Un unico stile viene implementato in un passaggio di rendering. Una o più sessioni possono essere incapsulate in una tecnica. Tutti i passaggi e le tecniche possono essere convalidati per verificare se il codice dell'effetto verrà eseguito sul dispositivo hardware.

## <a name="effects-save-and-restore-state"></a>Stato di salvataggio e ripristino degli effetti

Gestione degli effetti sullo stato. Lo stato della parola viene usato in modo molto ampio in quanto include tutti i tipi di informazioni necessarie alla pipeline per specificare le condizioni di rendering. Sono incluse quasi tutte le aree funzionali della pipeline.

Le opzioni di rendering sono controllate da tecniche e sessioni. Un'applicazione esegue il rendering di un effetto impostando una tecnica attiva e il rendering di uno o più passaggi. Tutto il rendering in un effetto viene eseguito all'interno di una coppia corrispondente di chiamate [**Begin**](id3dxeffect--begin.md) e [**end**](id3dxeffect--end.md) . Quando **Begin** viene chiamato, viene creato un stateblock e viene salvato lo stato del dispositivo, a meno che non venga specificato diversamente. Dopo che una tecnica ha eseguito il rendering dei passaggi specificati dall'applicazione per il rendering, viene chiamato **end** per terminare la tecnica attiva. Il sistema di effetto risponde ripristinando automaticamente lo stato della pipeline acquisito nel blocco di stato (a meno che non si scelga di disabilitare questa funzionalità di salvataggio e ripristino).

Quando si programmano sequenze di rendering a più passaggi, ciascuna delle quali richiede una propria configurazione dello stato, gli effetti possono ridurre la manutenzione necessaria per tenere traccia delle modifiche dello stato. Per visualizzare altre informazioni sugli Stati che possono essere salvati e ripristinati dagli effetti, vedere [Stati degli effetti (Direct3D 9)](effect-states.md).

## <a name="effects-can-share-parameters"></a>Gli effetti possono condividere parametri

I parametri degli effetti sono tutte le variabili non statiche dichiarate in un effetto. Possono essere incluse le variabili globali e le annotazioni. I parametri effetti possono essere condivisi tra diversi effetti dichiarando i parametri con la parola chiave Shared e quindi creando l'effetto con un pool di effetti.

Gli effetti clonati utilizzano lo stesso pool di effetti dell'effetto da cui vengono clonati. La clonazione di un effetto crea una copia esatta di un effetto, incluse le variabili globali, le tecniche, i passaggi e le annotazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori per Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
