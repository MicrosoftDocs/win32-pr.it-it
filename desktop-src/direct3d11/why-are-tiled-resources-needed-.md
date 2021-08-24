---
title: Perché sono necessarie risorse affiancate
description: Le risorse affiancate sono necessarie in modo che meno memoria gpu (Graphics Processing Unit) sia sprecata archiviando aree di superfici che l'applicazione sa non saranno accessibili e l'hardware può comprendere come filtrare tra riquadri adiacenti.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c2da8602cb0b2026ea8360c88388c18d37598d5672f547659cc6ea93e78e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631941"
---
# <a name="why-are-tiled-resources-needed"></a>Perché sono necessarie risorse affiancate?

Le risorse affiancate sono necessarie in modo che meno memoria gpu (Graphics Processing Unit) sia sprecata archiviando aree di superfici che l'applicazione sa non saranno accessibili e l'hardware può comprendere come filtrare tra riquadri adiacenti.

In un sistema grafico, ovvero il sistema operativo, il driver di visualizzazione e l'hardware grafico, senza supporto delle risorse affiancate, il sistema grafico gestisce tutte le allocazioni di memoria Direct3D con granularità della sottorisorsa. Per un [buffer](overviews-direct3d-11-resources-buffers.md), l'intero buffer è la sottorisorsa. Per una [trama](overviews-direct3d-11-resources-textures.md) (ad esempio, [**Texture2D),**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)ogni livello mip è una sottorisorsa; per una matrice di trame ( ad [**esempio, Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)), ogni livello mip in una determinata sezione di matrice è una sottorisorsa. Il sistema grafico espone solo la possibilità di gestire il mapping delle allocazioni a questa granularità della sottorisorsa. Nel contesto delle risorse affiancate, il "mapping" si riferisce a rendere i dati visibili alla GPU.

Si supponga che un'applicazione sappia che una particolare operazione di rendering deve accedere solo a una piccola parte di una catena mipmap dell'immagine (ad esempio non l'intera area di una mipmap specificata). Idealmente, l'app potrebbe informare il sistema grafico su questa necessità. Il sistema grafico si preoccupa quindi solo di assicurarsi che la memoria necessaria sia mappata nella GPU senza paging in una quantità eccessiva di memoria. In realtà, senza il supporto delle risorse affiancate, il sistema grafico può essere informato solo sulla memoria di cui è necessario eseguire il mapping nella GPU con granularità della sottorisorsa (ad esempio, un intervallo di livelli mipmap completi a cui è possibile accedere). Non è presente alcun errore di richiesta nel sistema grafico, quindi potenzialmente è necessario usare una grande quantità di memoria GPU in eccesso per eseguire il mapping di sottorisorse complete prima che venga eseguito un comando di rendering che fa riferimento a qualsiasi parte della memoria. Questo è solo un problema che rende difficile l'uso di allocazioni di memoria di grandi dimensioni in Direct3D senza supporto delle risorse affiancate.

Direct3D 11 supporta superfici [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) con un massimo di 16384 pixel su un determinato lato. Un'immagine larga 16384 per 16384 e alta 4 byte per pixel consumerebbe 1 GB di memoria video e l'aggiunta di mipmap raddoppierebbe tale quantità. In pratica, raramente è necessario fare riferimento a tutti i 1 GB in una singola operazione di rendering.

Alcuni sviluppatori di giochi modellano superfici di terreno grandi fino a 128.000 per 128.000. Il modo in cui queste funzionino sulle GPU esistenti è suddividere la superficie in riquadri sufficientemente piccoli da poter gestire l'hardware. L'applicazione deve determinare quali riquadri potrebbero essere necessari e caricarli in una cache di trame nella GPU, un sistema di paging software. Un aspetto negativo significativo di questo approccio deriva dall'hardware che non sa nulla del paging in corso: quando una parte di un'immagine deve essere visualizzata sullo schermo che si trova a livello di riquadri, l'hardware non sa come eseguire filtri a funzione fissa (ovvero efficiente) tra riquadri. Ciò significa che l'applicazione che gestisce il proprio affiancamento software deve ricorrere al filtro manuale delle trame nel codice shader (che diventa molto costoso se si desidera un filtro anisotropo di buona qualità) e/o ai riquadri di creazione della memoria di rifiuti che contengono dati da riquadri adiacenti, in modo che il filtro hardware a funzione fissa possa continuare a fornire assistenza.

Se una rappresentazione affiancata delle allocazioni di superfici può essere una funzionalità di prima classe nel sistema grafico, l'applicazione potrebbe indicare all'hardware quali riquadri rendere disponibili. In questo modo, meno memoria GPU viene sprecata archiviando aree di superfici che l'applicazione sa non saranno accessibili e l'hardware può comprendere come filtrare tra riquadri adiacenti, alleviando parte del problema riscontrato dagli sviluppatori che eseguono la affiancamento software da soli.

Tuttavia, per fornire una soluzione completa, è necessario fare qualcosa per gestire il fatto che, indipendentemente dal fatto che sia supportata la affiancamento all'interno di una superficie, la dimensione massima della superficie è attualmente 16384, da nessuna parte vicino al valore di 128K+ che le applicazioni vogliono già. È sufficiente che l'hardware supporti dimensioni di trama più grandi è un approccio, ma ci sono costi e/o compromessi significativi per questa route. Il percorso del filtro trame e il percorso di rendering di Direct3D 11 sono già saturati in termini di precisione nel supporto di trame da 16.000 con gli altri requisiti, ad esempio il supporto degli extent del viewport che cadono dalla superficie durante il rendering o il supporto della disposizione della trama dal bordo della superficie durante il filtro. Una possibilità consiste nel definire un compromesso in modo tale che, quando le dimensioni della trama aumentano oltre i 16.000,000, la funzionalità/precisione viene data in qualche modo. Anche con questa concessione, tuttavia, potrebbero essere necessari costi hardware aggiuntivi in termini di capacità di indirizzamento in tutto il sistema hardware per passare a dimensioni di trama maggiori.

Un problema che si verifica quando le trame sono molto grandi è che le coordinate della trama a virgola mobile a precisione singola (e gli interpolatori associati per supportare la rasterizzazione) eseguono la precisione per specificare in modo accurato le posizioni sulla superficie. Ne deriva un filtro trame instabilità. Un'opzione costosa potrebbe richiedere il supporto dell'interpolatore a precisione doppia, anche se ciò potrebbe essere eccessivo in base a un'alternativa ragionevole.

Un nome alternativo per le risorse affiancate è "trama di tipo sparse". "Sparse" indica sia la natura affiancata delle risorse, sia il motivo principale per cui vengono affiancate, che non tutte devono essere mappate contemporaneamente. In effetti, un'applicazione potrebbe creare intenzionalmente una risorsa affiancata in cui non vengono creati dati per tutte le aree+mip della risorsa. Pertanto, il contenuto stesso potrebbe essere di tipo sparse e il mapping del contenuto nella memoria GPU in un determinato momento sarebbe un subset di questo (ancora più sparse).

Un altro scenario che potrebbe essere servito da risorse affiancate consiste nell'abilitare più risorse di dimensioni/formati diversi per condividere la stessa memoria. In alcuni casi le applicazioni hanno set esclusivi di risorse che non vengono usate contemporaneamente o risorse create solo per un uso molto breve e quindi distrutte, seguite dalla creazione di altre risorse. Una forma di generalità che può uscire da "risorse affiancate" è che è possibile consentire all'utente di puntare più risorse diverse alla stessa memoria (sovrapposta). In altre parole, la creazione e la distruzione delle "risorse" (che definiscono una dimensione/formato e così via) possono essere disaccociate dalla gestione della memoria sottostante le risorse dal punto di vista dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 