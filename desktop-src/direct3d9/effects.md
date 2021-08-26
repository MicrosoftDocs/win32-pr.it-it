---
description: Un effetto Microsoft DirectX consente l'integrazione di vertex shader e pixel shader con lo stato della pipeline per il rendering degli oggetti. Gli effetti sono il passaggio logico successivo nella combinazione degli shader per produrre condizioni di rendering univoche.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Effetti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ed52a3a75f4b0682be4447f02ed305cf026af6aa30a59e921f4fa23f0e2211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985987"
---
# <a name="effects-direct3d-9"></a>Effetti (Direct3D 9)

Un effetto Microsoft DirectX consente l'integrazione di vertex shader e pixel shader con lo stato della pipeline per il rendering degli oggetti. Gli effetti sono il passaggio logico successivo nella combinazione degli shader per produrre condizioni di rendering univoche.

Gli effetti offrono anche un modo pratico per scrivere shader per versioni hardware diverse. Poiché schede video diverse supportano funzionalità diverse, un'applicazione può scrivere diverse tecniche che verranno eseguite su un'ampia gamma di dispositivi. In questo modo, se l'applicazione è in esecuzione nell'hardware più recente e più grande, l'applicazione può eseguire la tecnica di effetto più sofisticata. D'altra parte, è possibile scegliere automaticamente tecniche di effetto meno sofisticate per l'esecuzione su hardware meno costoso o meno idoneo.

Un effetto può sostituire l'elaborazione dei vertici e parte dell'elaborazione pixel eseguita dalla pipeline grafica. Un esempio di effetto che usa un vertex shader e un pixel shader è riportato nell'esempio BasicHLSL. È possibile ottenere questo esempio e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

Per altre informazioni sugli effetti, vedere gli argomenti seguenti:

-   [Scrittura di un effetto](writing-an-effect.md)
-   [Uso di un effetto](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Effetti e pipeline 3D

Il diagramma seguente illustra la pipeline.

![Diagramma della pipeline 3D](images/effects-block-diagram.png)

La pipeline trasforma i dati di input in pixel di output che riempiono il buffer dei frame. I dati di input provengono da oggetti che sono costituito da vertici nello spazio oggetti o da superfici di ordine superiore create da N patch, patch rettangolari e patch di triangolo. Dopo che i dati di input sono stati suddivisi a schema, la pipeline esegue l'elaborazione dei vertici, l'elaborazione primitiva e l'elaborazione pixel prima di generare i colori pixel finali.

L'elaborazione di vertici e pixel può essere eseguita dalla pipeline di funzioni fisse o implementata con shader programmabili. La tessellazione dei dati di input, l'elaborazione primitiva e gli output dei dati sono controllati dallo stato della pipeline. Tutto questo può essere integrato in un effetto. Un effetto imposta lo stato che controlla il funzionamento della pipeline. Gli effetti gestiscono gli shader programmabili e lo stato della funzione fissa.

Gli effetti possono salvare e ripristinare lo stato, lasciando il dispositivo nello stesso stato di prima dell'esecuzione dell'effetto. I tipi di stato che un effetto può gestire includono:

-   Stato dello shader. Ciò include la creazione e l'eliminazione di shader, l'impostazione delle costanti dello shader, l'impostazione dello stato dello shader e il rendering con gli shader.
-   Stato della trama e del campionatore. Ciò include la specifica dei file di trama, l'inizializzazione delle fasi della trama, la creazione di oggetti campionatore e l'impostazione dello stato del campionatore.
-   Altro stato della pipeline. Sono inclusi gli stati per l'impostazione di trasformazioni, illuminazione, materiali e opzioni di rendering. Possono essere variabili globali o locali. Le variabili possono essere impostate dall'effetto stesso o dall'applicazione.

Gli effetti contengono più opzioni di rendering denominate tecniche. Ogni tecnica incapsula le variabili globali, lo stato della pipeline, lo stato della trama e del campionatore e lo stato dello shader. Un singolo stile viene implementato in un passaggio di rendering. Uno o più passaggi possono essere incapsulati in una tecnica. Tutti i passaggi e le tecniche possono essere convalidati per verificare se il codice dell'effetto verrà eseguito nel dispositivo hardware.

## <a name="effects-save-and-restore-state"></a>Stato di salvataggio e ripristino degli effetti

Gli effetti gestiscono lo stato. La parola stato viene usata in modo molto ampio qui perché include tutti i tipi di informazioni necessarie alla pipeline per specificare le condizioni di rendering. Sono incluse quasi tutte le aree funzionali della pipeline.

Le opzioni di rendering sono controllate da tecniche e passaggi. Un'applicazione esegue il rendering di un effetto impostando una tecnica attiva ed esegue il rendering di uno o più passaggi. Tutto il rendering in un effetto viene eseguito all'interno di una coppia corrispondente [**di chiamate Begin**](id3dxeffect--begin.md) ed [**End.**](id3dxeffect--end.md) Quando **viene chiamato Begin,** viene creato un blocco di stato e lo stato del dispositivo viene salvato (se non diversamente specificato). Dopo che una tecnica esegue il rendering dei passaggi specificati dall'applicazione per il rendering, viene chiamato **End** per terminare la tecnica attiva. Il sistema degli effetti risponde ripristinando automaticamente lo stato della pipeline acquisito nel blocco di stato (a meno che non si sceva di disabilitare questa funzionalità di salvataggio e ripristino).

Quando si programmano sequenze di rendering a più passi, ognuna delle quali richiede la propria configurazione dello stato, gli effetti possono ridurre la gestione necessaria per tenere traccia delle modifiche dello stato. Per altre informazioni sugli stati che possono essere salvati e ripristinati dagli effetti, vedere [Stati degli effetti (Direct3D 9).](effect-states.md)

## <a name="effects-can-share-parameters"></a>Gli effetti possono condividere parametri

I parametri di effetto sono tutte le variabili non statiche dichiarate in un effetto. Può includere variabili globali e annotazioni. I parametri degli effetti possono essere condivisi tra diversi effetti dichiarando i parametri con la parola chiave shared e quindi creando l'effetto con un pool di effetti.

Gli effetti clonati usano lo stesso pool di effetti dell'effetto da cui vengono clonati. La clonazione di un effetto crea una copia esatta di un effetto, incluse variabili globali, tecniche, passaggi e annotazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
